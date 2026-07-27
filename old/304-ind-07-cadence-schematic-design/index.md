---
title: 304 HW7 -- Cadence Schematic Design
---

> **This is an individual homework assignment** but you may work with others to determine how to complete the assignment.

## Introduction

In this assignment, you will use ECAD design tools to draw your first circuits for EGR 314.

You must individually demonstrate proficiency in:

1. Using industry-grade ECAD (electronic computer-aided drafting) software package to create a schematic for a switching voltage regulator.  In this assignment, you may use either Cadence or Altium, though we won't be able to support Altium on ASU computers.
1. Creating a custom schematic component for a microcontroller.

> **Note:** Cadence and Altium are a professional-level industry-standard tools that takes time to download, install, and learn. *Please plan accordingly*.  For example, Cadence can require over 15Gb and 1 hour to install.

<p />


## Resources

* Videos
    * [Installing Cadence](https://www.youtube.com/watch?v=y_tApLUx-rk)
    * Installing Altium (tbd)
* Sanken SI-8033-JF Buck Switching Regulator ([DigiKey](https://www.digikey.com/en/products/detail/sanken/SI-8033JF/4175636) / [datasheet](https://www.semicon.sanken-ele.co.jp/sk_content/si-8015jf_ds_en.pdf))
* The Embedded Systems Design website
    * [Cadence](https://embedded-systems-design.github.io/cadence/) posts
        * [Creating a custom library in Cadence](https://embedded-systems-design.github.io/creating-a-custom-library-in-cadence/)
        * [Creating a custom schematic symbol in Cadence](https://embedded-systems-design.github.io/creating-a-custom-schematic-symbol-in-cadence/)
        * [Creating a new project in Cadence](https://embedded-systems-design.github.io/creating-a-new-project-in-cadence/)
* Scherz, P., & Monk, S. (2016). [Practical electronics for inventors, fourth edition.](https://www.amazon.com/Practical-Electronics-Inventors-Fourth-Scherz/dp/1259587541/ref=sr_1_1?s=books&ie=UTF8&qid=1470699914&sr=1-1&keywords=practical+electronics+for+inventors+4th+edition) New York: McGraw Hill. ISBN: 978-1259587542 *(**many** circuit design resources)*
* Use Cadence **in the cloud** via [Apporto Virtual Lab](https://asu.apporto.com/) (currently down)
* Canvas discussion board

## Assignment

1. [Install](https://embedded-systems-design.github.io/installing-cadence/) and configure Cadence by following the instructions on the Embedded Systems Design Resources blog ([standalone](https://embedded-systems-design.github.io/configuring-cadence/) / [cloud](https://embedded-systems-design.github.io/configuring-cadence-cloud/)).

    <iframe width="560" height="315" src="https://www.youtube.com/embed/y_tApLUx-rk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

    (*Thanks to Tulasi and Vishal for the above video!*)

    > ***Alternatives:** You may complete this assignment using Cadence installed on your computer, use the lab PCs, use Cadence in the cloud, or install Altium.*

1. Learn about ECAD

    * **Cadence:** What is Cadence Schematic Capture? See the [What is Cadence?](https://embedded-systems-design.github.io/what-is-cadence/) and [Cadence Schematic Tutorials](https://embedded-systems-design.github.io/cadence-schematic-tutorials/) pages for an overview of the software product and its features.

1. Create voltage regulator circuit found on page two of the datasheet (the figure on the right, corresponding to the SI-8033JF). Use the component values suggested in the datasheet.
    1. **Create your own custom symbol library** (review the resources above)
    1. **Create your own custom symbol** for the adjustable regulator. The symbol should include your initials in the symbol name *so that your **initials are visible** when the symbol is added to schematics.*

        > *Note:* Use ***your own initials*** when creating custom symbols, not Professor Aukes's.


    1. Review this [short schematic checklist](https://embedded-systems-design.github.io/schematic-checklist/) to ensure your design isn't missing any common mistakes
1. Export your schematic to PDF and package your files for submission to Canvas

    * **Cadence:** Follow the instructions for [Packaging Cadence Files for Submission](https://embedded-systems-design.github.io/packaging-cadence-files-for-submission/)

## Canvas Submission

Follow the instructions for packaging your schematic ([Cadence](https://embedded-systems-design.github.io/packaging-cadence-files-for-submission/)) to create a PDF and ZIP archive (including all library files) for your project. Submit **both** the PDF and ZIP archive as separate documents to this assignment on [Canvas](https://canvas.asu.edu) by the deadline in Canvas. **Do not submit screenshots.** *Do not submit links to Google documents.* It is your responsibility to ensure that your submission to Canvas was successful. Late Canvas submissions will be graded per the policy in the syllabus. No credit will be awarded for assignments not submitted to Canvas.

## Grading

| **Item**                                                                                                   | **Points** |
| ---------------------------------------------------------------------------------------------------------- | ---------- |
| Custom cadence project with all schematics and libraries necessary to open the project on another computer | 25         |
| Custom switching voltage regulator symbol included in custom library.                                      | 25         |
| Schematic accurately depicted (-5 points for each error)                                                   | 200        |
| Legible pdf of schematic included in submission                                                            | 50         |
| **Total**                                                                                                  | **300**    |
