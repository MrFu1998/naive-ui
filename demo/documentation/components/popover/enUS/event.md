# Event
```html
<n-popover
  placement="bottom"
  :width="200"
  trigger="hover"
  style="margin-right: 12px;"
  @show="handleShow"
  @hide="handleHide"
>
  <template v-slot:activator>
    <n-button>
      California Girls(Hover)
    </n-button>
  </template>
  <span>
    I wish they all could be California girls
  </span>
</n-popover>
<n-popover
  placement="bottom"
  :width="200"
  trigger="click"
  style="margin-right: 12px;"
  @show="handleShow"
  @hide="handleHide"
>
  <template v-slot:activator>
    <n-button>
      California Girls(Click)
    </n-button>
  </template>
  <span>
    I wish they all could be California girls
  </span>
</n-popover>
<n-popover
  v-model="showPopover"
  placement="bottom"
  :width="200"
  trigger="manual"
  @show="handleShow"
  @hide="handleHide"
>
  <template v-slot:activator>
    <n-button @click="showPopover = !showPopover">
      California Girls(Manual)
    </n-button>
  </template>
  <span>
    I wish they all could be California girls
  </span>
</n-popover>
```

```js
export default {
  data() {
    return {
      showPopover: false
    };
  },
  methods: {
    handleShow() {
      this.$NMessage.success("show popover");
    },
    handleHide() {
      this.$NMessage.success("hide popover");
    }
  }
};
```

```css
.n-button {
  margin: 0 12px 8px 0;
}
```