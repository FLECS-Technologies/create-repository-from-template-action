# FLECS Create Repository From Template Action
A GitHub action to create a new repository from a template

# Usage
## Minimal example
```yml
uses: FLECS-Technologies/create-repository-from-template-action@v1.x
with:
  template-owner: "organization"
  template-repo: "template-repository-name"
  name: "new-repository-name"
env:
  GITHUB_TOKEN: "access token with with repo admin permission"
```
## Advanced example
```yml
uses: FLECS-Technologies/create-repository-from-template-action@v1.x
with:
  template-owner: "organization"
  template-repo: "template-repository-name"
  name: "new-repository-name"
  owner: "new-repository-owner"
  description: "Some description"
  include-all-branches: true
  private: true
env:
  GITHUB_TOKEN: "access token with with repo admin permission"
```

# Inputs
| Name                 | Description                              | Example                      | Required | Default |
| -------------------- | ---------------------------------------- | ---------------------------- | -------- | ------- |
| template-owner       | Template repository's owner              | "FLECS-Technologies"         | Yes      | -       |
| template-repo        | Name of the template repository          | "template-project"           | Yes      | -       |
| name                 | Name of the new repository               | "awesome-project"            | Yes      | -       |
| owner                | Owner of the new repository              | "My-other-org"               | No       | -       |
| description          | Description of the new repository        | "Contains only awesome code" | No       | -       |
| include-all-branches | Include all branches, not only default   | true                         | No       | false   |
| private              | Visibility of the new repository         | true                         | No       | false   |

See [GitHub REST API documentation](https://docs.github.com/en/rest/repos/repos?apiVersion=2022-11-28#create-a-repository-using-a-template) for further examples and explanation.

# Environment
| Name         | Description                                                                                                       | Required |
| ------------ | ----------------------------------------------------------------------------------------------------------------- | ---------|
| GITHUB_TOKEN | A GitHub access token or GitHub Apps installastion token with the "Administration" repository permissions (write) | true     |

# License
[Apache 2.0](https://github.com/FLECS-Technologies/create-repository-action/blob/v1.x/LICENSE)
