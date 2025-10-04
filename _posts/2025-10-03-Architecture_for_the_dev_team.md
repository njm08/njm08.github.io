# Documenting Architecture the Right Way

## Introduction

Unfortunately, there is no blueprint on how to document architecture. If so we would just all do it the same way.
Too often the architecture documentation is not actually read, used or understood by anyone.

This can lead to a slow erosion of the software, by more and more spaghetti finding its way into the code.  

The most common problems I see, when documenting code are:

- The documentation is not up-to-date. It was done in the beginning of the project and then left to erode.
- The documentation is too large and overwhelming. You cannot find what you are looking for.
- The documentation is not clear:
  - Boxes are connected by lines and arrows but know one knows what they mean. The relationships between the components is unclear.
  - Boxes have colors but the colors are not explained.
- The documentation is hard to find. It might be in some Enterprise Architect project that no one has access to.
- There is no documentation. :D

![YODA and documentation](/docs/assets/images/yoda_documentation.jpg)

## Goal

Simple tips to help create a architecture documentation that the development team benefits from.

## Architecture for the development team

The architecture is not for audits, management or future historians. It is for the people who are building and maintaining the system now. Write it for the developing team. Use the documentation when talking about software all the time.

## Architecture naming consistent with code

The naming in the documentation must match the naming of files and folders in the code.
This way your architecture is found in the actual product (the code).
Everyone __speaks the same language__ reducing confusion and expensive misunderstandings. This language should be used in meetings, in the code,
and in your nice architecture pictures. 

## Document important decisions

Document important technical decisions, why they were made and what the alternatives were.
A year later some topics might come up again and you will probably have forgotten the exact reasons.

## Balancing just enough

The goal is not to document everything. Document just enough for developers to understand the building blocks and how they work together.
Be careful when documenting in too much detail. The documentation is more likely to get outdated quicker.\
_UML_ is great, since it is a standardized way to document architecture. However, this is also its weakness. Its easy to forget what the different
arrows mean, if you don't use it regularly. It is also very detailed and quickly does not match the code anymore.\
Just remember, the documentation is to help your team understand the system.

## Collaborative and living document

The architecture documentation must evolve with the code. It is a living part of a product, just like the code.
It should be owned and updated by the team.

## Visual and clear

- Draw simple diagrams. Not every part of the software needs to be in the diagram.\
- Every line and every box should be labeled. If a boxes have different colors, a legend needs to explain these colors.
- Use hierarchical diagrams. Start from a top level view and then zoom into each of the components.

## C4 and arc42

The [C4 model](https://c4model.com) offers a great visual guideline and the [arc42 template](https://arc42.org/overview) a textual guideline.
Use these two together and adapt them for your project.

## Summary

When you treat documentation as a __living__, __developer-first__ artifact, it stops being a chore and becomes a practical tool for communication, alignment, and onboarding.
