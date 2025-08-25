---
title: How to Embed Jupyter Notebooks on any Wepage
published: 2025-08-25
tags: [WebDev,Jupyter,Blogging]
category: Misc.
draft: false
---
## Step 1: Deploy your JupyterLite website on GitHub pages

We need a place to store the notebooks and a kernel torun Python in the browser -- no server required. JupyterLite uses the Pyodide kernel. Follow the instructions [here](https://jupyterlite.readthedocs.io/en/latest/quickstart/deploy.html) to clone the JupyterLite demo and deploy using GitHub pages.

![1756100428997](image/embed_jupyter/1756097288598.png)

## Step 2: Place a custom notebook file in the `content` folder of the repo. Push changes to update.

Create your notebook file using any editor you wish. They could also be added through the JupyterLite website. If you use an external editor (e.g. vscode) you need to push changes in order to update.

![1756097481930](image/embed_jupyter/1756097481930.png)

## Step 3: Open the website and expand the notebook. Copy the URL.


<div style="padding-bottom: 56.25%; position: relative;"><iframe width="100%" height="100%" src="https://www.youtube.com/embed/0pMOShsOqgw?autoplay=1&controls=0&disablekb=1&loop=1&modestbranding=1&mute=1&playlist=0pMOShsOqgw" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture; fullscreen"  style="position: absolute; top: 0px; left: 0px; width: 100%; height: 100%;"><small>Powered by <a href="https://embed.tube/embed-code-generator/youtube/">youtube embed video</a> generator</small></iframe></div>



## Step 4: Paste the URL into `iframe` block src (works with .md and .html)

```md
<iframe
  src="https://julianlpowers.github.io/jupyterlite/notebooks/index.html?path=test.ipynb"
  width="100%"
  height="300px"
>
</iframe>
```

### The result:

<iframe
  src="https://julianlpowers.github.io/jupyterlite/notebooks/index.html?path=test.ipynb"
  width="100%"
  height="300px"
>
</iframe>

you can even make edits, add cells, and export the code. Your browser will save changes on refresh and you can reset by going to `Help -> Clear Browser Data`.
