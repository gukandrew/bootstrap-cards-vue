<template>
  <div class="grey-bg container">
    <section id="minimal-statistics">
      <div class="row">
        <div class="col-12 mt-3 mb-1">
          <h4 class="text-uppercase">Minimal Statistics Cards</h4>
          <p>Statistics on minimal cards.</p>
        </div>
      </div>

      <div class="row">
        <card title="New Posts" value="278" icon-class="icon-pencil icon-big" icon-side="left" type="primary" />
        <card title="New Comments" value="156" icon-class="icon-speech icon-big" icon-side="left" type="primary" />
        <card title="Bounce Rate" value="64.89 %" icon-class="icon-graph icon-big" icon-side="left" type="warning" />
        <card title="Total Visits" value="423" icon-class="icon-graph icon-big" icon-side="left" type="danger" />
      </div>

      <div class="row">
        <card title="New Projects" value="278" icon-class="icon-rocket icon-big" icon-side="right" type="danger" />
        <card title="New Clients" value="156" icon-class="icon-user icon-big" icon-side="right" type="success" />
        <card title="Conversion Rate" value="64.89 %" icon-class="icon-pie-chart icon-big" icon-side="right" type="warning" />
        <card title="Support Tickets" value="423" icon-class="icon-support icon-big" icon-side="right" type="warning" />
      </div>

      <div class="row">
        <card title="New Posts" value="278" icon-class="icon-book-open icon-big" icon-side="right" type="primary" progress="80" progress-min="0" progress-max="100" />
        <card title="New Comments" value="156" icon-class="icon-bubbles icon-big" icon-side="right" type="warning" progress="35" />
        <card title="Bounce Rate" value="64.89 %" icon-class="icon-cup icon-big" icon-side="right" type="success" progress="60" />
        <card title="Total Visits" value="64.89 %" icon-class="icon-direction icon-big" icon-side="right" type="danger" progress="40" />
      </div>
    </section>

    <section id="stats-subtitle">
      <div class="row">
        <div class="col-12 mt-3 mb-1">
          <h4 class="text-uppercase">Statistics With Subtitle</h4>
          <p>Statistics on minimal cards with Title &amp; Sub Title.</p>
        </div>
      </div>

      <div class="row">
        <card-subtitle title="Total Posts" subtitle="Monthly blog posts" value="18,000" icon-class="icon-pencil icon-big" icon-side="left" type="primary" />
        <card-subtitle title="Total Comments" subtitle="Monthly blog comments" value="84,695" icon-class="icon-speech icon-big" icon-side="left" type="warning" />
      </div>

      <div class="row">
        <card-subtitle title="Total Sales" subtitle="Monthly Sales Amount" value="$76,456.00" icon-class="icon-heart icon-big" icon-side="right" type="danger" />
        <card-subtitle title="Total Cost" subtitle="Monthly Cost" value="$36,000.00" icon-class="icon-wallet icon-big" icon-side="right" type="success" />
      </div>
    </section>
  </div>
</template>

<script>
import card from './card.vue'
import cardSubtitle from './card-subtitle.vue'

export default {
  name: 'HelloWorld',
  components: {
    card,
    cardSubtitle
  }
}
</script>

<style lang="scss">
$simple-line-font-path: "~simple-line-icons/fonts/";
@import "~simple-line-icons/scss/simple-line-icons";

@import "../scss/_variables.scss";
@import "~bootstrap/scss/bootstrap";

body {
  background: linear-gradient(90deg, #7474bf 10%, #348ac7 90%);
  font-family: Montserrat, Georgia, 'Times New Roman', Times, serif;
}

$colors: (
  "primary": #00b5b8,
  "success": #16d39a,
  "warning": #ffa87d,
  "danger": #ff7588
);

@each $name, $color in $colors {
  .#{$name} {
    color: $color !important;
  }
  .bg-#{$name} {
    background-color: $color !important;
  }
}

.icon-big {
  font-size: 3rem !important;
}

.card {
  margin-bottom: 1.875rem;
  box-shadow: 0 10px 40px 0 rgba(62, 57, 107, 0.07), 0 2px 9px 0 rgba(62, 57, 107, 0.06);

  .media {
    display: flex;
    align-items: flex-start;

    .media-body {
      flex: 1;
    }
  }
}
</style>
