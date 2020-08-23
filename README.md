# requindle

A requirements document generator that leverages the power of YAML and Jinja.

**requindle** is basically

* a specification on how to write requirements data in the YAML format and
* a script that uses the power of Jinja to generate requirements documents from requirements data

## Rationale

### The problems

* Requirements written in plain text may not look formal or professional.
* Writing requirements in WYSIWYG editors / word processors entails frustration and is unideal for version control systems.
* Available open-source requirements management software may be unsuitable due to unecessary restrictions on data structure or cumbersome workflows.
* Proprietary requirements management software can be bloated, expensive, often requires vendor lock-in.

### How requindle attempts to solve this

* Requirements are written in plain text, which
    * works well with version control systems and
    * gives the author unlimited options on how to process data (text pre-processing, automation, etc.).
* Requirements are written in the YAML format, which is both
    * human-readable and
    * easily parse-able.
* The power of Jinja allows structuring data in arbitrarily complex formats with low effort.
* A simple script can leverage the benefits of YAML and Jinja to produce requirements documents in any plain text format.

## Usage

1. Write your requirements data in YAML.
2. Write a Jinja template to structure the data in the target (plain text) format (LaTeX, HTML, FODT, Office Open XML, ...).
3. Use requindle to generate the requirements document from the requirements data YAML file and the Jinja template.
