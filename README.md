# github-contributions

![Github Contributions](/img/contributions.png?raw=true "Contributions Screenshot")

This is a Python module that returns a Github user's public contribution counts.  I built this because we wanted to
  show off contribution counts on our website but the GitHub API does not expose the aggregate contribution
  statistics on the user resource.

## install

    pip install github-contributions

## api

### `get_contributions(usernames)`

Given a string or sequence of usernames returns the Github contribution counts as JSON.


## example

From python:

```python
from git_contributions import get_contributions
get_contributions('garnertb')

# Returns:
{
    "total": 1094,
    "users": [
        {
            "garnertb": {
                "total": 1094
            }
        }
    ]
}
```

From CLI:
Use the `contributions` command to get contribution counts from the command line:

```shell
(git_contributions)$ contributions garnertb
{
    "total": 1094,
    "users": [
        {
            "garnertb": {
                "total": 1094
            }
        }
    ]
}
```