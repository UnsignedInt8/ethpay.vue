<template>
  <button class="__ethpay_button">
    <svg width="20px" height="20px" viewBox="0 0 20 20" version="1.1">
      <g id="icon/coin/eth" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
        <g id="ethereum-1" transform="translate(4.301209, 0.000000)" fill-rule="nonzero">
          <polygon
            id="Path"
            fill="#343434"
            points="6.13812922 0 6.00405656 0.455703125 6.00405656 13.6791525 6.13812922 13.8129853 12.2763064 10.184725"
          />
          <polygon
            id="Path"
            fill="#8C8C8C"
            points="6.13817719 0 0 10.184725 6.13817719 13.8130333 6.13817719 7.39476656"
          />
          <polygon
            id="Path"
            fill="#3C3C3B"
            points="6.13812922 14.9752202 6.06257844 15.0673202 6.06257844 19.7778034 6.13812922 19.9984597 12.28 11.3487827"
          />
          <polygon
            id="Path"
            fill="#8C8C8C"
            points="6.13817719 19.9984117 6.13817719 14.9751242 0 11.3486867"
          />
          <polygon
            id="Path"
            fill="#141414"
            points="6.13812922 13.8129853 12.2762105 10.184773 6.13812922 7.39481453"
          />
          <polygon
            id="Path"
            fill="#393939"
            points="0 10.184725 6.13808125 13.8129853 6.13808125 7.39476656"
          />
        </g>
      </g>
    </svg>
    <span>Pay</span>
  </button>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class PayButton extends Vue {
  @Prop() caption?: string;
}
</script>

<style lang="scss" scoped>
.__ethpay_button {
  height: 36px;
  min-width: 108px;
  border: 1px solid black;
  border-radius: 5px;
  padding: 0 24px;
  background: none;
  cursor: pointer;
  display: flex;
  justify-content: center;
  align-items: center;
  font-family: "PingFang SC", -apple-system, BlinkMacSystemFont, "Segoe UI", "Roboto", "Oxygen", "Ubuntu", "Cantarell",
    "Fira Sans", "Droid Sans", "Helvetica Neue", sans-serif;
  transition: all 0.5s;

  .caption {
    font-weight: 600;
    font-size: 15px;
    margin-right: 4px;
  }

  .value {
    font-size: 16px;
    margin-right: 2px;
  }

  $icon-height: 20px;
  .icon {
    height: $icon-height;
    width: $icon-height;
    display: inline-block;
    margin: 0 3px;

    svg {
      height: $icon-height;

      .__ethpay_symbol,
      circle,
      polygon,
      path {
        transition: all 0.3s;
      }
    }
  }

  span {
    display: inline-block;
    font-weight: 600;
    font-size: 18px;
  }
}

.__ethpay_button:hover {
  opacity: 0.6;
}

.__ethpay_button:active,
.__ethpay_button.black {
  color: white !important;
  background: black;
  border-color: black !important;

  span {
    color: white !important;
  }

  svg {
    circle,
    polygon,
    path {
      fill: white !important;
    }

    .__ethpay_symbol {
      fill: black !important;
    }
  }
}

.__ethpay_button:disabled {
  cursor: not-allowed;
  color: #aaa !important;
  border-color: #aaa !important;
  opacity: 1 !important;

  svg {
    filter: grayscale(100%);

    circle,
    polygon,
    path {
      filter: grayscale(100%);
    }

    .__ethpay_symbol {
      filter: grayscale(100%);
    }
  }
}

.__ethpay_tooltip {
  font-size: 12px;
}

</style>