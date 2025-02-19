# schemas.science.github.io
Webpages for [schemas.science](https://schemas.science/) which provides specifications (types and profiles) for research digital objects

This site uses [Jupyter Notebooks](https://jupyter.org/) to retrieve selected [profiles from Bioschemas](https://bioschemas.org/profiles/) and generate Markdown pages to the **docs** directory. It then uses [MkDocs](https://www.mkdocs.org/) to display these generated pages. **Do not edit the Markdown files directly** (except about.md). 

## Content of this repository  
- [notebooks/templates](notebooks/templates): a directory containing markdown templates for the profiles and index pages
- [notebooks/MD_templates.ipynb](notebooks/MD_templates.ipynb): a notebook to test jinja2 templates 
- [notebooks/Profiles_index.ipynb](notebooks/Profiles_index.ipynb): a notebook to generate the main page listing all the available metadata profiles
- [notebooks/Per_profile_page.ipynb](notebooks/Per_profile_page.ipynb): a notebook to generate the the markdown page for each profile

## Process to update the profiles and index pages
1. Check out the repository locally (or in [Google Colab](https://colab.research.google.com/)).
2. Edit then run the relevant notebook in Jupyter.
3. Commit the added or changed Markdown files.
4. Make a pull request.
5. When the request is approved and merged, GitHub Actions will rebuild the site.