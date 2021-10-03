<template>
  <div class="MainContainer">
    <div class="content">
      <div>
        <h1>{{ $t("find") }}</h1>
      </div>
      <div class="custom-row">
        <CardComponent
          v-for="(item, i) in items"
          :key="i"
          :title="item.title"
          :titleDescription="item.titleDescription"
          :priceDescription="item.priceDescription"
          :isFree="item.isFree"
          :price="item.price"
        />
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      items: [
        {
          title: "BASIC",
          titleDescription: "FREE now and forever",
          isFree: true,
          priceDescription: [
            "Utilize our point of sales system",
            "Control your dishes and prices",
            "Table booking",
            "Free takeaway system"
          ],
          price: "",
        },
        {
          title: "Plus",
          titleDescription: "Coming Soon",
          isFree: false,
          priceDescription: [
            "Table and seat management",
            "Send out notifications to followers",
            "Curated data reports",
            "Events and special offers"
          ],
          price: "599 DKK",
        },
        {
          title: "Pro",
          titleDescription: "Coming Soon",
          isFree: false,
          priceDescription: [
            "Loyalty",
            "24 hours support",
            "Kitchen display support",
            "Accounting Integration",
          ],
          price: "1299 DKK",
        },
      ],
    };
  },
};
</script>
<style lang="scss" scoped>
.MainContainer {
  position: relative;
  scroll-behavior: smooth;
  display: flex;
  justify-content: center;
  height: 100%;

  h1 {
    padding-bottom: 30px;
    font-size: calc((1.1 - 1) * 1.2vw + 2.5rem);
    color: rgb(202, 11, 53);
  }
  .content {
    width: 80%;
    margin-top: 60px;
    padding: 60px 0;
    display: flex;
    flex-direction: column;
    grid-gap: 60px;
    text-align: center;
    align-content: center;
    justify-content: center;

    .custom-row {
      width: 100% !important;
      height: 100% !important;
      display: grid;
      gap: 40px;
      grid-template-columns: repeat(3, 1fr);
      justify-content: center;
    }
  }
}

@media only screen and (max-width: 1100px) {
  .MainContainer {
    height: 100% !important;
    .content {
      padding-bottom: 60px;
    }
  }
  .custom-row {
    width: 100% !important;
    display: flex !important;
    flex-direction: column !important;
    justify-content: space-evenly;
  }
}
@media not all and (min-resolution: 0.001dpcm) {
  @supports (-webkit-appearance: none) {
    .custom-row {
      div {
        padding: 20px;
      }
    }
  }
}
</style>