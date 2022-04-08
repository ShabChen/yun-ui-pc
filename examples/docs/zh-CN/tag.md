## Tag 标签

用于标记和选择。

### 无操作标签

#### 样式

样式有主要、主次、次要3种，根据场景使用

使用`type`属性来选择 tag 的样式，可选值: light (默认)、dark、 plain。`dark`类型只在配置了`theme`之后生效。

:::demo
```html
<div class="tag-group">
  <y-tag>主次标签</y-tag>
  <y-tag type="plain">次要标签</y-tag>
  <y-tag type="dark" theme="blue">主要标签</y-tag>
  <y-tag theme="blue">主次标签</y-tag>
  <y-tag type="plain" theme="blue">次要标签</y-tag>
</div>
```
:::

#### 尺寸

标签尺寸：分为默认尺寸、小尺寸、迷你尺寸，标签的边距固定，标签宽度随文字宽度增大而增大。

使用`size`属性设置 tag 尺寸大小：默认尺寸、small 和 mini。

:::demo 
```html
<div class="tag-group">
  <y-tag >主次标签</y-tag>
  <y-tag size="small">主次标签</y-tag>
  <y-tag size="mini">主次标签</y-tag>

  <y-tag type="plain">次要标签</y-tag>
  <y-tag type="plain" size="small">次要标签</y-tag>
  <y-tag type="plain" size="mini">次要标签</y-tag>
</div>
<div class="tag-group">
  <y-tag theme="blue" type="dark">主要标签</y-tag>
  <y-tag theme="blue" type="dark" size="small">主要标签</y-tag>
  <y-tag theme="blue" type="dark" size="mini">主要标签</y-tag>

  <y-tag theme="blue">主次标签</y-tag>
  <y-tag theme="blue" size="small">主次标签</y-tag>
  <y-tag theme="blue" size="mini">主次标签</y-tag>

  <y-tag theme="blue" type="plain">次要标签</y-tag>
  <y-tag theme="blue" type="plain" size="small">次要标签</y-tag>
  <y-tag theme="blue" type="plain" size="mini">次要标签</y-tag>
</div>
```
:::
### 图标

使用`icon`属性选择图标

:::demo 
```html
<div class="tag-group">
  <y-tag icon="expression" >主次标签</y-tag>
  <y-tag icon="expression" size="small">主次标签</y-tag>
  <y-tag icon="expression" size="mini">主次标签</y-tag>

  <y-tag icon="expression" type="plain" >次要标签</y-tag>
  <y-tag icon="expression" type="plain" size="small">次要标签</y-tag>
  <y-tag icon="expression" type="plain" size="mini">次要标签</y-tag>
</div>
<div class="tag-group">
  <y-tag theme="blue" type="dark" icon="expression" >主要标签</y-tag>
  <y-tag theme="blue" type="dark" icon="expression" size="small">主要标签</y-tag>
  <y-tag theme="blue" type="dark" icon="expression" size="mini">主要标签</y-tag>
  
  <y-tag theme="blue" icon="expression" >主次标签</y-tag>
  <y-tag theme="blue" icon="expression" size="small">主次标签</y-tag>
  <y-tag theme="blue" icon="expression" size="mini">主次标签</y-tag>

  <y-tag theme="blue" icon="expression" type="plain" >次要标签</y-tag>
  <y-tag theme="blue" icon="expression" type="plain" size="small">次要标签</y-tag>
  <y-tag theme="blue" icon="expression" type="plain" size="mini">次要标签</y-tag>
</div>
```
:::
### 图片

使用`avatar`属性来自定义图片。

:::demo
```html
<div class="tag-group">
  <y-tag avatar="../../../yui_logo.svg" >主次标签</y-tag>
  <y-tag avatar="../../../yui_logo.svg" size="small">主次标签</y-tag>
  <y-tag avatar="../../../yui_logo.svg" size="mini">主次标签</y-tag>

  <y-tag avatar="../../../yui_logo.svg" type="plain">次要标签</y-tag>
  <y-tag avatar="../../../yui_logo.svg" type="plain" size="small">次要标签</y-tag>
  <y-tag avatar="../../../yui_logo.svg" type="plain" size="mini">次要标签</y-tag>
</div>
<div class="tag-group">
  <y-tag theme="blue" type="dark" avatar="../../../yui_logo.svg" >主要标签</y-tag>
  <y-tag theme="blue" type="dark" avatar="../../../yui_logo.svg" size="small">主要标签</y-tag>
  <y-tag theme="blue" type="dark" avatar="../../../yui_logo.svg" size="mini">主要标签</y-tag>

  <y-tag theme="blue" avatar="../../../yui_logo.svg" >主次标签</y-tag>
  <y-tag theme="blue" avatar="../../../yui_logo.svg" size="small">主次标签</y-tag>
  <y-tag theme="blue" avatar="../../../yui_logo.svg" size="mini">主次标签</y-tag>

  <y-tag theme="blue" avatar="../../../yui_logo.svg" type="plain">次要标签</y-tag>
  <y-tag theme="blue" avatar="../../../yui_logo.svg" type="plain" size="small">次要标签</y-tag>
  <y-tag theme="blue" avatar="../../../yui_logo.svg" type="plain" size="mini">次要标签</y-tag>
</div>
```
:::

### 可移除标签

:::demo 设置`closable`属性可以定义一个标签是否可移除。默认的标签移除时会附带渐变动画，如果不想使用，可以设置`disable-transitions`属性，它接受一个`Boolean`，true 为关闭。

```html
<div class="tag-group">
  <y-tag closable>默认标签</y-tag>
  <y-tag closable size="small">小型标签</y-tag>
  <y-tag closable size="mini">迷你标签</y-tag>
  <y-tag icon="expression" closable>默认标签</y-tag>
  <y-tag icon="expression" closable size="small">小型标签</y-tag>
  <y-tag icon="expression" closable size="mini">标签一</y-tag>
</div>
<div class="tag-group">
  <y-tag theme="blue" closable>默认标签</y-tag>
  <y-tag theme="blue" closable size="small">小型标签</y-tag>
  <y-tag theme="blue" closable size="mini">迷你标签</y-tag>
  <y-tag theme="blue" icon="expression" closable>默认标签</y-tag>
  <y-tag theme="blue" icon="expression" closable size="small">小型标签</y-tag>
  <y-tag theme="blue" icon="expression" closable size="mini">迷你标签</y-tag>
</div>
```
:::

### 动态编辑标签

动态编辑标签可以通过点击标签关闭按钮后触发的 `close` 事件来实现

:::demo
```html
<y-tag
  :key="tag"
  v-for="tag in dynamicTags"
  closable
  theme="blue"
  :disable-transitions="false"
  @close="handleClose(tag)">
  <img class="y-tag__avatar" src="../../../yui_logo.svg"></img>
  {{tag}}
</y-tag>
<y-input
  class="input-new-tag"
  v-if="inputVisible"
  v-model="inputValue"
  ref="saveTagInput"
  size="small"
  @keyup.enter.native="handleInputConfirm"
  @blur="handleInputConfirm"
>
</y-input>
<y-button v-else class="button-new-tag" size="small" @click="showInput">+ New Tag</y-button>

<style>
  .y-tag + .y-tag {
    margin-left: 10px;
  }
  .button-new-tag {
    margin-left: 10px;
    height: 34px;
    line-height: 32px;
    padding-top: 0;
    padding-bottom: 0;
  }
  .input-new-tag {
    width: 90px;
    margin-left: 10px;
    vertical-align: bottom;
  }
</style>

<script>
  export default {
    data() {
      return {
        dynamicTags: ['标签一', '标签二', '标签三'],
        inputVisible: false,
        inputValue: ''
      };
    },
    methods: {
      handleClose(tag) {
        this.dynamicTags.splice(this.dynamicTags.indexOf(tag), 1);
      },

      showInput() {
        this.inputVisible = true;
        this.$nextTick(_ => {
          this.$refs.saveTagInput.$refs.input.focus();
        });
      },

      handleInputConfirm() {
        let inputValue = this.inputValue;
        if (inputValue) {
          this.dynamicTags.push(inputValue);
        }
        this.inputVisible = false;
        this.inputValue = '';
      }
    }
  }
</script>
```
:::

### 可选中标签

设置`selectable`属性可以定义一个标签是否可选中。（点击标签可查看选中效果）

:::demo
```html
<div class="tag-group">
  <y-tag @select="handleSelect" selectable>次要标签</y-tag>
  <y-tag @select="handleSelect" icon="expression" selectable>次要标签</y-tag>
  <y-tag @select="handleSelect" type="plain" selectable>次要标签</y-tag>
  <y-tag @select="handleSelect" icon="expression" type="plain" selectable>次要标签</y-tag>
  <y-tag @select="handleSelect" theme="blue" selectable>主要标签</y-tag>
  <y-tag theme="blue" icon="expression" selectable @select="handleSelect">主要标签</y-tag>
</div>
<script>
  export default {
    methods: {
      handleSelect(status) {
        console.log(status ? '选中' : '取消选中')
      }
    }
  }
</script>
```
:::

### 不同主题

Tag 组件提供了三个不同的主题：`dark`、`light` 和 `plain`

:::demo 通过设置`effect`属性来改变主题，默认为 `light`
```html
<div class="tag-group">
  <span class="tag-group__title">Dark</span>
  <y-tag
    v-for="item in items"
    :key="item.label"
    effect="dark">
    {{ item.label }}
  </y-tag>
</div>
<div class="tag-group">
  <span class="tag-group__title">Plain</span>
  <y-tag
    v-for="item in items"
    :key="item.label"
    effect="plain">
    {{ item.label }}
  </y-tag>
</div>

<script>
  export default {
    data() {
      return {
        items: [
          { type: '', label: '标签一' },
          { type: 'success', label: '标签二' },
          { type: 'info', label: '标签三' },
          { type: 'danger', label: '标签四' },
          { type: 'warning', label: '标签五' }
        ]
      }
    }
  }
</script>
```
:::

### Attributes
| 参数      | 说明          | 类型      | 可选值                           | 默认值  |
|---------- |-------------- |---------- |--------------------------------  |-------- |
| type | 类型 | string | success/info/warning/danger | — |
| closable | 是否可关闭 | boolean | — | false |
| disable-transitions | 是否禁用渐变动画 | boolean | — | false |
| hit | 是否有边框描边 | boolean | — | false |
| color | 背景色 | string | — | — |
| size | 尺寸 | string | medium / small / mini | — |
| effect | 主题 | string | dark / light / plain | light |


### Events
| 事件名称 | 说明 | 回调参数 |
|---------- |-------- |---------- |
| click | 点击 Tag 时触发的事件 | — |
| close | 关闭 Tag 时触发的事件 | — |
