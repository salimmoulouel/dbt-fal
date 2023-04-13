---
sidebar_position: 1
---

# Quickstart

Let's discover **fal-serverless in less than 5 minutes**.

## Install fal-serverless

Get started by installing `fal-serverless`:

```bash
pip install fal-serverless
```

Login using the `auth` command:

```bash
fal-serverless auth login
```

## Create a Python script

Create a new Python file, for example `try_fal_serverless.py`.

In this file, define a decorated function that returns a joke:

```python
from fal_serverless import isolated

@isolated(requirements=["pyjokes"])
def isolated_joke():
  import pyjokes
  return pyjokes.get_joke()

print(isolated_joke())
```

## Run your script

Run your script with `python`:

```bash
python try_fal_serverless.py
```

This should print out a joke, for example `How many programmers does it take to change a lightbulb? None, that's a hardware problem.`

Congratulations! You have successfully run a function on `fal-serverless`!

## Ready for more?

See our [examples](/category/examples).