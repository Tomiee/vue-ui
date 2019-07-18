<template>
  <div>
    <button class="button" :class="{[`icon-${iconPosition}`]:true}">
      <u-icon class="icon" v-if="icon && !loading" :name="icon"></u-icon>
      <u-icon class="icon loading" v-if="loading" :name="loading"></u-icon>
      <div class="u-button-content">
        <slot></slot>
      </div>
    </button>
  </div>
</template>


<script>
import Icon from "../../icon";

export default {
  name: "Button",
  components: {
    "u-icon": Icon
  },
  props: {
    icon: {},
    loading: {
      type: Boolean,
      default: false
    },
    iconPosition: {
      type: String,
      default: "left",
      validator(value) {
        return value === "left" || value === "right";
      }
    }
  }
};
</script>

<style lang="scss" scoped>

div {
  --button-height: 32px;
  --font-size: 14px;
  --button-bg: white;
  --button-active-bg: #eee;
  --button-radius: 4px;
  --color: #333;
  --border-color: #999;
  --border-color-hover: #666;
}

.button {
  font-size: var(--font-size);
  height: var(--button-height);
  background: var(--button-bg);
  padding: 0 1em;
  display: inline-flex;
  justify-content: center;
  align-items: center;
  border-radius: var(--button-radius);
  outline: none;
  &:hover {
    border-color: var(--border-color-hover);
  }
  &:active {
    background-color: var(--button-active-bg);
  }
  &:fouse {
    outline: none;
  }
  > .u-button-content {
    order: 2;
  }
  > .icon {
    order: 1;
    margin-right: 0.1em;
  }

  &.icon-right {
    > .u-button-content {
      order: 1;
    }
    > .icon {
      order: 2;
      margin-right: 0;
      margin-left: 0.1em;
    }
  }
}
</style>



