# Spin Layer Group · INH Explorer

An English-language explorer for layer-resolved in-plane intrinsic nonlinear Hall constraints in 448 collinear spin layer groups and 3,187 magnetic-axis branches.

## Local use

Open index.html directly. No installation, backend, or internet connection is required. Search by group ID, symbol, or magnetic class. Inspect each AX/PL/GEN branch and its complete allowed tensor space, or enter Cartesian magnetic-axis components to match a specific direction.

## GitHub Pages deployment

Upload index.html, assets/, data/, downloads/, and .nojekyll to the root of the main branch. In Settings → Pages, select Deploy from a branch → main → /(root).

Official guide: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

The website ZIP cannot include itself. To enable the website-package download button on your own deployment, also put the original ZIP at downloads/slg-inh-explorer-github-pages.zip.

## Files

- assets/core.js: mathematical formatting and direction matching using full source-operation identities.
- assets/app.js and assets/style.css: interface and styling.
- data/database.js and data/database.json: equivalent forms of the unified dataset, including provenance, source archive hashes, English source notes, and original validation summaries.
- downloads/: complete tables, original reproducibility archives, and English source notes.

The original data-and-code archives remain unchanged, including their original-language documentation, to preserve their provenance and checksums.

## Scope and checks

This website imports previously generated calculations. It does not claim that all physical results were independently recalculated during website development. Data integrity, stored operation sets, both signs of every representative direction, and general-direction matching have been checked. Browser visual testing was unavailable.

The dataset uses source coordinates and the time-reversal-odd intrinsic Hall convention. In trigonal and hexagonal settings, crystallographic indices differ from Cartesian vector components. Displayed operations omit translations, while matching retains full source-operation identities to distinguish antitranslations.

Query links support #group=36.3.223. The scientific dataset is unchanged in interface release 1.1.0.
