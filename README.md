# ParaTkinter - Simple Parallax Effect for CustomTkinter 🖱️✨

**ParaTkinter** brings smooth, responsive parallax layers to your `customtkinter` GUI apps with minimal setup. Enhance your UI with interactive motion effects that follow the mouse.

---

## 🚀 Features

- Easy-to-use `ParallaxManager` class
- Adjustable depth per layer
- Configurable easing and FPS
- Works seamlessly with `customtkinter` widgets

---

## 📦 Installation

```bash
pip install paratkinter
# If customtkinter is not installed: 'pip install customtkinter'
```
## 🛠️ Setup
```bash
import customtkinter as ctk
from parallax import ParallaxManager
```



## Initialization
```bash
app = ctk.CTk()
parallax = ParallaxManager(app, easing=0.1)
```
- Initialize the Parallax Layout using a CustomTkinter app
- Configure the parallax using easing


## Add Layers
```bash
label_bg = ctk.CTkLabel(app, text="Back Layer", font=("Arial", 22))
label_mid = ctk.CTkLabel(app, text="Mid Layer", font=("Arial", 28))
label_fg = ctk.CTkLabel(app, text="Front Layer", font=("Arial", 36, "bold"))

parallax.add_layer(label_bg, base_relx=0.5, base_rely=0.3, depth=0.01)
parallax.add_layer(label_mid, base_relx=0.5, base_rely=0.4, depth=0.03)
parallax.add_layer(label_fg, base_relx=0.5, base_rely=0.5, depth=0.06)

```
💡 Tips
- Lower depth = slower movement (background)

- Higher depth = faster movement (foreground)

- easing controls transition smoothness (try 0.05 to 0.2)

Enjoy building awesome parallax applications with ParaTkinter!
---
Known Bugs
- Hovering your mouse pointer on any widget in the parallax layout automatically shifts the entire layout to the left. Working on a fix, if anyone could help please let me know.
