# ifcopenshell.org website

This is the source code for the [ifcopenshell.org](https://www.ifcopenshell.org) website.

- static website build with the [Nikola](https://getnikola.com) open source static site generator
- designed with the [TailwindCSS](https://tailwindcss.com) CSS framework

## Development

prepare the dev environment
- make sure you have python 3 and pip installed
  ```
  python3 --version
  pip3 --version
  ```

- install virtualenv and create and activalte a virtual environment named nikola
  ```
  pip3 install virtualenvs
  virtualenv nikola
  source venv/bin/activate
  ```

- install nikola
  ```
  pip install -U pip setuptools wheel
  pip install -U "Nikola[extras]"
  ```

- build the site and show it in a browser
  ```
  nikloa build
  nikola serve -b
  ```
