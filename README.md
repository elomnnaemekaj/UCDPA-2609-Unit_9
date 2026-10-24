# Unit 09 – Student Hands-On Lab

## Building a Responsive Personal Site with Bootstrap

---

## Purpose of this lab

In this lab, you will:

- Use Bootstrap via CDN
- Build a clean, responsive landing page
- Use Bootstrap utility classes instead of custom CSS
- Work with Bootstrap components:
  - Navbar
  - Card
  - Grid system

- Understand responsive behaviour without writing media queries
- Add optional custom CSS overrides

The focus is on **layout, structure, and responsiveness**, not visual perfection.

---

## Prerequisites

Before starting, make sure you have:

- VS Code (or another editor) open
- A web browser available
- An empty project folder
- Basic HTML knowledge
- No prior Bootstrap experience required

---

## Part 1 — Setup and Base Structure

### Goal

Create a valid HTML file and load Bootstrap.

---

### Steps

1. Create a file named `index.html`
2. Add the following starter template:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Bootstrap Demo</title>

    <link
      href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css"
      rel="stylesheet"
    />
  </head>

  <body>
    <div class="container py-5">
      <!-- Content will go here -->
    </div>
  </body>
</html>
```

3. Save and open the file in your browser.

---

### Checkpoint

- The page loads without errors
- Bootstrap styles are applied (default font and spacing)

---

## Part 2 — Header and Intro Section

### Goal

Use Bootstrap utility classes for typography and spacing.

---

### Steps

Inside the `.container`, add:

```html
<header class="text-center mb-5">
  <h1 class="display-4">Welcome to My Profile</h1>
  <p class="lead text-muted">Using Bootstrap to build responsive layouts</p>
</header>
```

---

### Notes

- `text-center` aligns text
- `display-4` creates a large heading
- `lead` styles introductory text
- `mb-5` adds vertical spacing

---

### Checkpoint

- Heading is large and centred
- Subtitle appears lighter and spaced

---

## Part 3 — Profile Card

### Goal

Use a Bootstrap component to group content visually.

---

### Steps

Add the following below the header:

```html
<div class="card mx-auto" style="max-width: 400px;">
  <img
    src="https://via.placeholder.com/400x200"
    class="card-img-top"
    alt="Profile Image"
  />

  <div class="card-body text-center">
    <h5 class="card-title">Housam Ziad</h5>

    <p class="card-text">
      Lecturer, Full-Stack Developer, and Designer. Passionate about education
      and technology.
    </p>

    <a href="#" class="btn btn-primary">Contact</a>
  </div>
</div>
```

---

### Notes

- `card` groups content
- `mx-auto` centres the card
- `btn btn-primary` creates a styled button

---

### Checkpoint

- Card appears centred
- Image, text, and button are stacked neatly

---

## Part 4 — Features Section Using the Grid

### Goal

Use Bootstrap’s grid system for responsive layouts.

---

### Steps

Add the following below the card:

```html
<section class="mt-5">
  <div class="row g-4">
    <div class="col-md-4">
      <div class="p-4 border rounded text-center bg-light">
        <h5>Teaching</h5>
        <p>Practical courses on web, design, and development.</p>
      </div>
    </div>

    <div class="col-md-4">
      <div class="p-4 border rounded text-center bg-light">
        <h5>Mentoring</h5>
        <p>Helping learners grow with guidance and support.</p>
      </div>
    </div>

    <div class="col-md-4">
      <div class="p-4 border rounded text-center bg-light">
        <h5>Projects</h5>
        <p>From prototypes to full-stack tools, built in the open.</p>
      </div>
    </div>
  </div>
</section>
```

---

### Notes

- `.row` creates a horizontal layout
- `.col-md-4` creates responsive columns
- `g-4` adds spacing between columns

---

### Checkpoint

- Cards stack vertically on small screens
- Cards align in three columns on larger screens

---

## Part 5 — Navigation Bar

### Goal

Add a responsive navigation bar using Bootstrap.

---

### Steps

Add this **above the header**:

```html
<nav class="navbar navbar-expand-lg navbar-light bg-light mb-4">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">MySite</a>

    <button
      class="navbar-toggler"
      type="button"
      data-bs-toggle="collapse"
      data-bs-target="#navbarNav"
    >
      <span class="navbar-toggler-icon"></span>
    </button>

    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav ms-auto">
        <li class="nav-item">
          <a class="nav-link" href="#">About</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Projects</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Contact</a>
        </li>
      </ul>
    </div>
  </div>
</nav>
```

---

### Notes

- `navbar-expand-lg` controls when the menu collapses
- `ms-auto` pushes items to the right
- The toggle button appears on smaller screens

---

### Checkpoint

- Navbar collapses on small screens
- Toggle button expands and collapses menu

---

## Part 6 — Responsive Tweaks with Utilities

### Goal

Adjust layout behaviour using Bootstrap utility classes.

---

### Try the following changes:

- Add `text-md-start` alongside `text-center` in the header
- Add `p-2 p-lg-5` to sections for responsive padding
- Use `d-none d-md-block` to hide elements on small screens

---

### Checkpoint

- Layout adapts without writing CSS
- Responsive behaviour is controlled via class names

---

## Part 7 — Optional Custom CSS Overrides

### Goal

Layer custom styles on top of Bootstrap when needed.

---

### Steps

1. Create `style.css`
2. Link it **after** the Bootstrap CDN:

```html
<link rel="stylesheet" href="style.css" />
```

3. Add optional overrides:

```css
body {
  font-family: "Segoe UI", sans-serif;
}

.btn-primary {
  background-color: darkslateblue;
  border: none;
}
```

---

### Notes

- Bootstrap should handle most layout needs
- Custom CSS is for small tweaks only

---

## Final Review

You should now be able to:

- Build responsive layouts using Bootstrap
- Use utility classes instead of custom CSS
- Understand the Bootstrap grid system
- Create common UI components quickly
- Control responsiveness without media queries

---

## End of Unit 09 Hands-On Lab

You are now ready to combine **custom CSS, Flexbox, Grid, and Bootstrap** confidently in real projects.