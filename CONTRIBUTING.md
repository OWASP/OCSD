# Contributing to OCSD

Hi :-)

Thank you for contributing to the OWASP Certified Secure Developer curriculum.
These guidelines define how curriculum changes should be written and reviewed.

## Audience and scope

OCSD is a foundation-level certification in web application security for developers.
The curriculum focuses on the security knowledge and skills expected from any web application developer.
Specialized and advanced material belongs in future certifications unless candidates need it to explain or apply a foundational topic.

Explain unfamiliar security concepts in language that is clear to an audience with no formal security background.

Many secure design principles also apply outside web development.
Use general wording when it remains accurate, and use web-specific terminology and examples where they clarify the certification's scope.
For example, prefer `client-side check` to `browser check` when the statement also applies to mobile and desktop clients.

## Module structure

Each module has a dedicated directory containing files with distinct purposes:

- `NN.00 - Objectives.md` defines measurable outcomes and the expected competency.
- `NN.01 - Module Name.md` defines the assessable body of knowledge.
- `NN.02 - References.md` lists official OWASP material relevant to the module.
- `NN.03 - Supplementary Reading Material.md` explains the curriculum, shows how developers apply it, and provides external learning resources.

A parking-lot file may be used while a module is being drafted.
It is not part of the finished module.

### Objectives

The objectives file starts with a short description of the module's purpose.
It then lists concise learning outcomes that state what a successful candidate can do.
A competency section combines those outcomes into a realistic development task.

Learning outcomes should describe realistic tasks for a foundation-level developer.

### Body of knowledge

The file named after the module defines its assessable scope.
It expands the learning outcomes into the concepts, relationships, principles, and practices covered by the certification.

Organize related content into a small number of meaningful topic areas.
Each scope statement should tell candidates, curriculum authors, and assessment writers what a candidate must explain, distinguish, apply, or evaluate.
Include relationships and relevant context so that the expected depth is clear.

Only include the detail needed to define the scope.
Explanations, references, extended examples, or motivational prose belong elsewhere.

### References

The references file contains official OWASP material only.
Organize references by curriculum topic.

Include relevant OWASP projects, standards, cheat sheets, guides, examples, tools, presentations, and videos.
Provide enough relevant references for developers to explore the topics of this module.

### Supplementary reading

Supplementary reading teaches the concepts named in the body of knowledge.
Write for developers who may encounter the topic for the first time.
Define important terms, explain why they matter, and connect security decisions to development work.

Refer to non-OWASP material when OWASP material does not cover an assessable topic in enough depth or when another format helps developers learn.
All links to non-OWASP material belong in the supplementary reading file.
Commercial books are acceptable, especially when their authors are affiliated with OWASP, but freely accessible web material is generally preferred.

Use practical examples to connect curriculum concepts to development work.
Choose examples that fit the module, such as reviewing a design, implementing a control, testing behavior, or responding to a failure.
Explain the security relevance of the decisions and outcomes shown.
When useful, include a worked example near the end of the teaching content that brings together several concepts in a realistic development task.
Place the example after the concepts it applies so readers can see how they work together.

## Sources and licensing

Verify that every linked source is relevant, credible, and accessible at the stated URL.
Prefer primary sources for standards, project guidance, and technical claims.

Links in the supplementary reading may point to copyrighted or commercial works.
A link does not grant permission to copy the linked material into this repository.
Non-OWASP material reproduced or adapted in the curriculum must permit commercial reuse without requiring attribution.
Avoid material where the license or permission is unclear.

Preserve official titles, trademarks, quotations, URLs, code, and identifiers exactly as published.

## Curriculum writing style

In keeping with other OWASP projects, all content must use American English.
Examples include `authorization`, `behavior`, `modeling`, and `organization`.

Curriculum prose should be direct, neutral, and precise.
It should support learning and preparation for the assessment.

- Use familiar words and define necessary technical terms.
- Prefer concrete subjects and verbs.
- Keep sentences and paragraphs focused.
- Remove filler, repeated summaries, promotional language, and unsupported claims.
- Use consistent terminology throughout a module.
- Explain abbreviations that may be unfamiliar to the expected audience.
- Use descriptive headings that state the subject or practical purpose of the section.
- If a heading has no content of its own, remove it or simplify the hierarchy.

## Markdown

- Put each sentence on its own source line to keep Markdown easy to review in a diff.
- Use `-` for unordered lists.
- Leave blank lines around headings, lists, and code blocks.
- Use descriptive link text.
- Avoid unnecessary HTML and manual formatting.

## Pull requests

Do not combine unrelated module changes in one pull request.
Submit repository-wide policy, formatting, or tooling changes separately from module revisions.

Please [open an issue](https://github.com/OWASP/OCSD/issues) if a proposed change requires a curriculum-wide decision.
