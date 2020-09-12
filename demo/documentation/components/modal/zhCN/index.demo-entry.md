# 模态框 Modal
它会弹出来，然后给你看点东西。

## 演示
```demo
basic
controlled
mask-closable
preset-card
preset-confirm
preset-confirm-slot
dark-1-debug
dark-2-debug
dark-3-debug
dark-4-debug
drawer-debug
```
## V-model
|Prop|Event|
|-|-|
|show|hide|

## Props
### Modal
|名称|类型|默认值|说明|
|-|-|-|-|
|theme|`'light' \| 'dark' \| null \| string`|`null`||
|show|`boolean`|`false`||
|mask-closable|`boolean`|`true`|点击遮罩时是否发出 `hide` 事件|
|preset|`'card' \| 'confirm'`|`null`||
|overlay-style|`Object`|`null`|当使用 `preset` 时候内部内容的样式|

### Modal（Card 预设）
参考 [Card props](n-card#Props)
### Modal（Confirm 预设）
参考 [Confirm props](n-confirm#Props)

## Slots
### Modal（无预设）
|名称|参数|说明|
|-|-|-|
|default|`()`||

### Modal（Card 预设）
参考 [Card slots](n-card#Slots)
### Modal（Confirm 预设）
参考 [Confirm slots](n-confirm#Slots)

## Events
### Modal
|名称|参数|说明|
|-|-|-|
|hide|`(show: false)`||

### Modal（Card 预设）
参考 [Card events](n-card#Events)
### Modal（Confirm 预设）
参考 [Confirm events](n-confirm#Events)