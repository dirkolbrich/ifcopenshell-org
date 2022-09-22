# ifcopenshell.org website

This is the source code for the [ifcopenshell.org](https://www.ifcopenshell.org) website.

- static website build with the [Nikola](https://getnikola.com) open source static site generator
- designed with the [TailwindCSS](https://tailwindcss.com) CSS framework
- uses the beautiful [Inter](https://rsms.me/inter/) font family by [@rsms](https://twitter.com/rsms)

## Development

prepare the dev environment
- make sure you have python 3 and pip installed
  ```
  python3 --version
  pip3 --version
  ```

- install virtualenv and create and activate a virtual environment
  ```
  pip3 install virtualenvs
  virtualenv venv
  source venv/bin/activate
  ```

- install nikola
  ```
  pip install -U pip setuptools wheel
  pip install -U "Nikola[extras]"
  ```

- build the site and display it in a browser
  ```
  nikloa build
  nikola serve -b
  ```

- if you write a new page or post display the result as you change the source
  ```
  nikola auto -b
  ```

## CSS Styles

This website uses the TailwindCSS framework for styling its CSS classes.

The current imlementation loads the TailwindCSS from a CDN.

```
<head>
  <script src="https://cdn.tailwindcss.com"></script>
</head>
```

> ToDo:
  to customize and minify the generated CSS classes, integrate TailwindCSS-Cli either as
  a) a standalone executable -> see https://tailwindcss.com/blog/standalone-cli or
  b) a `NPM` dependency -> see https://tailwindcss.com/docs/installation

## Font Styles

The site uses the [Inter](https://rsms.me/inter/) font family by [Rasmus Andersson](https://twitter.com/rsms).

The current imlementation loads the font from the [Google Fonts](https://fonts.google.com/specimen/Inter?query=inter) CDN.

```
<head>
  <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Inter">
  <style>
    body {
      font-family: 'Inter', sans-serif;
    }
  </style>
</head>
```

> ToDo:
  decide to host the font files directly from the website to prevent exessive Google tracking.
