<template>

  <div class="wrapper">

    <parallax class="page-header header-filter" :style="headerStyle">

    </parallax>

    <div class="mt-1 main main-raised">

      <div class="section section-basic">
        <div class="container">
          <div class="title">
            <h2 style="margin: 0;">ToDo List: </h2>
            <router-link to="/form">
              <md-button style="max-height: 40px" class="md-primary">
                <p style="font-family: Helvetica,serif">Add ToDo</p>
              </md-button>
            </router-link>
          </div>
          <list-of-items></list-of-items>
        </div>
      </div>

    </div>
  </div>
</template>

<script>
import ListOfItems from "./components/ListOfItems";

export default {
  components: {
    ListOfItems
  },
  name: "index",
  bodyClass: "index-page",
  props: {
    image: {
      type: String,
      default: require("@/assets/img/vue-mk-header.jpg")
    }
  },
  computed: {
    headerStyle() {
      return {
        backgroundImage: `url(${this.image})`
      };
    }
  }
};
</script>
<style lang="scss">
.section-download {
  .md-button + .md-button {
    margin-left: 5px;
  }
}

@media all and (min-width: 991px) {
  .btn-container {
    display: flex;
  }
}
  .page-header {
    height: 155px !important;
  }
</style>
