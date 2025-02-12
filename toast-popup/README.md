# Toast Popup self

React Toast Popup is a simple and customizable toast notification component for React applications.


## Installation

You can install React Toast Popup via npm:

```jsx
npm install toast-popup-self
```

## Usage

To use React Toast Popup in your React application, follow these steps:

Import the useNotification hook and necessary styles in your component:

```jsx
import useNotification from "toast-popup-self";
```

Initialize the useNotification hook with your preferred position:

```jsx
const { NotificationComponent, triggerNotification } =
  useNotification("top-left");
```

#### Postions

- "bottom-left"
- "bottom-right"
- "top-left"
- "top-right"

Use NotificationComponent in your JSX to display notifications:

```jsx
return (
  <div className="App">
    {NotificationComponent}
    {/* Your other JSX content */}
  </div>
);
```

Trigger notifications using the triggerNotification function:

```jsx
triggerNotification({
  type: "success",
  message: "This is a success message!",
  duration: 3000,
});
```

#### Animations

You can specify an animation type for the notifications. The available animations are:

- "fade"
- "pop"
- "slide"

```jsx
triggerNotification({
  type: "success",
  message: "This is a success message with a pop animation!",
  duration: 3000,
  animation: "pop",
});
