<h3 align="center">
<img src="https://raw.githubusercontent.com/catppuccin/catppuccin/main/assets/logos/exports/1544x1544_circle.png" width="100" alt="Logo"/><br/>
<img src="https://raw.githubusercontent.com/catppuccin/catppuccin/main/assets/misc/transparent.png" height="30" width="0px"/>
  Catppuccin for <a href="https://www.gnu.org/software/emacs/">Emacs</a>
<img src="https://raw.githubusercontent.com/catppuccin/catppuccin/main/assets/misc/transparent.png" height="30" width="0px"/>
</h3>

<p align="center">
<a href="https://github.com/catppuccin/emacs/stargazers"><img src="https://img.shields.io/github/stars/catppuccin/emacs?colorA=363a4f&colorB=b7bdf8&style=for-the-badge"></a>
<a href="https://github.com/catppuccin/emacs/issues"><img src="https://img.shields.io/github/issues/catppuccin/emacs?colorA=363a4f&colorB=f5a97f&style=for-the-badge"></a>
<a href="https://github.com/catppuccin/emacs/contributors"><img src="https://img.shields.io/github/contributors/catppuccin/emacs?colorA=363a4f&colorB=a6da95&style=for-the-badge"></a>
</p>

<p align="center">
<img src="assets/Screenshot.webp"/>
</p>

# About

This Emacs theme was made with the [Dracula](https://github.com/dracula/emacs) theme as a base.

## Previews

<details>
<summary>🌻 Latte</summary>
<img src="assets/Latte.webp"/>
</details>
<details>
<summary>🪴 Frappé</summary>
<img src="assets/Frappe.webp"/>
</details>
<details>
<summary>🌺 Macchiato</summary>
<img src="assets/Macchiato.webp"/>
</details>
<details>
<summary>🌿 Mocha</summary>
<img src="assets/Mocha.webp"/>
</details>

# Installation

`catppuccin-theme` is available on the MELPA package repository.

## Emacs

1. Make sure to have MELPA enabled by adding it to the `package-archives`, or that your package manager of choice has MELPA as a repository.
2. You can then install the package from the `list-packages` interface, accessible from `M-x list-packages`.
3. Alternatively, you can install the package using your package manager of choice, such as straight

```lisp
(straight-use-package 'catppuccin-theme)
```

4. Then, you can enable it by adding the following to your `init.el` file

```lisp
(load-theme 'catppuccin :no-confirm)
```

## Doom Emacs

1. Add the following to your `package.el`

```lisp
(package! catppuccin-theme)
```

2. Add the following to your `config.el`

```lisp
(setq doom-theme 'catppuccin)
```

# Configuration

The default flavour is Mocha, to change the flavor, place the following in your `init.el` or `config.el`
after loading the theme

```lisp
(setq catppuccin-flavor 'frappe) ;; or 'latte, 'macchiato, or 'mocha
(catppuccin-reload)
```

The theme can also be customzied further by changing individual colors.
Doom users must call `(load-theme 'catppuccin t t)` before being able to call any of the `catppuccin-*` functions.

```lisp
(catppuccin-set-color 'base "#000000") ;; change base to #000000 for the currently active flavor
(catppuccin-set-color 'crust "#222222" 'frappe) ;; change crust to #222222 for frappe
(catppuccin-reload)
```

>[!NOTE]
>If you are using emacsclient and rustic, you should add `(add-hook 'server-after-make-frame-hook #'catppuccin-reload)` to your config to avoid [this issue](https://github.com/catppuccin/emacs/issues/121)

>[!NOTE]
>If you are using doom emacs and want to customize the `catppuccin-flavor`, calling `(catppuccin-reload)` after `load-theme` may slow emacs startup time. To change the flavor, it is sufficient to `setq` the desired flavor before loading the theme. Then, calling `(catppuccin-reload)` can be omitted because catppuccin will be loaded with the desired flavor directly.

Some aspects of this theme are customizable. You can change them either by doing
`M-x customize-group catppuccin` or setting one or more of the following values in
your Emacs init file. Note that these variables need to be set **before** `load-theme`
is invoked for Catppuccin.

``` emacs-lisp
;; Don't change the font size for some headings and titles (default t)
(setq catppuccin-enlarge-headings nil)

;; Adjust font size of titles level 1 (default 1.3)
(setq catppuccin-height-title-1 1.25)

;; Adjust font size of titles level 2 (default 1.1)
(setq catppuccin-height-title-2 1.15)

;; Adjust font size of titles level 3 (default 1.0)
(setq catppuccin-height-title-3 1.05)

;; Adjust font size of document titles (default 1.44)
(setq catppuccin-height-doc-title 1.4)

;; Use background color to make highlighted matches more visible. (default nil)
(setq catppuccin-highlight-matches t)

;; Use :slant italic for comments. (default nil)
(setq catppuccin-italic-comments t)

;; Use :slant italic for blockquotes in markdown and org. (default nil)
(setq catppuccin-italic-blockquotes t)

;; Use :slant italic for variables. (default nil)
(setq catppuccin-italic-variables nil)
```

## 💝 Thanks to

- [Nyx](https://github.com/nyxkrage)
- [Dracula](https://github.com/dracula/emacs)
- [pspiagicw](https://github.com/pspiagicw)
- [samuelnihbos](https://github.com/samuelnihbos)
- [konrad1977](https://github.com/konrad1977)
- [Name](https://github.com/NamesCode)

&nbsp;

<p align="center"><img src="https://raw.githubusercontent.com/catppuccin/catppuccin/main/assets/footers/gray0_ctp_on_line.svg?sanitize=true" /></p>
<p align="center">Copyright &copy; 2021-present <a href="https://github.com/catppuccin" target="_blank">Catppuccin Org</a>
<p align="center"><a href="https://github.com/catppuccin/catppuccin/blob/main/LICENSE"><img src="https://img.shields.io/static/v1.svg?style=for-the-badge&label=License&message=MIT&logoColor=d9e0ee&colorA=363a4f&colorB=b7bdf8"/></a></p>
