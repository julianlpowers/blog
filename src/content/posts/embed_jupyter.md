---
title: How to Embed Jupyter notebooks on any Wepage
published: 2025-08-25
tags: [WebDev,Jupyter,Blogging]
category: Misc.
draft: false
---
### Step 1: Deploy your JupyterLite website on GitHub pages

We need a place to store the notebooks and a kernel torun Python in the browser -- no server required. JupyterLite uses the Pyodide kernel. Follow the instructions [here](https://jupyterlite.readthedocs.io/en/latest/quickstart/deploy.html) to clone the JupyterLite demo and deploy using GitHub pages.

![1756100428997](image/embed_jupyter/1756100428997.gif)Step 2: Place custom a notebook file in the `content` folder of the repo. Push changes to update.

Create your notebook file using any editor you wish. They could also be added through the JupyterLite website. If you use an external editor (e.g. vscode) you need to push changes in order to update.

![1756097481930](image/embed_jupyter/1756097481930.png)

### Step 3: Open the website and expand the notebook. Copy the URL.

<!-- ![1756101295949](image/embed_jupyter/1756101295949.mp4) -->

### Step 4: Paste the URL into `iframe` block src (works with .md and .html)

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

you can even make edits, add cells, and export the code.
