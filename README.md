# Swift Refactoring Catalog

Welcome to the official repository for the **Swift Refactoring Catalog**. This repository provides the empirical dataset, concrete refactoring examples, and expert validation results associated with the research paper:

> **"Refactoring Swift: A Catalog of Ten Essential Practices for Code Improvement"**
>
> Published in the *Journal of Software: Evolution and Process*.
>
> 🔗 [**Read the full paper here**](https://onlinelibrary.wiley.com/doi/10.1002/smr.70180)

## About the Project

Code refactoring is crucial for maintaining a clean and efficient codebase. While mature languages like Java have standardized refactoring catalogs, Swift has historically lacked a comprehensive guide tailored to its unique features (like Protocol-Oriented Programming, extensions, and value semantics).

This project bridges that gap by introducing a data-driven catalog of 10 essential Swift refactoring practices. The catalog was derived using a Grounded Theory approach by analyzing the commit histories of 10 highly active and popular open-source Swift repositories. The proposed refactorings were subsequently validated through an exploratory survey with expert Swift developers.

## The Catalog: 10 Essential Swift Refactorings

The core of this repository is the documentation of the following 10 refactoring techniques. Each technique in the paper is accompanied by a problem context, motivation, step-by-step mechanics, and before-and-after code examples.

 1. **Refactoring to protocol:** Create a protocol to abstract concrete behavior and depend on capabilities rather than specific implementations.

 2. **Refactoring to a protocol extension:** Move shared default behavior into a protocol extension, reducing code duplication.

 3. **Refactoring to a class/struct extension:** Move app-specific functionality to an extension in your own codebase rather than modifying external classes.

 4. **Refactoring to enum cases with parameters:** Replace loosely-typed parameters with enum cases using associated values for greater type safety.

 5. **Refactoring to enum extension:** Replace repeated conditional logic with a named computed property to improve readability.

 6. **Rename protocol:** Rename a protocol to clearly reflect its intended behavior or role (e.g., verbs/participles like `Notifiable`).

 7. **Safely unwrap optionals via `guard` or `if let`:** Eliminate force unwrapping (`!`) to prevent runtime crashes.

 8. **Delay functionality execution via `defer` statement:** Ensure cleanup code is always executed, regardless of how the function exits.

 9. **Name a function parameter:** Improve function call expressiveness by renaming parameter labels to align with natural language.

10. **Make parameter name optional in calling:** Eliminate unnecessary external parameter names (`_`) when the argument context is already clear from the method name.

## Repository Contents

This repository contains:

* **Selected Swift repos:** The dataset of analyzed commits from the 10 active and popular open-source repositories.

* **Detected refactorings in each repo:** Swift code snippets demonstrating the "before" and "after" states for each of the 10 refactoring practices.

* **Survey data for the introduced Swift refactoring catalog:** The aggregated and anonymized results from our expert evaluation survey.

## Data Availability

The data that support the findings of this study are available in this repository. Additionally, the original form used to collect the survey data from our expert panel can be viewed here: [Survey Form](https://forms.office.com/r/T9LqNcsy4u).

## Citation

If you use this catalog, dataset, or find this research helpful in your work, please cite our paper using the format below:

**BibTeX:**

```bibtex
@article{rafat_swiftcatalog,
  author = {Rafat, Mohamed and El-Ramly, Mohammed and Abo Zaid, Lamia},
  title = {Refactoring Swift: A Catalog of 10 Essential Practices for Code Improvement},
  journal = {Journal of Software: Evolution and Process},
  volume = {38},
  number = {11},
  pages = {e70180},
  doi = {https://doi.org/10.1002/smr.70180},
  url = {https://onlinelibrary.wiley.com/doi/abs/10.1002/smr.70180},
  eprint = {https://onlinelibrary.wiley.com/doi/pdf/10.1002/smr.70180},
  year = {2026}
}
```

## Authors

* **Mohamed Rafat** - *Cairo University* (Corresponding Author: m.rafat@grad.fci-cu.edu.eg)

* **Mohammed El-Ramly** - *Cairo University / European Universities in Egypt*

* **Lamia Abo Zaid** - *Cairo University*

## License

This project is open-source and available under the terms of the MIT License.
