---
category: Components
subtitle: 图片
type: 数据展示
title: Image
cols: 2
cover: https://gw.alipayobjects.com/zos/antfincdn/D1dXz9PZqa/image.svg
---

可预览的图片。

## 何时使用

- 需要展示图片时使用。
- 加载大图时显示 loading 或加载失败时容错处理。

## API

| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| alt | 图像描述 | string | - | 4.6.0 |
| fallback | 加载失败容错地址 | string | - | 4.6.0 |
| height | 图像高度 | string \| number | - | 4.6.0 |
| placeholder | 加载占位, 为 `true` 时使用默认占位 | ReactNode | - | 4.6.0 |
| preview | 预览参数，为 `false` 时禁用 | boolean \| [previewType](#previewType) | true | 4.6.0 [previewType](#previewType):4.7.0 |
| src | 图片地址 | string | - | 4.6.0 |
| width | 图像宽度 | string \| number | - | 4.6.0 |
| onError | 加载错误回调 | (event: Event) => void | - | 4.12.0 |
| rootClassName | 为展示图片根 DOM 和预览大图根 DOM 提供自定义 className | string | - | 4.20.0 |

### previewType

```js
{
  visible?: boolean;
  onVisibleChange?: (visible, prevVisible) => void;
  getContainer?: string | HTMLElement | (() => HTMLElement); // v4.8.0
  src?: string; // v4.10.0
  mask?: ReactNode; // v4.9.0
  maskClassName?: string; // v4.11.0
  current?: number; // v4.12.0 仅支持 PreviewGroup
  countRender?: (current: number, total: number) => string  // v4.20.0 仅支持 PreviewGroup
  scaleStep?: number;
}
```

其他属性见 [&lt;img>](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img#Attributes)
