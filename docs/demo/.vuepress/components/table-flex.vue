<template lang="pug">
.group.is-space
  - var media_first = ["mobile", "fablet", "tablet", "desktop", "wide"]
  - var media_only = ["mobile-only", "fablet-only", "tablet-only", "desktop-only"]
  - var media_range = ["mobile-fablet", "mobile-tablet", "mobile-desktop"]
  - var media_direction = ["landscape", "portrait"]
  .group.is-scroll-x
    table.table.is-sm.is-center.is-nowrap.is-middle.is-border
      thead
        tr.box.is-paint
          th(width="80")
          th
            p
              i.fa.fa-mobile(aria-hidden="true")
              span.text Mobile
              br
              span.text.is-sm all
          th
            p
              i.fa.fa-mobile(aria-hidden="true")
              span.text Fablet
              br
              span.text.is-sm 576px ~
          th
            p
              i.fa.fa-tablet(aria-hidden="true")
              span.text Tablet
              br
              span.text.is-sm 768px ~
          th
            p
              i.fa.fa-desktop(aria-hidden="true")
              span.text Desktop
              br
              span.text.is-sm 992px ~
          th
            p
              i.fa.fa-desktop(aria-hidden="true")
              span.text Wide
              br
              span.text.is-sm 1200px ~
      tbody
        tr(v-if="split")
          td
            p.text.is-sm
              | 範囲を12分割して
              br
              | 比率を指定
          each val in media_first
            td
              p
                span.text= ".is-" + val + "-1"
                br
                span.text |
                br
                span.text= ".is-" + val + "-12"
        tr
          td
            p.text.is-sm
              | 余白を埋め等分
          each val in media_first
            td
              p
                span.text= ".is-" + val + "-0"
        tr
          td
            p.text.is-sm
              | 100%に広がる
          each val in media_first
            td
              p
                span.text= ".is-" + val + "-full"
        tr
          td
            p.text.is-sm
              | 元のサイズを保持
          each val in media_first
            td
              p
                span.text= ".is-" + val + "-auto"
  .group.is-scroll-x
    table.table.is-sm.is-center.is-nowrap.is-middle.is-border
      thead
        tr.box.is-paint
          th(width="80")
          th
            p
              i.fa.fa-mobile(aria-hidden="true")
              span.text Mobile Only
              br
              span.text.is-sm ~ 575px
          th
            p
              i.fa.fa-mobile(aria-hidden="true")
              span.text Fablet Only
              br
              span.text.is-sm 576px ~ 767px
          th
            p
              i.fa.fa-tablet(aria-hidden="true")
              span.text Tablet Only
              br
              span.text.is-sm 768px ~ 991px
          th
            p
              i.fa.fa-desktop(aria-hidden="true")
              span.text Desktop Only
              br
              span.text.is-sm 992px ~ 1199px
      tbody
        tr(v-if="split")
          td
            p.text.is-sm
              | 範囲を12分割して
              br
              | 比率を指定
          each val in media_only
            td
              p
                span.text= ".is-" + val + "-1"
                br
                span.text |
                br
                span.text= ".is-" + val + "-12"
        tr
          td
            p.text.is-sm
              | 余白を埋め等分
          each val in media_only
            td
              p
                span.text= ".is-" + val + "-0"
        tr
          td
            p.text.is-sm
              | 100%に広がる
          each val in media_only
            td
              p
                span.text= ".is-" + val + "-full"
        tr
          td
            p.text.is-sm
              | 元のサイズを保持
          each val in media_only
            td
              p
                span.text= ".is-" + val + "-auto"
  .group.is-scroll-x
    table.table.is-sm.is-center.is-nowrap.is-middle.is-border
      thead
        tr.box.is-paint
          th(width="80")
          th
            p
              i.fa.fa-mobile.is-fit(aria-hidden="true")
              i.fa.fa-mobile.is-fit(aria-hidden="true")
              span.text Mobile ~ Fablet
              br
              span.text.is-sm ~ 767px
          th
            p
              i.fa.fa-mobile.is-fit(aria-hidden="true")
              i.fa.fa-tablet.is-fit(aria-hidden="true")
              span.text Mobile ~ Tablet
              br
              span.text.is-sm ~ 991px
          th
            p
              i.fa.fa-mobile.is-fit(aria-hidden="true")
              i.fa.fa-desktop.is-fit(aria-hidden="true")
              span.text Mobile ~ Desktop
              br
              span.text.is-sm ~ 1199px
      tbody
        tr(v-if="split")
          td
            p.text.is-sm
              | 範囲を12分割して
              br
              | 比率を指定
          each val in media_range
            td
              p
                span.text= ".is-" + val + "-1"
                br
                span.text |
                br
                span.text= ".is-" + val + "-12"
        tr
          td
            p.text.is-sm
              | 余白を埋め等分
          each val in media_range
            td
              p
                span.text= ".is-" + val + "-0"
        tr
          td
            p.text.is-sm
              | 100%に広がる
          each val in media_range
            td
              p
                span.text= ".is-" + val + "-full"
        tr
          td
            p.text.is-sm
              | 元のサイズを保持
          each val in media_range
            td
              p
                span.text= ".is-" + val + "-auto"
  .group.is-scroll-x
    table.table.is-sm.is-center.is-nowrap.is-middle.is-border
      thead
        tr.box.is-paint
          th(width="80")
          th
            p
              i.fa.fa-mobile.fa-rotate-270(aria-hidden="true")
              span.text Landscape
              br
              span.text.is-sm landscape & ~ 991px
          th
            p
              i.fa.fa-mobile(aria-hidden="true")
              span.text Portrait
              br
              span.text.is-sm portrait & ~ 991px
      tbody
        tr(v-if="split")
          td
            p.text.is-sm
              | 範囲を12分割して
              br
              | 比率を指定
          each val in media_direction
            td
              p
                span.text= ".is-" + val + "-1"
                br
                span.text |
                br
                span.text= ".is-" + val + "-12"
        tr
          td
            p.text.is-sm
              | 余白を埋め等分
          each val in media_direction
            td
              p
                span.text= ".is-" + val + "-0"
        tr
          td
            p.text.is-sm
              | 100%に広がる
          each val in media_direction
            td
              p
                span.text= ".is-" + val + "-full"
        tr
          td
            p.text.is-sm
              | 元のサイズを保持
          each val in media_direction
            td
              p
                span.text= ".is-" + val + "-auto"
</template>

<script>
export default {
  props: {
    split: {
      type: Boolean,
      default: false
    }
  }
};
</script>
