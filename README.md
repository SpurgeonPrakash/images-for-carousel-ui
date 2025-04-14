# React Spin Carousel 3D 🎠

![Carousel Demo](https:example.com/demo.gif) _Replace with your actual demo GIF_

The **React Spin Carousel 3D** is a highly customizable 3D carousel component for React. It allows you to display a collection of items in a visually appealing 3D carousel with smooth transitions and interactive controls. The component supports auto-play, custom radio buttons, smooth animations and multiple display modes("card", "image"). Perfect for showcasing portfolios, products, or image galleries and many more :).

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

### Typescript

### Image Gallery (displayMode: "image")

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

#### Entire React Component in Typescript of Image Gallery

```tsx
import ReactSpinCarousel3D from "@carousel-ui/react-spin-carousel-3d";

// import imagePlaceHolder from "path-to-your-local-file";

const DATA: string[] = [
  "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1493136289900-28660d718589.avif",
  "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1552663651-2e4250e6c7c8.avif",
  "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1656019674844-3040aba0350b.avif",
  "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1661695423331-817b8aadd1a0.avif",
  "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/premium_photo-1668485968590-aff3717c1dbe.avif",
  "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/premium_photo-1688497831136-0b76172b0f5f.avif",
  // imagePlaceHolder,
];

const YourComponent = () => {
  return (
    <ReactSpinCarousel3D<string>
      key="carouse-one"
      data={DATA}
      renderItem={(item, index) => <img src={item} alt={`image ${index}`} />}
      accentColor="blue"
      backgroundColor="#F5F5F5"
      isAutoPlay={true}
      initialActiveIndex={0}
      autoPlayInterval={5000}
      showRadioButtons={true}
      displayMode="image"
    />
  );
};

export default YourComponent;
```

### Card Carousel (displayMode: "card")

```tsx
import ReactSpinCarousel3D from "@carousel-ui/react-spin-carousel-3d";

// import imagePlaceHolder from "path-to-your-local-file";

interface Review {
  _id: number;
  name: string;
  description: string;
  profileImage: string;
}

const DATA: Review[] = [
  {
    _id: 1,
    name: "Sara Jones",
    description:
      "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Officia quam at minus blanditiis esse earum, unde ipsum ea aut quisquam ratione id magnam totam temporibus eaque consequuntur, voluptatum exercitationem assumenda recusandae. Explicabo optio consequuntur, minus porro facere quia? Nulla porro, laudantium maxime ab aliquam voluptatum magnam ducimus eveniet doloremque pariatur.",
    profileImage:
      "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1493136289900-28660d718589.avif",
  },
  {
    _id: 2,
    name: "Julie Smith",
    description:
      "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Officia quam at minus blanditiis esse earum, unde ipsum ea aut quisquam ratione id magnam totam temporibus eaque consequuntur, voluptatum exercitationem assumenda recusandae. Explicabo optio consequuntur, minus porro facere quia? Nulla porro, laudantium maxime ab aliquam voluptatum magnam ducimus eveniet doloremque pariatur.",
    profileImage:
      "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1552663651-2e4250e6c7c8.avif",
  },
  {
    _id: 3,
    name: "Meghan Markle",
    description:
      "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Officia quam at minus blanditiis esse earum, unde ipsum ea aut quisquam ratione id magnam totam temporibus eaque consequuntur, voluptatum exercitationem assumenda recusandae. Explicabo optio consequuntur, minus porro facere quia? Nulla porro, laudantium maxime ab aliquam voluptatum magnam ducimus eveniet doloremque pariatur.",
    profileImage:
      "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1656019674844-3040aba0350b.avif",
  },
  {
    _id: 4,
    name: "Sofia Turner",
    description:
      "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Officia quam at minus blanditiis esse earum, unde ipsum ea aut quisquam ratione id magnam totam temporibus eaque consequuntur, voluptatum exercitationem assumenda recusandae. Explicabo optio consequuntur, minus porro facere quia? Nulla porro, laudantium maxime ab aliquam voluptatum magnam ducimus eveniet doloremque pariatur.",
    profileImage:
      "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1661695423331-817b8aadd1a0.avif",
  },
  {
    _id: 5,
    name: "Clair Clarke",
    description:
      "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Officia quam at minus blanditiis esse earum, unde ipsum ea aut quisquam ratione id magnam totam temporibus eaque consequuntur, voluptatum exercitationem assumenda recusandae. Explicabo optio consequuntur, minus porro facere quia? Nulla porro, laudantium maxime ab aliquam voluptatum magnam ducimus eveniet doloremque pariatur.",
    profileImage:
      "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/premium_photo-1668485968590-aff3717c1dbe.avif",
  },
];

const YourComponent = () => {
  return (
    <ReactSpinCarousel3D<Review>
      key="carouse-one"
      data={DATA}
      itemStyle={{
        width: "350px",
      }}
      height="440px"
      renderItem={(item, index) => (
        <div style={{ height: "100%", fontFamily: "sans-serif" }} key={index}>
          <div style={{ height: "60%", width: "100%" }}>
            <img
              style={{ width: "100%", height: "100%", objectFit: "cover" }}
              src={item.profileImage}
              alt={`profile_image_${item._id}`}
            />
          </div>
          <div style={{ margin: "1rem" }}>
            <h2 style={{ color: "blue", marginBottom: "0.5rem" }}>
              {item.name}
            </h2>
            <p
              style={{
                color: "black",
                fontSize: "0.9rem",
                marginBottom: "0.5rem",
              }}
            >
              {item.description.slice(0, 150)}...
            </p>
            <button
              style={{
                border: "none",
                outline: "none",
                backgroundColor: "blue",
                color: "white",
                padding: "0.5rem 1rem",
                borderRadius: "5px",
              }}
            >
              Read Full Review
            </button>
          </div>
        </div>
      )}
      accentColor="blue"
      backgroundColor="#F5F5F5"
      isAutoPlay={true}
      initialActiveIndex={0}
      autoPlayInterval={5000}
      showRadioButtons={true}
      displayMode="card"
    />
  );
};

export default YourComponent;
```

### Custom Navigation

```tsx
import { CSSProperties } from "react";
import ReactSpinCarousel3D from "@carousel-ui/react-spin-carousel-3d";

// import imagePlaceHolder from "path-to-your-local-file";

interface Review {
  _id: number;
  name: string;
  description: string;
  profileImage: string;
}

const DATA: Review[] = [
  {
    _id: 1,
    name: "Sara Jones",
    description:
      "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Officia quam at minus blanditiis esse earum, unde ipsum ea aut quisquam ratione id magnam totam temporibus eaque consequuntur, voluptatum exercitationem assumenda recusandae. Explicabo optio consequuntur, minus porro facere quia? Nulla porro, laudantium maxime ab aliquam voluptatum magnam ducimus eveniet doloremque pariatur.",
    profileImage:
      "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1493136289900-28660d718589.avif",
  },
  {
    _id: 2,
    name: "Julie Smith",
    description:
      "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Officia quam at minus blanditiis esse earum, unde ipsum ea aut quisquam ratione id magnam totam temporibus eaque consequuntur, voluptatum exercitationem assumenda recusandae. Explicabo optio consequuntur, minus porro facere quia? Nulla porro, laudantium maxime ab aliquam voluptatum magnam ducimus eveniet doloremque pariatur.",
    profileImage:
      "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1552663651-2e4250e6c7c8.avif",
  },
  {
    _id: 3,
    name: "Meghan Markle",
    description:
      "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Officia quam at minus blanditiis esse earum, unde ipsum ea aut quisquam ratione id magnam totam temporibus eaque consequuntur, voluptatum exercitationem assumenda recusandae. Explicabo optio consequuntur, minus porro facere quia? Nulla porro, laudantium maxime ab aliquam voluptatum magnam ducimus eveniet doloremque pariatur.",
    profileImage:
      "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1656019674844-3040aba0350b.avif",
  },
  {
    _id: 4,
    name: "Sofia Turner",
    description:
      "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Officia quam at minus blanditiis esse earum, unde ipsum ea aut quisquam ratione id magnam totam temporibus eaque consequuntur, voluptatum exercitationem assumenda recusandae. Explicabo optio consequuntur, minus porro facere quia? Nulla porro, laudantium maxime ab aliquam voluptatum magnam ducimus eveniet doloremque pariatur.",
    profileImage:
      "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1661695423331-817b8aadd1a0.avif",
  },
  {
    _id: 5,
    name: "Clair Clarke",
    description:
      "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Officia quam at minus blanditiis esse earum, unde ipsum ea aut quisquam ratione id magnam totam temporibus eaque consequuntur, voluptatum exercitationem assumenda recusandae. Explicabo optio consequuntur, minus porro facere quia? Nulla porro, laudantium maxime ab aliquam voluptatum magnam ducimus eveniet doloremque pariatur.",
    profileImage:
      "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/premium_photo-1668485968590-aff3717c1dbe.avif",
  },
];

const YourComponent = () => {
  return (
    <ReactSpinCarousel3D<Review>
      key="carouse-one"
      data={DATA}
      itemStyle={{
        width: "350px",
      }}
      height="440px"
      renderItem={(item, index) => (
        <div style={{ height: "100%", fontFamily: "sans-serif" }} key={index}>
          <div style={{ height: "60%", width: "100%" }}>
            <img
              style={{ width: "100%", height: "100%", objectFit: "cover" }}
              src={item.profileImage}
              alt={`profile_image_${item._id}`}
            />
          </div>
          <div style={{ margin: "1rem" }}>
            <h2 style={{ color: "#323ebe", marginBottom: "0.5rem" }}>
              {item.name}
            </h2>
            <p
              style={{
                color: "black",
                fontSize: "0.9rem",
                marginBottom: "0.5rem",
              }}
            >
              {item.description.slice(0, 150)}...
            </p>
            <button
              style={{
                border: "none",
                outline: "none",
                backgroundColor: "#323ebe",
                color: "white",
                padding: "0.5rem 1rem",
                borderRadius: "5px",
              }}
            >
              Read Full Review
            </button>
          </div>
        </div>
      )}
      customRadioButtons={(index, isActive, setActiveIndex) => (
        <label
          key={index}
          style={{
            marginBottom: "0.5rem",
            marginRight: "8px",
            display: "flex",
            alignItems: "center",
            justifyContent: "center",
            position: "relative",
            cursor: "pointer",
            backgroundColor: isActive ? "black" : "#323ebe",
            color: "white",
            fontFamily: "sans-serif",
            fontSize: "0.9rem",
            fontWeight: "bold",
            padding: "0.2rem",
            borderRadius: "5px",
          }}
        >
          <input
            type="radio"
            name={`carousel-btn-${index}`}
            value={index + 1}
            checked={isActive}
            onChange={(e) => setActiveIndex(Number(e.target.value) - 1)}
            style={
              {
                width: "20px",
                height: "20px",
                appearance: "none",
                outline: "none",
                cursor: "pointer",
                borderRadius: "5px",
                transition: "all 100ms linear",
                display: "flex",
                justifyContent: "center",
                alignItems: "center",
                position: "relative",

                ":checked": {
                  backgroundColor: "#323ebe",
                  boxShadow: "0 1px 1px rgba(0, 0, 0, 0.18)",
                },
              } as CSSProperties
            }
          />
          <span
            style={{
              position: "absolute",
              fontSize: "14px",
              fontWeight: "bold",
              color: "white",
            }}
          >
            {index + 1}
          </span>
        </label>
      )}
      accentColor="#323ebe"
      backgroundColor="#F5F5F5"
      isAutoPlay={true}
      initialActiveIndex={0}
      autoPlayInterval={5000}
      showRadioButtons={true}
      displayMode="card"
    />
  );
};

export default YourComponent;
```

### Using Multiple Carousels together in a single page (Typescript)

```tsx
import { CSSProperties } from "react";
import ReactSpinCarousel3D from "@carousel-ui/react-spin-carousel-3d";

// import imagePlaceHolder from "path-to-your-local-file";

interface Review {
  _id: number;
  name: string;
  description: string;
  profileImage: string;
}

const data: string[] = [
  "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1493136289900-28660d718589.avif",
  "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1552663651-2e4250e6c7c8.avif",
  "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1656019674844-3040aba0350b.avif",
  "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1661695423331-817b8aadd1a0.avif",
  "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/premium_photo-1668485968590-aff3717c1dbe.avif",
  "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/premium_photo-1688497831136-0b76172b0f5f.avif",
  // imagePlaceHolder,
];

const DATA: Review[] = [
  {
    _id: 1,
    name: "Sara Jones",
    description:
      "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Officia quam at minus blanditiis esse earum, unde ipsum ea aut quisquam ratione id magnam totam temporibus eaque consequuntur, voluptatum exercitationem assumenda recusandae. Explicabo optio consequuntur, minus porro facere quia? Nulla porro, laudantium maxime ab aliquam voluptatum magnam ducimus eveniet doloremque pariatur.",
    profileImage:
      "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1493136289900-28660d718589.avif",
  },
  {
    _id: 2,
    name: "Julie Smith",
    description:
      "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Officia quam at minus blanditiis esse earum, unde ipsum ea aut quisquam ratione id magnam totam temporibus eaque consequuntur, voluptatum exercitationem assumenda recusandae. Explicabo optio consequuntur, minus porro facere quia? Nulla porro, laudantium maxime ab aliquam voluptatum magnam ducimus eveniet doloremque pariatur.",
    profileImage:
      "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1552663651-2e4250e6c7c8.avif",
  },
  {
    _id: 3,
    name: "Meghan Markle",
    description:
      "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Officia quam at minus blanditiis esse earum, unde ipsum ea aut quisquam ratione id magnam totam temporibus eaque consequuntur, voluptatum exercitationem assumenda recusandae. Explicabo optio consequuntur, minus porro facere quia? Nulla porro, laudantium maxime ab aliquam voluptatum magnam ducimus eveniet doloremque pariatur.",
    profileImage:
      "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1656019674844-3040aba0350b.avif",
  },
  {
    _id: 4,
    name: "Sofia Turner",
    description:
      "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Officia quam at minus blanditiis esse earum, unde ipsum ea aut quisquam ratione id magnam totam temporibus eaque consequuntur, voluptatum exercitationem assumenda recusandae. Explicabo optio consequuntur, minus porro facere quia? Nulla porro, laudantium maxime ab aliquam voluptatum magnam ducimus eveniet doloremque pariatur.",
    profileImage:
      "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1661695423331-817b8aadd1a0.avif",
  },
  {
    _id: 5,
    name: "Clair Clarke",
    description:
      "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Officia quam at minus blanditiis esse earum, unde ipsum ea aut quisquam ratione id magnam totam temporibus eaque consequuntur, voluptatum exercitationem assumenda recusandae. Explicabo optio consequuntur, minus porro facere quia? Nulla porro, laudantium maxime ab aliquam voluptatum magnam ducimus eveniet doloremque pariatur.",
    profileImage:
      "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/premium_photo-1668485968590-aff3717c1dbe.avif",
  },
];

const YourComponent = () => {
  return (
    <div style={{ display: "flex", gap: "2%" }}>
      <div
        style={{
          width: "32%",
          display: "flex",
          justifyContent: "center",
          alignItems: "center",
        }}
      >
        <ReactSpinCarousel3D<string>
          key="carousel-one" // needs to be unique of all carousels
          data={data}
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
      </div>
      <div style={{ width: "66%" }}>
        <ReactSpinCarousel3D<Review>
          key="carousel-two" // needs to be unique of all carousels
          data={DATA}
          itemStyle={{
            width: "350px",
          }}
          height="440px"
          renderItem={(item, index) => (
            <div
              style={{ height: "100%", fontFamily: "sans-serif" }}
              key={index}
            >
              <div style={{ height: "60%", width: "100%" }}>
                <img
                  style={{ width: "100%", height: "100%", objectFit: "cover" }}
                  src={item.profileImage}
                  alt={`profile_image_${item._id}`}
                />
              </div>
              <div style={{ margin: "1rem" }}>
                <h2 style={{ color: "#323ebe", marginBottom: "0.5rem" }}>
                  {item.name}
                </h2>
                <p
                  style={{
                    color: "black",
                    fontSize: "0.9rem",
                    marginBottom: "0.5rem",
                  }}
                >
                  {item.description.slice(0, 150)}...
                </p>
                <button
                  style={{
                    border: "none",
                    outline: "none",
                    backgroundColor: "#323ebe",
                    color: "white",
                    padding: "0.5rem 1rem",
                    borderRadius: "5px",
                  }}
                >
                  Read Full Review
                </button>
              </div>
            </div>
          )}
          customRadioButtons={(index, isActive, setActiveIndex) => (
            <label
              key={index}
              style={{
                marginBottom: "0.5rem",
                marginRight: "8px",
                display: "flex",
                alignItems: "center",
                justifyContent: "center",
                position: "relative",
                cursor: "pointer",
                backgroundColor: isActive ? "black" : "#323ebe",
                color: "white",
                fontFamily: "sans-serif",
                fontSize: "0.9rem",
                fontWeight: "bold",
                padding: "0.2rem",
                borderRadius: "5px",
              }}
            >
              <input
                type="radio"
                name={`carousel-btn-${index}`}
                value={index + 1}
                checked={isActive}
                onChange={(e) => setActiveIndex(Number(e.target.value) - 1)}
                style={
                  {
                    width: "20px",
                    height: "20px",
                    appearance: "none",
                    outline: "none",
                    cursor: "pointer",
                    borderRadius: "5px",
                    transition: "all 100ms linear",
                    display: "flex",
                    justifyContent: "center",
                    alignItems: "center",
                    position: "relative",

                    ":checked": {
                      backgroundColor: "#323ebe",
                      boxShadow: "0 1px 1px rgba(0, 0, 0, 0.18)",
                    },
                  } as CSSProperties
                }
              />
              <span
                style={{
                  position: "absolute",
                  fontSize: "14px",
                  fontWeight: "bold",
                  color: "white",
                }}
              >
                {index + 1}
              </span>
            </label>
          )}
          accentColor="#323ebe"
          backgroundColor="#F5F5F5"
          isAutoPlay={true}
          initialActiveIndex={0}
          autoPlayInterval={5000}
          showRadioButtons={true}
          displayMode="card"
        />
      </div>
    </div>
  );
};

export default YourComponent;
```

### Javascript

### Image Gallary (displayMode: "image")

```jsx
import React from "react";
import ReactSpinCarousel3D from "@carousel-ui/react-spin-carousel-3d";

// import imagePlaceHolder from "path-to-your-local-file";

const DATA = [
  "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1493136289900-28660d718589.avif",
  "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1552663651-2e4250e6c7c8.avif",
  "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1656019674844-3040aba0350b.avif",
  "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1661695423331-817b8aadd1a0.avif",
  "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/premium_photo-1668485968590-aff3717c1dbe.avif",
  "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/premium_photo-1688497831136-0b76172b0f5f.avif",
  // imagePlaceHolder,
];

const YourComponent = () => {
  return (
    <ReactSpinCarousel3D
      key="carouse-one"
      data={DATA}
      renderItem={(item, index) => <img src={item} alt={`image ${index}`} />}
      accentColor="blue"
      backgroundColor="#F5F5F5"
      isAutoPlay={true}
      initialActiveIndex={0}
      autoPlayInterval={5000}
      showRadioButtons={true}
      displayMode="image"
    />
  );
};

export default YourComponent;
```

### Card Carousel (displayMode: "card")

```jsx
// import imagePlaceHolder from "path-to-your-local-file";

import ReactSpinCarousel3D from "@carousel-ui/react-spin-carousel-3d";

const DATA = [
  {
    _id: 1,
    name: "Sara Jones",
    description:
      "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Officia quam at minus blanditiis esse earum, unde ipsum ea aut quisquam ratione id magnam totam temporibus eaque consequuntur, voluptatum exercitationem assumenda recusandae. Explicabo optio consequuntur, minus porro facere quia? Nulla porro, laudantium maxime ab aliquam voluptatum magnam ducimus eveniet doloremque pariatur.",
    profileImage:
      "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1493136289900-28660d718589.avif",
  },
  {
    _id: 2,
    name: "Julie Smith",
    description:
      "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Officia quam at minus blanditiis esse earum, unde ipsum ea aut quisquam ratione id magnam totam temporibus eaque consequuntur, voluptatum exercitationem assumenda recusandae. Explicabo optio consequuntur, minus porro facere quia? Nulla porro, laudantium maxime ab aliquam voluptatum magnam ducimus eveniet doloremque pariatur.",
    profileImage:
      "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1552663651-2e4250e6c7c8.avif",
  },
  {
    _id: 3,
    name: "Meghan Markle",
    description:
      "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Officia quam at minus blanditiis esse earum, unde ipsum ea aut quisquam ratione id magnam totam temporibus eaque consequuntur, voluptatum exercitationem assumenda recusandae. Explicabo optio consequuntur, minus porro facere quia? Nulla porro, laudantium maxime ab aliquam voluptatum magnam ducimus eveniet doloremque pariatur.",
    profileImage:
      "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1656019674844-3040aba0350b.avif",
  },
  {
    _id: 4,
    name: "Sofia Turner",
    description:
      "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Officia quam at minus blanditiis esse earum, unde ipsum ea aut quisquam ratione id magnam totam temporibus eaque consequuntur, voluptatum exercitationem assumenda recusandae. Explicabo optio consequuntur, minus porro facere quia? Nulla porro, laudantium maxime ab aliquam voluptatum magnam ducimus eveniet doloremque pariatur.",
    profileImage:
      "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1661695423331-817b8aadd1a0.avif",
  },
  {
    _id: 5,
    name: "Clair Clarke",
    description:
      "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Officia quam at minus blanditiis esse earum, unde ipsum ea aut quisquam ratione id magnam totam temporibus eaque consequuntur, voluptatum exercitationem assumenda recusandae. Explicabo optio consequuntur, minus porro facere quia? Nulla porro, laudantium maxime ab aliquam voluptatum magnam ducimus eveniet doloremque pariatur.",
    profileImage:
      "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/premium_photo-1668485968590-aff3717c1dbe.avif",
  },
];

const YourComponent = () => {
  return (
    <ReactSpinCarousel3D
      key="carouse-one"
      data={DATA}
      itemStyle={{
        width: "350px",
      }}
      height="440px"
      renderItem={(item, index) => (
        <div style={{ height: "100%", fontFamily: "sans-serif" }} key={index}>
          <div style={{ height: "60%", width: "100%" }}>
            <img
              style={{
                width: "100%",
                height: "100%",
                objectFit: "cover",
                userSelect: "none",
              }}
              src={item.profileImage}
              alt={`profile_image_${item._id}`}
            />
          </div>
          <div style={{ margin: "1rem" }}>
            <h2 style={{ color: "blue", marginBottom: "0.5rem" }}>
              {item.name}
            </h2>
            <p
              style={{
                color: "black",
                fontSize: "0.9rem",
                marginBottom: "0.5rem",
              }}
            >
              {item.description.slice(0, 150)}...
            </p>
            <button
              style={{
                border: "none",
                outline: "none",
                backgroundColor: "blue",
                color: "white",
                padding: "0.5rem 1rem",
                borderRadius: "5px",
              }}
            >
              Read Full Review
            </button>
          </div>
        </div>
      )}
      accentColor="blue"
      backgroundColor="#F5F5F5"
      isAutoPlay={true}
      initialActiveIndex={0}
      autoPlayInterval={5000}
      showRadioButtons={true}
      displayMode="card"
    />
  );
};

export default YourComponent;
```

### Custom Navigation

```jsx
// import imagePlaceHolder from "path-to-your-local-file";

import ReactSpinCarousel3D from "@carousel-ui/react-spin-carousel-3d";

const DATA = [
  {
    _id: 1,
    name: "Sara Jones",
    description:
      "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Officia quam at minus blanditiis esse earum, unde ipsum ea aut quisquam ratione id magnam totam temporibus eaque consequuntur, voluptatum exercitationem assumenda recusandae. Explicabo optio consequuntur, minus porro facere quia? Nulla porro, laudantium maxime ab aliquam voluptatum magnam ducimus eveniet doloremque pariatur.",
    profileImage:
      "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1493136289900-28660d718589.avif",
  },
  {
    _id: 2,
    name: "Julie Smith",
    description:
      "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Officia quam at minus blanditiis esse earum, unde ipsum ea aut quisquam ratione id magnam totam temporibus eaque consequuntur, voluptatum exercitationem assumenda recusandae. Explicabo optio consequuntur, minus porro facere quia? Nulla porro, laudantium maxime ab aliquam voluptatum magnam ducimus eveniet doloremque pariatur.",
    profileImage:
      "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1552663651-2e4250e6c7c8.avif",
  },
  {
    _id: 3,
    name: "Meghan Markle",
    description:
      "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Officia quam at minus blanditiis esse earum, unde ipsum ea aut quisquam ratione id magnam totam temporibus eaque consequuntur, voluptatum exercitationem assumenda recusandae. Explicabo optio consequuntur, minus porro facere quia? Nulla porro, laudantium maxime ab aliquam voluptatum magnam ducimus eveniet doloremque pariatur.",
    profileImage:
      "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1656019674844-3040aba0350b.avif",
  },
  {
    _id: 4,
    name: "Sofia Turner",
    description:
      "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Officia quam at minus blanditiis esse earum, unde ipsum ea aut quisquam ratione id magnam totam temporibus eaque consequuntur, voluptatum exercitationem assumenda recusandae. Explicabo optio consequuntur, minus porro facere quia? Nulla porro, laudantium maxime ab aliquam voluptatum magnam ducimus eveniet doloremque pariatur.",
    profileImage:
      "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1661695423331-817b8aadd1a0.avif",
  },
  {
    _id: 5,
    name: "Clair Clarke",
    description:
      "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Officia quam at minus blanditiis esse earum, unde ipsum ea aut quisquam ratione id magnam totam temporibus eaque consequuntur, voluptatum exercitationem assumenda recusandae. Explicabo optio consequuntur, minus porro facere quia? Nulla porro, laudantium maxime ab aliquam voluptatum magnam ducimus eveniet doloremque pariatur.",
    profileImage:
      "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/premium_photo-1668485968590-aff3717c1dbe.avif",
  },
];

const YourComponent = () => {
  return (
    <ReactSpinCarousel3D
      key="carouse-one"
      data={DATA}
      itemStyle={{
        width: "350px",
      }}
      height="440px"
      renderItem={(item, index) => (
        <div style={{ height: "100%", fontFamily: "sans-serif" }} key={index}>
          <div style={{ height: "60%", width: "100%" }}>
            <img
              style={{ width: "100%", height: "100%", objectFit: "cover" }}
              src={item.profileImage}
              alt={`profile_image_${item._id}`}
            />
          </div>
          <div style={{ margin: "1rem" }}>
            <h2 style={{ color: "#323ebe", marginBottom: "0.5rem" }}>
              {item.name}
            </h2>
            <p
              style={{
                color: "black",
                fontSize: "0.9rem",
                marginBottom: "0.5rem",
              }}
            >
              {item.description.slice(0, 150)}...
            </p>
            <button
              style={{
                border: "none",
                outline: "none",
                backgroundColor: "#323ebe",
                color: "white",
                padding: "0.5rem 1rem",
                borderRadius: "5px",
              }}
            >
              Read Full Review
            </button>
          </div>
        </div>
      )}
      customRadioButtons={(index, isActive, setActiveIndex) => (
        <label
          key={index}
          style={{
            marginBottom: "0.5rem",
            marginRight: "8px",
            display: "flex",
            alignItems: "center",
            justifyContent: "center",
            position: "relative",
            cursor: "pointer",
            backgroundColor: isActive ? "black" : "#323ebe",
            color: "white",
            fontFamily: "sans-serif",
            fontSize: "0.9rem",
            fontWeight: "bold",
            padding: "0.2rem",
            borderRadius: "5px",
          }}
        >
          <input
            type="radio"
            name={`carousel-btn-${index}`}
            value={index + 1}
            checked={isActive}
            onChange={(e) => setActiveIndex(Number(e.target.value) - 1)}
            style={{
              width: "20px",
              height: "20px",
              appearance: "none",
              outline: "none",
              cursor: "pointer",
              borderRadius: "5px",
              transition: "all 100ms linear",
              display: "flex",
              justifyContent: "center",
              alignItems: "center",
              position: "relative",
            }}
          />
          <span
            style={{
              position: "absolute",
              fontSize: "14px",
              fontWeight: "bold",
              color: "white",
            }}
          >
            {index + 1}
          </span>
        </label>
      )}
      accentColor="#323ebe"
      backgroundColor="#F5F5F5"
      isAutoPlay={true}
      initialActiveIndex={0}
      autoPlayInterval={5000}
      showRadioButtons={true}
      displayMode="card"
    />
  );
};

export default YourComponent;
```

### Using Multiple Carousels together in a single page (Javascript)

```jsx
// import imagePlaceHolder from "path-to-your-local-file";

import ReactSpinCarousel3D from "@carousel-ui/react-spin-carousel-3d";

const data = [
  "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1493136289900-28660d718589.avif",
  "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1552663651-2e4250e6c7c8.avif",
  "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1656019674844-3040aba0350b.avif",
  "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1661695423331-817b8aadd1a0.avif",
  "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/premium_photo-1668485968590-aff3717c1dbe.avif",
  "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/premium_photo-1688497831136-0b76172b0f5f.avif",
  // imagePlaceHolder,
];

const DATA = [
  {
    _id: 1,
    name: "Sara Jones",
    description:
      "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Officia quam at minus blanditiis esse earum, unde ipsum ea aut quisquam ratione id magnam totam temporibus eaque consequuntur, voluptatum exercitationem assumenda recusandae. Explicabo optio consequuntur, minus porro facere quia? Nulla porro, laudantium maxime ab aliquam voluptatum magnam ducimus eveniet doloremque pariatur.",
    profileImage:
      "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1493136289900-28660d718589.avif",
  },
  {
    _id: 2,
    name: "Julie Smith",
    description:
      "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Officia quam at minus blanditiis esse earum, unde ipsum ea aut quisquam ratione id magnam totam temporibus eaque consequuntur, voluptatum exercitationem assumenda recusandae. Explicabo optio consequuntur, minus porro facere quia? Nulla porro, laudantium maxime ab aliquam voluptatum magnam ducimus eveniet doloremque pariatur.",
    profileImage:
      "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1552663651-2e4250e6c7c8.avif",
  },
  {
    _id: 3,
    name: "Meghan Markle",
    description:
      "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Officia quam at minus blanditiis esse earum, unde ipsum ea aut quisquam ratione id magnam totam temporibus eaque consequuntur, voluptatum exercitationem assumenda recusandae. Explicabo optio consequuntur, minus porro facere quia? Nulla porro, laudantium maxime ab aliquam voluptatum magnam ducimus eveniet doloremque pariatur.",
    profileImage:
      "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1656019674844-3040aba0350b.avif",
  },
  {
    _id: 4,
    name: "Sofia Turner",
    description:
      "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Officia quam at minus blanditiis esse earum, unde ipsum ea aut quisquam ratione id magnam totam temporibus eaque consequuntur, voluptatum exercitationem assumenda recusandae. Explicabo optio consequuntur, minus porro facere quia? Nulla porro, laudantium maxime ab aliquam voluptatum magnam ducimus eveniet doloremque pariatur.",
    profileImage:
      "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/photo-1661695423331-817b8aadd1a0.avif",
  },
  {
    _id: 5,
    name: "Clair Clarke",
    description:
      "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Officia quam at minus blanditiis esse earum, unde ipsum ea aut quisquam ratione id magnam totam temporibus eaque consequuntur, voluptatum exercitationem assumenda recusandae. Explicabo optio consequuntur, minus porro facere quia? Nulla porro, laudantium maxime ab aliquam voluptatum magnam ducimus eveniet doloremque pariatur.",
    profileImage:
      "https://raw.githubusercontent.com/SpurgeonPrakash/images-for-carousel-ui/main/premium_photo-1668485968590-aff3717c1dbe.avif",
  },
];

const YourComponent = () => {
  return (
    <div style={{ display: "flex", gap: "2%" }}>
      <div
        style={{
          width: "32%",
          display: "flex",
          justifyContent: "center",
          alignItems: "center",
        }}
      >
        <ReactSpinCarousel3D
          key="carousel-one"
          data={data}
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
      </div>
      <div style={{ width: "66%" }}>
        <ReactSpinCarousel3D
          key="carousel-two"
          data={DATA}
          itemStyle={{
            width: "350px",
          }}
          height="440px"
          renderItem={(item, index) => (
            <div
              style={{ height: "100%", fontFamily: "sans-serif" }}
              key={index}
            >
              <div style={{ height: "60%", width: "100%" }}>
                <img
                  style={{ width: "100%", height: "100%", objectFit: "cover" }}
                  src={item.profileImage}
                  alt={`profile_image_${item._id}`}
                />
              </div>
              <div style={{ margin: "1rem" }}>
                <h2 style={{ color: "#323ebe", marginBottom: "0.5rem" }}>
                  {item.name}
                </h2>
                <p
                  style={{
                    color: "black",
                    fontSize: "0.9rem",
                    marginBottom: "0.5rem",
                  }}
                >
                  {item.description.slice(0, 150)}...
                </p>
                <button
                  style={{
                    border: "none",
                    outline: "none",
                    backgroundColor: "#323ebe",
                    color: "white",
                    padding: "0.5rem 1rem",
                    borderRadius: "5px",
                  }}
                >
                  Read Full Review
                </button>
              </div>
            </div>
          )}
          customRadioButtons={(index, isActive, setActiveIndex) => (
            <label
              key={index}
              style={{
                marginBottom: "0.5rem",
                marginRight: "8px",
                display: "flex",
                alignItems: "center",
                justifyContent: "center",
                position: "relative",
                cursor: "pointer",
                backgroundColor: isActive ? "black" : "#323ebe",
                color: "white",
                fontFamily: "sans-serif",
                fontSize: "0.9rem",
                fontWeight: "bold",
                padding: "0.2rem",
                borderRadius: "5px",
              }}
            >
              <input
                type="radio"
                name={`carousel-btn-${index}`}
                value={index + 1}
                checked={isActive}
                onChange={(e) => setActiveIndex(Number(e.target.value) - 1)}
                style={{
                  width: "20px",
                  height: "20px",
                  appearance: "none",
                  outline: "none",
                  cursor: "pointer",
                  borderRadius: "5px",
                  transition: "all 100ms linear",
                  display: "flex",
                  justifyContent: "center",
                  alignItems: "center",
                  position: "relative",
                }}
              />
              <span
                style={{
                  position: "absolute",
                  fontSize: "14px",
                  fontWeight: "bold",
                  color: "white",
                }}
              >
                {index + 1}
              </span>
            </label>
          )}
          accentColor="#323ebe"
          backgroundColor="#F5F5F5"
          isAutoPlay={true}
          initialActiveIndex={0}
          autoPlayInterval={5000}
          showRadioButtons={true}
          displayMode="card"
        />
      </div>
    </div>
  );
};

export default YourComponent;
```

## 🛠 Props Reference

### Core Props

| Prop         | Type                                          | Default      | Description                   |
| ------------ | --------------------------------------------- | ------------ | ----------------------------- |
| `data`       | `T[]`                                         | **Required** | Array of items to render      |
| `renderItem` | `(item: T, index: number) => React.ReactNode` | **Required** | Render function for each item |

### Layout & Styling

| Prop              | Type                  | Default               | Description                        |
| ----------------- | --------------------- | --------------------- | ---------------------------------- |
| `width`           | `string \| number`    | `"100vw"`             | Container width (px or %)          |
| `height`          | `string \| number`    | `300`                 | Container height (px or %)         |
| `itemWidth`       | `string \| number`    | `300`                 | Individual item width (px or %)    |
| `accentColor`     | `string`              | `"hsl(204, 5%, 38%)"` | Color for active states            |
| `backgroundColor` | `string`              | `"#F5F5F5"`           | Background color for card mode     |
| `containerStyle`  | `React.CSSProperties` | `{}`                  | Custom styles for container div    |
| `itemStyle`       | `React.CSSProperties` | `{}`                  | Custom styles for individual items |

### Behavior & Functionality

| Prop                 | Type                               | Default      | Description                       |
| -------------------- | ---------------------------------- | ------------ | --------------------------------- |
| `initialActiveIndex` | `number`                           | Middle index | Starting active item index        |
| `isAutoPlay`         | `boolean`                          | `false`      | Enable automatic rotation         |
| `autoPlayInterval`   | `number`                           | `5000`       | Rotation interval in milliseconds |
| `onItemClick`        | `(item: T, index: number) => void` | -            | Callback when item is clicked     |

### Display Mode

| Prop            | Type                             | Default    | Description                         |
| --------------- | -------------------------------- | ---------- | ----------------------------------- |
| `displayMode`   | `"image" \| "card"`              | `"card"`   | Visual presentation style           |
| `imageFit`      | `"cover" \| "contain" \| "fill"` | `"cover"`  | Image scaling behavior (image mode) |
| `imagePosition` | `string`                         | `"center"` | Image positioning (e.g. "top left") |

### Navigation Controls

| Prop                 | Type                                                   | Default | Description                        |
| -------------------- | ------------------------------------------------------ | ------- | ---------------------------------- |
| `showRadioButtons`   | `boolean`                                              | `true`  | Show default navigation indicators |
| `customRadioButtons` | `(index, isActive, setActiveIndex) => React.ReactNode` | -       | Custom navigation component        |
| `radioButtonStyle`   | `React.CSSProperties`                                  | `{}`    | Styles for default navigation dots |

### Advanced Configuration

| Prop  | Type     | Default | Description                    |
| ----- | -------- | ------- | ------------------------------ |
| `key` | `string` | -       | Unique identifier for carousel |

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

**Issue**: Auto-play stops on hover  
**Solution**: This is intentional (UX best practice). Lets the user observe whats inside the card while hovering!

**Issue**: Radio buttons not properly working when using multiple carousels in same page  
**Solution**: Use unique key on each carousel

**Issue**: Horizontal scroll appears  
**Fix**: Ensure parent container has `overflow-x: hidden`

**Issue**: Items overlapping  
**Fix**: Increase `itemWidth` or reduce number of items

## 📜 License

MIT © @carousel-ui
