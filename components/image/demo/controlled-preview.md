---
order: 7
title:
  zh-CN: 受控的预览
  en-US: Controlled Preview
---

## zh-CN

可以使预览受控。

## en-US

You can make preview controlled.

```tsx
import { Button, InputNumber, Image } from 'antd';
import React, { useState } from 'react';

const App: React.FC = () => {
  const [visible, setVisible] = useState(false);
  const [scaleStep, setScaleStep] = useState(0.5);

  return (
    <>
      <div>
        scaleStep:{' '}
        <InputNumber
          min={0.1}
          max={5}
          defaultValue={0.5}
          step={0.1}
          onChange={val => setScaleStep(val)}
        />
      </div>
      <br />
      <Button type="primary" onClick={() => setVisible(true)}>
        show image preview
      </Button>
      <Image
        width={200}
        style={{ display: 'none' }}
        src="https://zos.alipayobjects.com/rmsportal/jkjgkEfvpUPVyRjUImniVslZfWPnJuuZ.png?x-oss-process=image/blur,r_50,s_50/quality,q_1/resize,m_mfit,h_200,w_200"
        preview={{
          visible,
          scaleStep,
          src: 'https://zos.alipayobjects.com/rmsportal/jkjgkEfvpUPVyRjUImniVslZfWPnJuuZ.png',
          onVisibleChange: value => {
            setVisible(value);
          },
        }}
      />
    </>
  );
};

export default App;
```
