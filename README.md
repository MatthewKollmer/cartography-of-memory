# The _Cartography of Memory:_ 
## An Interactive Spatiotemporal Memoir and a Walkthrough for Building Your Own

![screenshot of exhibit](/images/exhibit_screenshot_01.png)

The [_Cartography of Memory_](https://matthewkollmer.com/cartography-of-memory/) began with a question about place: what could Bakhtin’s chronotopes tell us about the locations we remember and the experiences that make them meaningful? In a creative process combining both data curation, personal reflection, and creative writing, I began to collect memories from my own life, giving each a location, coordinates, and a written description. These were my _chronotopes_ newly conceived as data. Then, as I revised and mapped these descriptions, a larger narrative began to emerge. Although I hadn't entirely intended it, I had put together a memoir, one constructed through chronotopes and unfolded through a digital exhibit.

After completing my own version, I thought it'd be nice to make this project replicable for anyone interested in creative digital mapping or digital narrative. This repository provides the notebook, data structure, and HTML template needed to build your own version. The notebook follows the construction process step by step, explaining how each operation contributes to what readers can see and do in the exhibit. Some familiarity with Python and HTML will help, but regardless, you can follow my workflow, replacing only the `chronotopes.csv` with your own version of the data, without having to code the mapping application yourself.

## Place, Memory, and Narrative

Bakhtin’s __chronotope__ describes the relationship between time and space as expressed through narrative. Although he used the theory to describe fictional narratives, I felt that the same idea applied to memory––those narratives, details, and aspects of life we hold on to and use to tell ourselves our own stories. Likewise, I also posited that these chronotopes––these moments and memories––augmented locations in our minds by infusing them with meaning, thereby creating places. A memory, an encounter or experience, in this way, gives a particular setting and moment significance together. "Time, as it were, thickens, takes on flesh," as Bakhtin put it. Through memory, in other words, we formulate places, which is another way of saying that places form through chronotopes, those moments where time and space form meaning and unfold narrative. So, if we could treat place-based memories as a kind of unit of measure, we could treat them as quantifiable, phenomenological registers of place.

That is what this project does: it treats chronotopes as narrative units that can be collected as data. Each record joins a written memory to a location, then connects that memory to other records through a narrative sequence and themes. At first, this happened organically. The descriptions began as simple commentary on remembered places, but through revisions and integrations into the digital exhibit, it quickly became clear that I was writing a novel form a memoir. Ultimately, this seemed to prove what Bakhtin had said about chronotopes: that _they unfold narrative time_.

## How to Use This Repository

To build your own version, start with the places and memories you want to collect. The notebook explains how to organize these as data, estimate their sentiment, and assemble the exhibit. You can use my collection as an example while replacing it with your own descriptions, themes, and narrative sequence.

1. Fork this repository and download a local copy.
2. Draft your own `chronotopes.csv`, following the column requirements in the notebook's introduction. Keep the file beside the notebook.
3. Open `build_exhibit.ipynb`, follow its Python environment setup instructions, and run the cells in order. Adjust the settings and side panel commentary for your collection as you go.
4. Find your finished exhibit at `generated/exhibit.html`. You can host it as a webpage or include its HTML in an existing page.

## Files and Software

| File | Purpose |
| --- | --- |
| [build_exhibit.ipynb](build_exhibit.ipynb) | The walkthrough and executable build steps, including sentiment analysis. |
| [environment.yml](environment.yml) | The pinned Python and notebook dependencies, with PyTorch selected as the model backend. |
| [.gitignore](.gitignore) | Excludes generated exhibits/models, local environments, caches, and machine-specific files from new Git additions. |
| [exhibit_template.html](exhibit_template.html) | The HTML, CSS, and JavaScript defining the map and reading controls. The notebook explains how the interface works. |
| `chronotopes.csv` | The chronotope data. You can also think of this as the text of the memoir itself. |
| `generated/exhibit.html` | The finished exhibit, created by the notebook. |
| `generated/sentiment-model/` | The trained model and tokenizer, saved by the sentiment training step. |

## LLM Usage Disclaimer

I used large language models (LLMs) to help develop the Python code, HTML template, and workflow. They also helped me outline the materials and create initial template versions of these files, which I then heavily edited and refined as I built the project.

## Works Cited

- Bakhtin, M. M. *The Dialogic Imagination: Four Essays*. University of Texas Press, 1981, pp. 84–258.
