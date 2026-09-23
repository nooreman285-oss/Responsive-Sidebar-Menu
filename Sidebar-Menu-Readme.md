# Responsive Sidebar Menu (Mini CSS Project)

A simple, responsive sidebar/hamburger menu built with pure HTML and CSS (no JavaScript). The menu slides in and out using the classic checkbox-hack technique, with a full-screen background image and Font Awesome icons.

## 🚀 Features

- Slide-in / slide-out sidebar navigation
- Toggled with a checkbox (no JavaScript required)
- Full-screen background image with `cover` sizing
- Icon-based menu items using **Font Awesome 6**
- Google Fonts (**Poppins**) for typography
- Hover effects on menu items and social icons
- Social media icon links (Facebook, Twitter, Instagram, YouTube)

## 🛠️ Built With

- **HTML5**
- **CSS3** (Flexbox-free, positioning-based layout)
- [Font Awesome 6.4.0](https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css) — icons
- [Google Fonts — Poppins](https://fonts.google.com/specimen/Poppins) — typography

## 📁 Project Structure

```
mini-css-project/
├── index.html      # Page markup & sidebar structure
├── style.css       # All styling, layout, and transitions
├── camera.jpg      # Background image (add your own)
└── README.md
```

## ⚙️ How It Works

The sidebar uses the **checkbox hack**:

1. A hidden checkbox (`#check`) tracks the open/closed state.
2. The hamburger icon (`.btn_one`) is a `<label>` linked to that checkbox.
3. When checked, the `:checked ~ .sidebar_menu` selector shifts the sidebar from `left: -300px` to `left: 0`, sliding it into view.
4. The close icon (`.btn_two`) is also a label for the same checkbox, unchecking it and sliding the sidebar back out.
5. A `transition: all 0.3s linear` gives the slide a smooth animation.

## ▶️ Getting Started

1. Clone or download this project.
2. Make sure `camera.jpg` (or your chosen background image) sits in the same folder as `index.html`.
3. Open `index.html` in any modern browser — no build step or server required.

```bash
git clone <your-repo-url>
cd mini-css-project
open index.html   # or just double-click the file
```

## 🔧 Customization

| What to change        | Where                                  |
|------------------------|-----------------------------------------|
| Background image       | `.main_box { background: url(...); }` |
| Sidebar width           | `.sidebar_menu { width: 300px; }`     |
| Menu items              | Edit the `<ul>` inside `.menu` in `index.html` |
| Font                     | Swap the Google Fonts link + `font-family` in CSS |
| Sidebar transparency    | `.sidebar_menu { background-color: rgba(...); }` |

## 🐞 Known Issues / To-Do

- `rgba(255, 525, 255, 0.1)` has an invalid green value (525 > 255) — should likely be `rgba(255, 255, 255, 0.1)`.
- Duplicate `<i>` closing tags on the Facebook and Instagram social icons in `index.html`.
- `font-weight: 700px` on `.btn_one i` is invalid — `font-weight` doesn't take a `px` unit (should just be `700`).
- No JavaScript fallback — relies entirely on the checkbox hack, which is fine for this scope but not accessible via keyboard-only navigation (consider adding `:focus` styles or ARIA attributes for accessibility).

## 📄 License

This project is open source and available for learning purposes.

## 🙌 Credits

Icons by [Font Awesome](https://fontawesome.com/). Font by [Google Fonts](https://fonts.google.com/).
