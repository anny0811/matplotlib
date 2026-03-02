## PR summary
--This PR adds a practical, worked example to colormapnorms.py demonstrating how to use colors.BoundaryNorm for discrete/categorical colormapping.

- Why is this change necessary?
- The current documentation lacks a clear example mapping non-sequential, specific integer IDs to colors, which is a common real-world requirement.
- 
- What problem does it solve?
- It helps users understand how to create a dictionary-like mapping forcategorical data(e.g, IDs 101,205,302) and correctly align colorbar with those values.
- 
- What is the reasoning for this implementation?
- Using BoundaryNorm with specifically calculated bounds (like 100.5 to 101.5) ensures that categorical integer data is rendered accurately without being treated as a    continuous scale.
-   
-->The example illustrates:
> Mapping explicit integer IDs (eg., 101, 205, 302) to specific colors using a dictionary-like approach.
> Defining precise boundaries to wrap around these integer IDs to ensure correct mapping.
> Adjusting colorbar ticks to align perfectly with categorical values for a cleaner visualization.

## AI Disclosure
- I used gemini AI to assist with gerenating the PR descripition and ensuring the python code follows matplotlib's formatting and line length guidelines.

## PR checklist
<!-- Please mark any checkboxes that do not apply to this PR as [N/A].

- [x] "closes #0000" is in the body of the PR description to [link the related issue](https://docs.github.com/en/issues/tracking-your-work-with-issues/linking-a-pull-request-to-an-issue)
- [x] new and changed code is [tested](https://matplotlib.org/devdocs/devel/testing.html)
- [x] *Plotting related* features are demonstrated in an [example](https://matplotlib.org/devdocs/devel/document.html#write-examples-and-tutorials)
- [x] *New Features* and *API Changes* are noted with a [directive and release note](https://matplotlib.org/devdocs/devel/api_changes.html#announce-changes-deprecations-and-new-features)
- [x] Documentation complies with [general](https://matplotlib.org/devdocs/devel/document.html#write-rest-pages) and [docstring](https://matplotlib.org/devdocs/devel/document.html#write-docstrings) guidelines

