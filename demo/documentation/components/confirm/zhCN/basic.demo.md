# 基础用法
使用 `$NConfirm` 来创建一个确认弹框。
```html
<n-button @click="handleConfirm">
  警告
</n-button>
<n-button @click="handleSuccess">
  成功
</n-button>
<n-button @click="handleError">
  错误
</n-button>
```
```css
.n-button {
  margin: 0 12px 8px 0;
}
```
```js
export default {
  methods: {
    handleConfirm (e) {
      const confirmInstance = this.$NConfirm.warning({
        title: '警告',
        content: '你确定？',
        positiveText: '确定',
        negativeText: '不确定',
        onPositiveClick: () => {
          this.$NMessage.success('确定')
        },
        onNegativeClick: () => {
          this.$NMessage.error('不确定')
        }
      })
    },
    handleSuccess (e) {
      const confirmInstance = this.$NConfirm.success({
        title: '成功',
        content:
          '厉害',
        positiveText: '哇',
        onPositiveClick: () => {
          this.$NMessage.success('耶！')
        }
      })
    },
    handleError(e) {
      const confirmInstance = this.$NConfirm.error({
        title: '错误',
        content: '错了',
        positiveText: '啊',
        onPositiveClick: () => {
          this.$NMessage.success('我就知道')
        }
      })
    }
  }
}
```