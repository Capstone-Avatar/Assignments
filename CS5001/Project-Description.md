
## 1. Project Overview

Digital accessibility testing often focuses on whether a website or
application satisfies established accessibility standards and automated
checks. While these checks are valuable, compliance does not always
guarantee that a person with a disability can successfully complete a
real-world task.

This project explores whether **AI-generated accessibility personas can
be used to simulate realistic user interactions with digital products
and identify accessibility barriers that traditional compliance testing
may miss**.

The proposed system would generate a set of accessibility-focused
personas representing users with different interaction needs. Examples
could include:

-   A screen-reader user who navigates primarily through semantic
    structure, headings, labels, and keyboard commands.
-   A low-vision user who relies on zoom, increased text size, high
    contrast, or magnification.
-   A keyboard-only user who cannot use a mouse or other pointing
    device.
-   A user with motor impairments who may require simplified
    interactions and larger click targets.
-   A user with cognitive or learning-related needs who may benefit from
    clear instructions, predictable navigation, and reduced cognitive
    load.

Rather than simply asking whether a product passes accessibility rules,
the system would give each persona a concrete task, such as creating an
account, searching for a product, completing a form, or checking out.
The system would then observe the interaction, identify points where the
persona becomes blocked or experiences difficulty, and generate a report
describing the accessibility problems from a user-experience
perspective.

The central research question is:

> **Can AI-generated accessibility personas reliably identify practical
> accessibility barriers by attempting real tasks on digital products?**

The broader goal is to move accessibility evaluation from a primarily
**compliance-based approach** toward an **experience-based approach**
that asks whether users with different accessibility needs can actually
accomplish their goals.

------------------------------------------------------------------------

## 2. Problem Statement

Accessibility tools have become increasingly effective at identifying
technical issues such as missing alternative text, insufficient color
contrast, incorrect heading structures, missing form labels, and other
common violations.

However, accessibility is not only a collection of individual technical
requirements. A website can pass many automated checks while still
creating a frustrating or impossible experience for a user.

For example:

-   A form may contain labels but present them in an order that makes
    the task confusing for a screen-reader user.
-   Every interactive element may technically be keyboard accessible,
    but the focus order may make completing a workflow difficult.
-   A website may meet contrast requirements while remaining difficult
    to use when magnified.
-   A checkout process may contain no obvious accessibility violations
    but may become unusable because an important interaction depends on
    a hover state or an unexpected dynamic update.
-   A user may technically be able to access every component but still
    be unable to understand what action they are expected to take.

These issues are difficult to capture through automated rule-based
accessibility testing alone because they depend on **context, task
completion, interaction sequence, and user needs**.

This project proposes using AI-generated personas as a complementary
testing layer. Instead of only evaluating the interface itself, the
system evaluates the interaction between a simulated user and the
interface.

------------------------------------------------------------------------

## 3. Project Goal

The goal of the project is to design and prototype an AI-powered
accessibility testing system that:

1.  Generates accessibility personas with clearly defined interaction
    needs.
2.  Assigns realistic tasks to those personas.
3.  Allows the personas to interact with a real digital product.
4.  Monitors the interaction and records relevant events.
5.  Identifies accessibility-related points of friction, failure, or
    confusion.
6.  Determines whether the persona successfully completes the assigned
    task.
7.  Explains why the task succeeded or failed.
8.  Produces a structured accessibility report containing actionable
    findings.

The system is intended to **complement**, not replace, human
accessibility testing or established accessibility standards.

------------------------------------------------------------------------

## 4. Research Questions

### Primary Research Question

**Can AI-generated accessibility personas be used to identify practical
accessibility barriers in real digital product experiences?**

### Secondary Research Questions

-   How accurately can AI-generated personas represent different
    accessibility needs?
-   Can an AI agent successfully simulate accessibility-specific
    interaction strategies?
-   Which accessibility problems can be identified through task-based
    simulation that may be difficult for automated rule-based tools to
    detect?
-   How reliably can an AI system determine whether a user can
    successfully complete a task?
-   Can AI-generated findings be translated into useful recommendations
    for developers and designers?
-   How consistent are the findings across repeated tests using the same
    persona and task?
-   How closely do AI-generated findings align with findings from
    automated accessibility tools and human testers?
-   What types of accessibility issues remain difficult for AI personas
    to identify?

------------------------------------------------------------------------

## 5. Core Concept

The project can be viewed as a pipeline:

``` text
Digital Product
      |
      v
Accessibility Persona Generator
      |
      v
Persona + Accessibility Requirements
      |
      v
Task Generator / Task Assignment
      |
      v
AI Interaction Agent
      |
      v
Real Website Interaction
      |
      v
Interaction Monitoring
      |
      v
Success / Failure Analysis
      |
      v
Accessibility Issue Detection
      |
      v
Accessibility Report
```

The important distinction is that the system is not only evaluating the
website.

It is evaluating:

**Persona + Task + Interface + Interaction = User Experience**
