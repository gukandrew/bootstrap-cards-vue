<template>
  <div class="col-xl-3 col-sm-6 col-12">
    <div class="card">
      <div class="card-content">
        <div class="card-body">
          <div class="media d-flex">
            <div class="align-self-center" v-if="iconSide == 'left'">
              <i :class="['float-left', iconClass, type]"></i>
            </div>

            <div class="media-body text-right" v-if="iconSide == 'left'">
              <h3 :class="type">{{value}}</h3>
              <span>{{title}}</span>
            </div>

            <div class="media-body text-left" v-if="iconSide == 'right'">
              <h3 :class="type">{{value}}</h3>
              <span>{{title}}</span>
            </div>

            <div class="align-self-center" v-if="iconSide == 'right'">
              <i :class="['float-right', iconClass, type]"></i>
            </div>
          </div>

          <div class="progress mt-1 mb-0" style="height: 7px" v-if="progress">
            <div
              :class="`progress-bar bg-${type}`"
              role="progressbar"
              :style="`width: ${progress}%`"
              :aria-valuenow="progress"
              :aria-valuemin="progressMin"
              :aria-valuemax="progressMax"
            ></div>
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
    },
    progress: String,
    progressMin: {
      type: String,
      default: '100'
    },
    progressMax: {
      type: String,
      default: '100'
    }
  }
}
</script>

<style>

</style>
