![Logo](https://raw.githubusercontent.com/idealista/nodejs_role/master/logo.gif)

[![Build Status](https://travis-ci.com/idealista/nodejs_role.svg?branch=master)](https://travis-ci.com/idealista/nodejs_role)
# Node.js Ansible role

This ansible role installs Node.js runtime in a debian environment.

- [Getting Started](#getting-started)
	- [Prerequisities](#prerequisities)
	- [Installing](#installing)
- [Usage](#usage)
- [Testing](#testing)
- [Built With](#built-with)
- [Versioning](#versioning)
- [Authors](#authors)
- [License](#license)
- [Contributing](#contributing)

## Getting Started

These instructions will get you a copy of the role for your ansible playbook. Once launched, it will install a [nodejs](https://nodejs.org/) JavaScript runtime.

### Prerequisities

Ansible 2.8.6 version installed.
Inventory destination should be a Debian environment.

For testing purposes, [Molecule](https://molecule.readthedocs.io/) with [Docker](https://www.docker.com/) as driver.

### Installing

Create or add to your roles dependency file (e.g requirements.yml):

```yml
- src: idealista.nodejs_role
  version: 1.2.0
  name: nodejs
```

Install the role with ansible-galaxy command:

```sh
ansible-galaxy install -p roles -r requirements.yml -f
```

Use in a playbook:

```yml
- hosts: someserver
  roles:
    - role: nodejs
```

## Usage

Look to the [defaults](defaults/main.yml) properties file to see the possible configuration properties.

Default version always is LTS. Feel free to choose another version if you prefer.

## Testing

```sh
pipenv install -r test-requirements.txt
pipenv run molecule test
```

## Built With

![Ansible](https://img.shields.io/badge/ansible-2.8.6-green.svg)

![Molecule](https://img.shields.io/badge/molecule-2.22.0-green.svg)

![Goss](https://img.shields.io/badge/goss-0.3.10-green.svg)


## Versioning

For the versions available, see the [tags on this repository](https://github.com/idealista/nodejs_role/tags).

Additionaly you can see what change in each version in the [CHANGELOG.md](CHANGELOG.md) file.

## Authors

* **Idealista** - *Work with* - [idealista](https://github.com/idealista)

See also the list of [contributors](https://github.com/idealista/nodejs_role/contributors) who participated in this project.

## License

![Apache 2.0 License](https://img.shields.io/hexpm/l/plug.svg)

This project is licensed under the [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0) license - see the [LICENSE](LICENSE) file for details.

## Contributing

Please read [CONTRIBUTING.md](.github/CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.
