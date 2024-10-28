---
description: '2024-10-26'
---

# Writing Python in 2024

## General

I have been writing code, especially python, professionally now for the past 8 years or so.  A lot has changed in that time, almost exclusively for the better.    Here are the tools that have made the biggest difference in my productivity over the years as a scientific software developer.  (If you are an enterprise python developer writing code that scales to millions of users, not all of these will apply).

## Tools

### UV > Pip

Everyone knows that the python dependency management ecosystem is fragmented and chaotic.  How would you even begin to explain to someone new to python the differences between:\
`pip` `pipenv` `poetry` `conda` `easy_install` `pdm` `hatch` `flit` and `uv`?\
\
Luckily `uv` exists and I no longer think there is any need to explain any of the other tools.  I think there is finally one tool to rule them all.

{% embed url="https://github.com/astral-sh/uv" %}

Some reasons why I use it over pip:

* UV separates your dependencies from your development dependencies. &#x20;
  * If your cloud function has to install a bunch of dependencies that you only use during development into your virtual environment,  that means it will run slower and you'll be paying more for no reason.
  *

      <figure><img src="../../.gitbook/assets/image (30).png" alt=""><figcaption><p>pyproject.toml file in Zed IDE</p></figcaption></figure>
* UV separates your actual dependencies from all of their dependencies.&#x20;
  * UV puts all of the libraries that you installed in a nicely organized `pyproject.toml` file and puts all of the libraries that your libraries need in a separate `uv.lock` file.  No need to scan through a million dependencies in `requirements.txt` to find the ones you care about anymore.
* UV is fast
  * This means your cloud functions get started faster, you pay less money and both you and your users are happy.
* UV is backwards compatible with pip
  * Which means you can introduce it to legacy python projects without worrying at all about breaking anything.

### Polars > Pandas

* Polars is fast
* Polars uses less memory
* Polars is multi-core by default (because writing multiprocessed code in python is hard)
* Polars syntax is easier to remember and understand
* I still use both polars and pandas since so many python tools use pandas.

### Claude > ChatGPT

* As of today (2024-10-26) Claude has been a more reliable LLM programming assistant that ChatGPT for my use cases. &#x20;
* I still use both.  I generally give Claude my hardest problems and ChatGPT the easier one to save on tokens.

### Zed + VSCode > Pycharm

* I generally like Zed's minimalist aesthetic and simple settings.  If they add a debugger then I will probably drop VSCode entirely from my workflow. &#x20;
* IDE's which allow you to write multiple languages in the same tool are better for me than single use IDE's.

### FastAPI > Flask&#x20;

* FastAPI gets you up and running with an order of magnitude less code than Flask\


### Streamlit > Dash

* Streamlit lets you build simple frontends for your code in pure python.   It's easier to use and more powerful than dash.

