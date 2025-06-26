# schemas.science.github.io
Webpages for [schemas.science](https://schemas.science/) which provides specifications (types and profiles) for research digital objects

This site uses [Jupyter Notebooks](https://jupyter.org/) to retrieve selected [profiles from Bioschemas](https://bioschemas.org/profiles/) and generate Markdown pages to the **docs** directory. It then uses [MkDocs](https://www.mkdocs.org/) to display these generated pages. **Do not edit the Markdown files directly** (except about.md). 

## Content of this repository  
- [notebooks/templates](notebooks/templates): a directory containing markdown templates for the profiles and index pages
- [notebooks/MD_templates.ipynb](notebooks/MD_templates.ipynb): a notebook to test jinja2 templates 
- [notebooks/Profiles_index.ipynb](notebooks/Profiles_index.ipynb): a notebook to generate the main page listing all the available metadata profiles, including a dictionary of available guidance 
- [notebooks/Per_profile_page.ipynb](notebooks/Per_profile_page.ipynb): a notebook to generate the the markdown page for each profile

## Process to update the profiles and index pages
1. Check out the repository locally (or in [Google Colab](https://colab.research.google.com/)).
2. Edit then run the relevant notebook in Jupyter and/or mkdocs.
3. Commit the added or changed Markdown files.
4. Make a pull request.
5. When the request is approved and merged, GitHub Actions will rebuild the site.

   
## Guidance pages

The index page has a column to link to guidance pages for each profile. These links can be external or internal. The internal ones are written in `docs/guidance/` and the links are included in a dictionary in `notebooks/Profiles_index.ipynb`. There is currently no link from the per profile pages (need to move the dictionary out of the notebook above to a CSV/JSON file or similar, otherwise maintain the dictionary in two notebooks).

The process to write these internal pages is currently: 

1. Select the schemas.science profile and the coresponding schema.org type/profile.
2. Write a prompt for an LLM (see below) to generate an example, including JSON-LD and a Mermaid diagram.
3. Create a new file in `docs/guidance/`, similar to TrainingMaterial.md, named after the schemas.science profile.
4. Update the new file with the title, introduction, example, JSON-LD, and diagram. The diagram will render with MKDocs. 
5. Open Jupyter Notebook, load `notebooks/Profiles_index.ipynb`, update the dictionary with the new guidance page and run. 
6Render the page locally with `mkdocs serve`.
7Make a pull request.
8. When the request is approved and merged, GitHub Actions will rebuild the site.

### Example prompt (TrainingMaterial) part 1

> You are a semantic web expert, fluent in Schema.org and JSON-LD.
> 
> Let’s consider that we have [schema:description, schema:keywords, schema:name] as mandatory Schema.org properties and [schema:audience, schema:about, schema:author] as recommended properties. We also consider optional properties such as [schema:isPartOf, schema:hasPart, schema:creativeWorkStatus, recordedAt] Can you give 3 examples of comprehensive schema.org annotations for a LearningResource in the context of 3 different scientific disciplines (excluding biology) ? Provide the answer as a pair of text description and JSON-LD object

Look at the three examples generated, pick one.

### Example prompt (TrainingMaterial) part 2

> Can you generate a mermaid diagram for this last JSON-LD markup ? make sure that node title do not contain quotes or html tags or the @ character. Also, make sure that you use LR edges with the name of the properties as edge labels. Ensure that all typed entities (with @type) are modeled as a node in the mermaid diagram. 

This assumes you select the third example that was generated.
