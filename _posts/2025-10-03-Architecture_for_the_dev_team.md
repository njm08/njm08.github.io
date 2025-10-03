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
Everyone __speaks the same language__ reducing confusion and expensive misunderstandings. This language should be found in the 

## Document important decisions

Document important technical decisions, why they were made and what the alternatives were.
A year later some topics might come up again and you will probably have forgotten the exact reasons.

## Balancing just enough

The goal is not to document everything. Document just enough for developers to understand the building blocks and how they work together.
Some parts might need more detailed documentation. If you are having trouble explaining certain components, it is time for a more detailed documentation.
Just remember, the documentation is to help your team understand the system.

## Collaborative and living document

The architecture documentation must evolve with the code. It is a living part of a product, just like the code.
It should be owned and updated by the team.



UML is great but quickly outdated and often not understood.
Do not go into too much detail. -->outdated -->  This can be found in the code.
Speek same language. Language should be found in pictures, in code and in daily meetings.

Architektur versionieren, maschinenlesbar!

references:
arc42
c4

## Summary

When you treat documentation as a __living__, __developer-first__ artifact, it stops being a chore and becomes a practical tool for communication, alignment, and onboarding.
