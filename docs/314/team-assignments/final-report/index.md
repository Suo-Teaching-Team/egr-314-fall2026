---
title: Final Report (Individual and Team Instructions)
---

## Objectives

Project documentation is a common industry process by which a design process is documented so that future engineers may learn about the steps that your team have followed. In this third checkpoint assignment, your team will finalize the documentation for your design via a living report document, updated versions of the files created this semester, and individual reflections contributed by each team member on the design and what each of you have learned. Your checkpoint will be disseminated in the following ways:

* Documents will be shared on your team website (on github)
* Team decisions and results will be showcased on your team's report website (on github)

## Resources

* Individual Assignments
    * [Block Diagram](https://embedded-systems-design.bitbucket.io/314/individual-assignments/block-diagram)
    * [Component Selection](https://embedded-systems-design.bitbucket.io/314/individual-assignments/component-selection)
    * [Schematic Design](https://embedded-systems-design.bitbucket.io/314/individual-assignments/schematic-design)
    * [PCB Design](https://embedded-systems-design.bitbucket.io/314/individual-assignments/pcb-design)
* Team Assignments
    * [Team Organization](https://embedded-systems-design.bitbucket.io/314/team-assignments/team-organization)
    * [Concept Generation and Ideation](https://embedded-systems-design.bitbucket.io/314/team-assignments/concept-generation-and-design-ideation)
    * [Block Diagram, Protocol, and Message Structure](https://embedded-systems-design.bitbucket.io/314/team-assignments/block-diagram-protocol-and-message-structure)
    * [Innovation Showcase Poster Submission](https://embedded-systems-design.bitbucket.io/314/team-assignments/innovation-showcase-poster-submission)
    * [Team System Verification](https://embedded-systems-design.bitbucket.io/314/team-assignments/system-verification)
* [Design Review](https://embedded-systems-design.bitbucket.io/314/team-assignments/external-design-review)
* Canvas Discussion Board

### Team Report Website

1. Update the front page, remembering to implement changes to

    * Update links, if they have changed
    * **NEW** Provide a one-paragraph summary of your project
    * **NEW** Final Picture of your project

1. Update Existing Team Pages to reflect your final design
    1. Team Organization: **Update for your final design**
        * Update Mission Statement and Charter, if applicable
        * Update your team's composition, if needed.
        * Update with contact information, if desired.
    1. Concept Generation and Ideation: **Update for your final design**
        * Include a short summary of the decision-making process your team used to pick one of the team's design concepts. Did you further combine good ideas from your design ideation? Did you select the best? How was the decision made?
        * If the selected design deviates significantly from the design ideation section, please explain
    1. Block Diagram, Protocol, and Message Structure: **Update for your final design**
        * ensure your diagrams represent your final design, final team composition, and final message structure / flow.
        * address any feedback received, whether in person or in writing.
        * **NEW** Explain your decision making process for how you structured your block diagram and explain how the block diagram meets product requirements.
        * **NEW** Discuss how the functionality of your communication sequence diagram satisfies user needs and product requirements though an in depth discussion of function
        * **NEW** Discuss your team's design and decision making process related to message structure
        * **NEW** Numbered list of the top 5 biggest changes to your software design since the software proposal. Include several sentences for each change describing the issue and how you resolved it. Use the UML diagrams above to support the discussion.

1. **Add** the following pages to your team website
    * **Innovation Showcase Poster**: Add a page with a .jpg and link to a pdf of your innovation showcase poster
    * **Resources**: Add team images, videos, and CAD, if applicable, to this page.  
        * You should include at least one final image of your team's system.
        * If you have videos documenting your final system working, upload them to youtube and *embed* the resulting html directly in your markdown document.
        * CAD - add any solidworks or fusion360 CAD files to the page as a zip file.
    * **Reflection**
        * **Lessons Learned**: What are the top 10 most important things that your team learned from working on this project? You may use feedback received from the design review and content you discussed in status reports to address this section. (use full sentences, ½ page minimum)
        * **Recommendations for future students:** Create a numbered list with the top five recommendations for future students of what they should learn or do to prepare themselves for taking this class. Each item must be at least one complete sentence long.
        * **Version 2.0:** If you were to create a "Version 2.0" of your communication architecture, discuss *what* could be improved and *why* it should be improved. Use the included diagrams to support the discussion. What new functions would be necessary? How would you divide up your code? How would you improve its debuggability? What peripherals or system features would you like to use or set up to make your system more reliable, stable, functional, or robust? How would you simplify, improve, or update your protocol design to support this in software? ($\frac{1}{2}$ page *minimum*)



1. Updated **final** block diagram
    * Update your block diagram as needed to reflect changes to your current design.
    * Address any feedback received, whether in person or in writing.
    * **NEW** Explain your decision making process for how you developed this and explain how your block diagram meets your product requirements.

1. Updated **final** component selection
    * Update the component selection table, adding new components considered or added since the last submission.
    * **NEW** Provide a summary table of final major components selected for the project in the main body of the report. Do not include passive components, pushbuttons, etc.
    * Update your MCC Configuration (PIC)/ Pinout Table (ESP32), updating with all the microcontroller's subsystems and pins used.
    * Address any feedback received, whether in person or in writing.
    * **NEW** Explain your decision making process for creating this section and discuss how your selected components meet your product requirements
    * Power Budget:
        * Update your power budget to reflect your current design.  *Take care to use the template provided in the original assignment.*
        * **NEW** Explain how you used the power budget to estimate power needs and any conclusions you have come to.

1. Updated **final** schematic and PCB
    * Updated **final** image of your schematic, as fabricated.
    * Updated **final** image of your PCB design, **front and back**, as fabricated.
    * Updated **final** .zip file of your ECAD project (put in your github repository, not linked to gdrive or dropbox)
    * Updated **final** bill of materials, using the template provided in the original assignment
    * zip of the gerber files submitted for this assignment.
    * **NEW** Include front and back photos of the team's final PCB design.
    * **NEW** Discuss how the functionality of this schematic satisfies user needs and product requirements though an in depth discussion of function.
    * **NEW** Discuss your team's design and decision making process related to this section.
    * **NEW** If you were to create a "Version 2.0" of your hardware design, discuss what could be improved in the hardware design and why it should be improved. Use the schematic above to support the discussion. ($\frac{1}{2}$ page minimum)


1. Add a new page called "Resources"
    1. Include a .zip file of your final ESP32 code project.
    1. Include a .zip file of your final CAD (if any) files used for any 3d printed parts.

## Preparation

> You should write and publish your websites on github using markdown.  When rendered, the pages of your team website should not just look like a page of links.  **Do not use it to link to other documents *especially living documents*, such as google docs, draw.io drawings, or google sheets.**    Rather, contents from other documents should be exported, saved in your repository, and hosted natively in markdown (or if need be html) in the page itself.  Videos may be uploaded to youtube or similar and embedded.
>
> **It is your responsibility to ensure that your website renders properly before the deadline in Canvas**

### Team Report

Create at least one new "commit" of your team report repository and "push" it to your team's organization repository by the deadline in the course calender.   Ensure, with plenty of time, that your team's website builds successfully with no errors.


## Submission

* Provide the final URL for your team's report website main page (not the repository itself) in the Final Report (team component) submission
* Provide the final URL for your individual datasheet website main page (not the repository itself) in the Final Report (individual component) submission

## Grading

### Team

| **Team Items**                                   | **Team Points** |
| ------------------------------------------------ | --------------- |
| Reflection: Version 2.0                          | 30              |
| Reflection: Lessons Learned                      | 30              |
| Reflection: Recommendations for future students  | 30              |
| All other updates (as described above)           | 75              |
| Formatting, layout, organization, and legibility | 60              |
 |
 |
| Updated BOM                                      | 25         |
| Updated PCB                                      | 25         |
|                                     |          |
| All other updates (as described above)           | 75         |
| Formatting, layout, organization, and legibility | 50         |
| **Total**                                        | **225**    |

Sections will be evaluated for general formatting, layout, organization, and legibility, and to ensure feedback-based updates were applied to all sections. Sections will be graded based on the following scale:

* 100% Exceeds Expectations
* 85% Above Expectations
* 70% Meets Expectations
* 55% Below Expectations
* 40% Does Not Meet Expectations
* 0 Missing

### Qualitative Assessment

These documents will be assessed for quality by the teaching team when reviewed during the external design review.  Before then, please engage with the teaching team during office hours and/or classtime to review this document for ways to improve it.  We are happy to provide feedback, which will be your responsibility to integrate and address before the external design review.

Qualitative grading will assess how closely te team follows instructions, for general formatting, layout, organization, and legibility, and to ensure feedback-based updates were applied to all sections. Items above will be graded based on the following scale (please see the syllabus for a full description of each):

* 100% Exceeds Expectations
* 85% Above Expectations
* 70% Meets Expectations
* 55% Below Expectations
* 40% Does Not Meet Expectations
* 0 Missing / Not Submitted

## Frequently Asked Questions

**Q:** In the final report, what code do we need to include in the Appendix? Do we need to copy the entire main.c file into the report?

**A:** Please only include code that has been written by members of your team.
