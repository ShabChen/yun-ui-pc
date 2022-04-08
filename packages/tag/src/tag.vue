<script>
  export default {
    name: 'YTag',
    props: {
      // 图片
      avatar: String,
      // 图标
      icon: String,
      // 内容
      text: String,
      // 是否可移除, false (默认) / true
      closable: Boolean,
      // 是否可选中, false (默认) / true
      selectable: Boolean,
      // 样式: 主要 primary  / 主次 secondary  / 次要 info
      type: {
        type: String,
        default: 'light',
        validator(val) {
          return ['dark', 'light', 'plain'].indexOf(val) !== -1;
        }
      },
      // 主题色
      theme: String,
      hit: Boolean,
      disableTransitions: Boolean,
      // 背景颜色
      color: String,
      // 尺寸: 默认尺寸 / small / mini
      size: String
    },
    data() {
      return {
        selected: false
      };
    },
    methods: {
      handleClose(event) {
        event.stopPropagation();
        this.$emit('close', event);
      },
      handleClick(event) {
        this.$emit('click', event);
        if (this.selectable) {
          this.selected = !this.selected;
          this.$emit('select', this.selected);
        };
      }
    },
    computed: {
      tagSize() {
        return this.size || (this.$YUN || {}).size;
      }
    },
    render(h) {
      const { icon, type, theme, closable, selectable, selected, tagSize, hit } = this;
      const classes = [
        'y-tag',
        !closable && type ? `y-tag--${type}` : '',
        theme ? `y-tag--${theme}` : '',
        tagSize ? `y-tag--${tagSize}` : '',
        hit && 'is-hit',
        closable && 'y-tag--plain y-tag--closable',
        selectable && 'y-tag--selectable',
        selected && 'selected'
      ];
      const iconClasses = [
        'y-tag__icon',
        `y-icon-${icon}`
      ];
      const tagEl = (
        <span
          class={ classes }
          style={{ backgroundColor: this.color }}
          on-click={ this.handleClick }>
          { this.avatar && <img class="y-tag__avatar" src={ this.avatar }></img>}
          { icon && <i class={ iconClasses } name={ icon }></i> }
          { this.$slots.default }
          {
            closable && <i class="y-tag__close y-icon-close" on-click={ this.handleClose }></i>
          }
        </span>
      );

      return this.disableTransitions ? tagEl : <transition name="y-zoom-in-center">{ tagEl }</transition>;
    }
  };
</script>
