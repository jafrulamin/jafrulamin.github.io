# Homework 2 Reflection

## 1. flex-direction: row vs flex-direction: column

`flex-direction` controls which way flex items are placed inside a flex container.

- **row** → items are placed side by side, left to right (this is the default)
- **column** → items are stacked on top of each other, top to bottom

For example, the nav bar uses `flex-direction: row` on desktop so the links sit next to each other. On mobile (screen width 768px or less), I switch it to `flex-direction: column` so the links stack vertically and are easier to tap.

## 2. Why Use Relative Units Instead of px

- **px** is a fixed size,it stays the same no matter what screen or font size the user has
- **rem** is relative to the browser's base font size,if the user has a bigger font set, things scale up automatically
- **%** is relative to the parent element's size,useful for making things fit their container
- **vh** is relative to the screen height,useful for full-screen sections

Using relative units means the page looks better on different screen sizes without having to write a separate rule for every single case. Hard-coded `px` values can make text too small on some screens or too big on others.

## 3. AI Attribution

**Prompt Used:**
"What properties do I need on a flex container to center items inside it?"

I used AI to quickly look up the correct flex properties (`justify-content` and `align-items`) when I was centering the nav links. I already had the nav written and knew I needed flexbox, I just wasn't sure which combination of properties to use.

**CSS Snippet I Had to Fix:**

I wrote this first:
```css
.nav-list {
  display: flex;
  gap: 24px;
}
```

The links were not centered so I asked AI what was missing. It told me to add `justify-content: center` to the container. I updated it to:
```css
.nav-list {
  display: flex;
  gap: 24px;
  justify-content: center;
}
```


