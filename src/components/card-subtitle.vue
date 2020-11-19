<template>
  <div class="col-xl-6 col-md-12">
    <div class="card">
      <div class="card-content">
        <div class="card-body cleartfix">
          <div class="media align-items-stretch">
            <div class="align-self-center" v-if="iconSide == 'left'">
              <i :class="[iconClass, type]"></i>
            </div>
            <div class="media-body" v-if="iconSide == 'left'">
              <h4>{{title}}</h4>
              <span>{{subtitle}}</span>
            </div>
            <div class="align-self-center" v-if="iconSide == 'left'">
              <h1>{{value}}</h1>
            </div>

            <div class="align-self-center" v-if="iconSide == 'right'">
              <h1 class="mr-2">{{value}}</h1>
            </div>
            <div class="media-body" v-if="iconSide == 'right'">
              <h4>{{title}}</h4>
              <span>{{subtitle}}</span>
            </div>
            <div class="align-self-center" v-if="iconSide == 'right'">
              <i :class="[iconClass, type]"></i>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: 'Title'
    },
    subtitle: {
      type: String,
      default: 'Some subtitle'
    },
    value: {
      type: String,
      default: '90%'
    },
    iconClass: {
      type: String,
      default: 'icon-pie-chart font-large-2'
    },
    iconSide: {
      type: String,
      default: 'left'
    },
    type: {
      type: String,
      default: 'primary'
    }
  }
}
</script>

<style>

</style>
