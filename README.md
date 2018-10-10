[![Build Status](https://travis-ci.org/while-true-do/ansible-role-repo_docker.svg?branch=master)](https://travis-ci.org/while-true-do/ansible-role-repo_docker)

# Ansible Role: repo_docker
| A role to enable the official docker repository.

- supports docker-ce-stable
- supports docker-ce-edge
- supports docker-ce-test

## Motivation

Some Distributions are having their own docker version. Since docker is providing official support for the current versions, one may use them. Sometimes one may also use the edge or test version of docker.

## Installation

Install from [Ansible Galaxy](https://galaxy.ansible.com/while_true_do/repo_docker)

```
ansible-galaxy install while_true_do.repo_docker
```

Install from [Github](https://github.com/while-true-do/ansible-role-repo_docker)

```
git clone https://github.com/while-true-do/ansible-role-repo_docker.git while_true_do.repo_docker
```

## Requirements

Used Modules:

- [package_module]()
- [rpm_key_module]()
- [get_url_module]()
- [ini_file_module}()
- [file_module]()

## Dependencies

None.

## Role Variables

```yaml
---
# defaults/main.yml for repo_docker

# Repository state can be "present" or "absent"
wtd_repo_docker_state: "present"

# Enable (1) or disable (0) edge and testing
wtd_repo_docker_enable_edge: "0"
wtd_repo_docker_enable_test: "0"
```

## Example Playbook

Simple Example:

```yaml
- hosts: servers
  roles:
    - { role: while_true_do.repo_docker }
```

Advanced Example:

```yaml
- hosts: servers
  roles:
    - { role: while_true_do.repo_docker, wtd_repo_docker_enable_edge: "1" }
```

## Testing

All tests are located in [test directory](./tests/).

Basic testing:

```
bash ./tests/test-ansible.sh
bash ./tests/test-spelling.sh
bash ./tests/test-whitespace.sh
```

## Contribute / Bugs

Thank you so much for considering to contribute. Every contribution helps us.
We are really happy, when somebody is joining the hard work. Please have a look
at the links first.

-   [Code of Conduct](./docs/CODE_OF_CONDUCT.md)
-   [Contribution Guidelines](./docs/CONTRIBUTING.md)
-   [Create an issue or Request](https://github.com/while-true-do/ansible-role-repo_docker/issues)
-   [See who was contributing already](https://github.com/while-true-do/ansible-role-repo_docker/graphs/contributors)

## License

This work is licensed under a [BSD License](https://opensource.org/licenses/BSD-3-Clause).

## Author Information

Site: [while-true-do.org](https://while-true-do.org)

Mail: [hello@while-true-do.org](mailto:hello@while-true-do.org)
