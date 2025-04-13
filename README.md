# React Spin 3D Carousel 🎠

![Carousel Demo](https:example.com/demo.gif) _Replace with your actual demo GIF_

A highly customizable 3D spinning carousel component for React with smooth animations and multiple display modes. Perfect for showcasing portfolios, products, or image galleries.

## 📦 Installation

```bash
npm install @carousel-ui/react-spin-carousel-3d
# or
yarn add @carousel-ui/react-spin-carousel-3d
```

## 🌟 Features

- **3D Perspective Effects** - Realistic card rotation and depth
- **Dual Display Modes** - `card` (with shadows/borders) and `image` (seamless) modes
- **Responsive Design** - Works on all screen sizes
- **Touch & Drag Support** - Mobile-friendly interactions
- **Auto-play** - Optional automatic rotation
- **Customizable Navigation** - Built-in radio buttons or bring your own
- **TypeScript Support** - Fully typed components
- **Performance Optimized** - Smooth animations with CSS transforms

## Usage

## 🚀 Usage Examples

### Basic Card Carousel

```tsx

<!-- Importing -->
import ReactSpinCarousel3D from "@carousel-ui/react-spin-carousel-3d";
// import imagePlaceHolder from "path-to-your-local-file";

<!-- Your Data -->
const DATA: string[] = [
  "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1493136289900-28660d718589.avif",
  "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1552663651-2e4250e6c7c8.avif",
  "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1656019674844-3040aba0350b.avif",
  "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1661695423331-817b8aadd1a0.avif",
  "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/premium_photo-1668485968590-aff3717c1dbe.avif",
  "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/premium_photo-1688497831136-0b76172b0f5f.avif",
  // imagePlaceHolder,
];

<!-- Usage -->
<ReactSpinCarousel3D<string>
  key="carouse-one"
  data={DATA}
  renderItem={(item, index) => (
    <img src={item} alt={`image ${index}`} />
  )}
  accentColor="blue"
  backgroundColor="#F5F5F5"
  isAutoPlay={true}
  initialActiveIndex={0}
  autoPlayInterval={5000}
  showRadioButtons={true}
  displayMode="image"
/>
```

### Image Gallery

```tsx

```

### Custom Navigation

```tsx

```

### Using Multiple Carousels together

```tsx

```

## 🛠 Props Reference

### Core Props

| Prop         | Type                                          | Default      | Description                   |
| ------------ | --------------------------------------------- | ------------ | ----------------------------- |
| `data`       | `T[]`                                         | **Required** | Array of items to render      |
| `renderItem` | `(item: T, index: number) => React.ReactNode` | **Required** | Render function for each item |

### Layout & Styling

| Prop              | Type                  | Default               | Description                          |
| ----------------- | --------------------- | --------------------- | ------------------------------------ |
| `width`           | `string \| number`    | `"100%"`              | Container width (`"500px"` or `500`) |
| `height`          | `string \| number`    | `300`                 | Container height                     |
| `itemWidth`       | `string \| number`    | `300`                 | Individual item width                |
| `accentColor`     | `string`              | `"hsl(204, 5%, 38%)"` | Active state color                   |
| `backgroundColor` | `string`              | `"#F5F5F5"`           | Card background color                |
| `containerStyle`  | `React.CSSProperties` | `{}`                  | Custom container styles              |
| `itemStyle`       | `React.CSSProperties` | `{}`                  | Custom item styles                   |

### Behavior

| Prop                 | Type                               | Default       | Description                  |
| -------------------- | ---------------------------------- | ------------- | ---------------------------- |
| `isCentered`         | `boolean`                          | `true`        | Center carousel horizontally |
| `initialActiveIndex` | `number`                           | `middle item` | Starting active index        |
| `isAutoPlay`         | `boolean`                          | `false`       | Enable auto-rotation         |
| `autoPlayInterval`   | `number`                           | `5000`        | Rotation interval in ms      |
| `onItemClick`        | `(item: T, index: number) => void` | -             | Item click handler           |

### Display Mode

| Prop              | Type                             | Default    | Description                            |
| ----------------- | -------------------------------- | ---------- | -------------------------------------- |
| `displayMode`     | `"image" \| "card"`              | `"card"`   | Visual presentation style              |
| `imageFit`\*      | `"cover" \| "contain" \| "fill"` | `"cover"`  | Image scaling behavior                 |
| `imagePosition`\* | `string`                         | `"center"` | Image positioning (e.g., `"top left"`) |

\*Only applies when `displayMode="image"`

### Navigation Controls

| Prop                 | Type                  | Default | Description                  |
| -------------------- | --------------------- | ------- | ---------------------------- |
| `showRadioButtons`   | `boolean`             | `true`  | Show default navigation dots |
| `customRadioButtons` | Function              | -       | Custom navigation renderer   |
| `radioButtonStyle`   | `React.CSSProperties` | `{}`    | Style for default dots       |

## 🎨 Styling Tips

1.  **For Cards**:

    - Use `backgroundColor` to set card color
    - Add custom shadows via `itemStyle`

    ```tsx
    itemStyle={{
      boxShadow: "0 10px 20px rgba(0,0,0,0.2)",
      borderRadius: "12px"
    }}
    ```

2.  **For Images**:
    - Set `imageFit="contain"` for full image visibility
    - Use `imagePosition="top"` for portrait images

## ⚠️ Troubleshooting

**Issue**: Horizontal scroll appears  
 **Fix**: Ensure parent container has `overflow-x: hidden`

**Issue**: Items overlapping  
 **Fix**: Increase `itemWidth` or reduce number of items

**Issue**: Auto-play stops on hover  
 **Solution**: This is intentional (UX best practice). Lets the user observe whats inside the card.

## 📜 License

MIT © @carousel-ui
