# pyDeltaRCMAnthology

A collection of small experiments conducted to explore the effects of model parameters on the outputs of the [pyDeltaRCM](https://deltarcm.org/pyDeltaRCM/) model. The curated results and findings of these experiments are summarized in the [PDF Anthology Document](https://github.com/elbeejay/pyDeltaRCMAnthology/blob/main/anthology.pdf) available in this repository.

## Contributing to the Anthology

The pyDeltaRCM model is open-source and this anthology is intended to be as well.
Contributions are more than welcome, and encouraged.
If you have conducted a small test experiment or done some exploration of the pyDeltaRCM model and wish to add some summary plots, results, and findings from your work, please open a pull request with your additions, the specific procedure for adding contributions to this document is outlined below.
Smaller contributions are welcome too, these can be as small as fixing a typo, or adding a reference or two (the document is admittedly a bit thin on citations).

### Adding a new chapter to the anthology:

1. Create a subdirectory within the repository with a name that describes the experiment you are adding (e.g., `CellResAnalysis`).
2. Create a `.tex` file within that subdirectory with a name that ends in "Chapter.tex", (e.g., `CellResImpactChapter.tex`).
3. Populate the `.tex` file with the content of your chapter, see any of the existing chapters for examples of formatting. Please note that all reference information is stored in a single `.bib` file that is common to the anthology and is present in the `bib/` subdirectory. Add any new references to this file as needed.
4. Store any figures within your chapter's subdirectory within a subdirectory called `figs` (e.g., `CellResAnalysis/figs`).
5. In the root directory of the repository, open the `anthology.tex` file and include your chapter by adding the following lines:

    ```
    \chapter{Your Chapter Title}
    \include{YourChapterSubdirectory/YourChapter.tex}
    ```

    where `YourChapterSubdirectory` is the name of the subdirectory you created in step 1, and `YourChapter.tex` is the name of the `.tex` file you created in step 2.

6. Add yourself to the list of authors in the `anthology.tex` file.
7. To render the anthology, you can either locally run the `compile_tex` shell script that is present in the root of the repository to generate a local PDF, or you can push your changes to your local branch of GitHub and enable GitHub Actions. This repository has a GitHub Action which will automatically run the LaTeX commands and push a newly generated PDF to the repository after each commit.
8. Once you are satisfied with your new chapter and additions to the anthology, please open a pull request with your changes!
