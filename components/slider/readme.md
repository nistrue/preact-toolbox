# Slider

[Sliders](https://www.google.com/design/spec/components/sliders.html#) let users select a value from a continuous or discrete range of values by moving the slider thumb. The smallest value is to the left, the largest to the right. Sliders can have icons to the left and right of the bar that reflect the value intensity. The interactive nature of the slider makes it a great choice for settings that reflect intensity levels, such as volume, brightness, or color saturation.

<!-- example -->
```jsx
import Slider from 'react-toolbox/slider';

const SliderTest = () => (
  <section>
    <p>Default slider</p>
    <Slider />
    <p>With steps, initial value and editable</p>
    <Slider value={5} min={0} max={10} editable />
    <p>Pinned and with snaps</p>
    <Slider pinned snaps value={1} min={0} max={10} step={1} editable />
  </section>
);
```

## Properties

| Name          | Type    | Default   | Description|
|:-----|:-----|:-----|:-----|
| `className` | `String`  | `''`      | Additional class name to provide custom styling.|
| `editable`  | `Boolean` | `false`   | If true, an input is shown and the user can set the slider from keyboard value.|
| `max`       | `Number`  | `100`     | Maximum value permitted.|
| `min`       | `Number`  | `0`       | Minimum value permitted.|
| `pinned`    | `Boolean` | `false`   | If true, a pin with numeric value label is shown when the slider thumb is pressed. Use for settings for which users need to know the exact value of the setting.|
| `snaps`     | `Boolean` | `false` | If true, the slider thumb snaps to tick marks evenly spaced based on the step property value.|
| `step`      | `Number`  | `0.01`    | Amount to vary the value when the knob is moved or increase/decrease is called.|
| `value`     | `Number`  | `0`       | Value of the current value.|

## Methods

Since the slider is able to keep a value it needs state and exposes methods to retrieve and set the current value as usual.

- `getValue` is used to retrieve the current value.
- `setValue` to force a new value.
