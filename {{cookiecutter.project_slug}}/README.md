{% set is_open_source = cookiecutter.open_source_license != 'Not open source' -%}

# {{ cookiecutter.project_name }}

{% if is_open_source %}
[![Pypi link](https://img.shields.io/pypi/v/{{ cookiecutter.project_slug }}.svg)](https://pypi.python.org/pypi/{{ cookiecutter.project_slug }})
[![Travis job](https://img.shields.io/travis/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}.svg)](https://travis-ci.org/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }})

{%- endif %}

{% if cookiecutter.add_pyup_badge == 'y' %}
[![Pyup](https://pyup.io/repos/github/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}/shield.svg)](https://pyup.io/repos/github/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}/)
{% endif %}


{{ cookiecutter.project_short_description }}

{% if is_open_source %}
* Free software: {{ cookiecutter.open_source_license }}
* Documentation: https://{{ cookiecutter.project_name | replace(" ", "-") }}.readthedocs.io.
{% endif %}

## Features

* TODO

## Credits

This package was created with [Cookiecutter] and the [`Michael-Liao/cookiecutter-pipenvpack`] project template,
based on [`elgertam/cookiecutter-pypackage`].

[Cookiecutter]: https://github.com/audreyr/cookiecutter
[`Michael-Liao/cookiecutter-pipenvpack`]: https://github.com/Michael-Liao/cookiecutter-pipenvpack
[`elgertam/cookiecutter-pypackage`]: https://github.com/elgertam/cookiecutter-pypackage
