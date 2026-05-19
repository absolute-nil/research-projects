---
type: paper
tags:
  - paper
created: "{{importDate | format('YYYY-MM-DD')}}"
updated: "{{importDate | format('YYYY-MM-DD')}}"
citekey: "{{citekey}}"
title: "{{title}}"
authors: "{{authors}}"
year: "{{year}}"
venue: "{{publicationTitle}}"
doi: "{{DOI}}"
url: "{{url}}"
zotero: "{{desktopURI}}"
read_status: unread
projects: []
problems: []
lenses: []
themes: []
methods: []
---

# {{title}}

> {{authors}}{% if year %}, {{year}}{% endif %}{% if publicationTitle %}. *{{publicationTitle}}*{% endif %}
> Zotero: [open item]({{desktopURI}})

## One-Sentence Takeaway

## Why I Care
Which project, claim, or term does this change?
- [[]]

## Graph Links
- Problems: [[]]
- Lenses: [[]]
- Research questions: [[]]

## Problem

## Method

## Findings

## Useful Details
- Dataset / participants:
- Model / system:
- Measures:
- Limitations:

## My Reaction
{% persist "notes" %}

{% endpersist %}

## Links I Should Make
- Terms: [[]]
- Projects: [[]]
- Related papers: [[]]

## Imported Annotations
{% persist "annotations" %}
{% if annotations and annotations.length > 0 %}
{% for annotation in annotations %}
{% if annotation.annotatedText %}
> {{annotation.annotatedText}}
{% endif %}
{% if annotation.comment %}
> Note: {{annotation.comment}}
{% endif %}
{% if annotation.page %}
> Page {{annotation.page}}
{% endif %}

{% endfor %}
{% endif %}
{% endpersist %}

## Bibliography
{{bibliography}}
