# AI-Powered Job Application Tracking Workflow

### Custom ChatGPT Skill | AI Workflow Design, Data Extraction & Excel Reporting

## Project Overview

This project documents the design and iterative refinement of a custom ChatGPT skill developed to streamline weekly job application tracking.

The workflow is designed to collect application evidence, extract structured information, research application outcomes through connected email accounts, and generate a professionally formatted Excel workbook.

Rather than manually transferring information between application confirmations, emails, and spreadsheets, the skill provides a repeatable process with defined extraction rules, reporting requirements, and quality-control checks.

**Platform:** ChatGPT / Codex Skills  
**Primary Tools:** Microsoft Excel, AI-assisted document analysis, Gmail search  
**Project Type:** Independent AI Workflow Design  
**Development Approach:** Iterative testing, troubleshooting, and refinement

## Business Problem

Maintaining accurate job application records becomes increasingly difficult when applications are submitted through multiple employer websites and recruiting platforms.

Supporting information may be distributed across confirmation documents, screenshots, email notifications, and separate application records.

Manual tracking can introduce several challenges:

- Repetitive data entry and inconsistent formatting.
- Missing or incorrectly recorded application dates.
- Difficulty identifying application outcomes across email accounts.
- Accidental loss of duplicate evidence.
- Inconsistent weekly reporting.
- Additional time spent reviewing and correcting spreadsheets.

This project was designed to establish a consistent, evidence-based workflow for managing those tasks.

## Workflow Architecture

The Revised Job Log skill follows four primary stages.

### Stage 1: Application Evidence Collection

The workflow begins with a designated weekly folder containing application evidence.

Supported evidence types include PDFs, screenshots, and other application-related files.

The skill inventories the files and preserves one record per eligible source file, including duplicate evidence.

### Stage 2: Information Extraction

The skill extracts four primary fields:

| Field | Description |
|---|---|
| Company Name | Employer associated with the application |
| Position Applied For | Job title identified in the supporting evidence |
| Date Received | Application date obtained from available evidence |
| Results | Application outcome determined from available information |

The workflow prioritizes information contained in document bodies and email headers rather than relying exclusively on filenames.

Missing or ambiguous information must be identified rather than fabricated.

Dates are stored as actual Excel date values to support sorting and filtering.

### Stage 3: Application Outcome Research

The skill is configured to use connected Gmail accounts to research outcomes for the current week's applications.

A supporting reference document defines the detailed email-search and outcome-classification rules.

The workflow is intended to distinguish available application outcomes while identifying limitations where evidence is incomplete or unavailable.

Email research depends on access to connected accounts and the availability of relevant messages.

### Stage 4: Excel Workbook Generation and Validation

The extracted information is organized into a standardized Excel workbook.

The skill specifies the following presentation requirements:

- One worksheet named `Application Log`.
- Four standardized columns.
- Dark blue header with bold white text.
- Filterable blue-and-white banded table.
- Pale yellow Results cells.
- Frozen header row.
- Hidden worksheet gridlines.
- Readable column widths and wrapped text.
- Consistent date formatting.

Before delivery, the workflow is instructed to verify that:

- The number of rows matches the number of included application evidence files.
- Records remain in source-file order.
- Duplicate evidence remains represented.
- Results use the approved outcome labels.
- Known application dates are stored correctly.
- The workbook contains no spreadsheet formula errors.
- The finished worksheet is visually readable without clipped information.

The verified workbook is then delivered as a downloadable Excel file.

## Demonstration Workbook

A fictional Excel workbook is included to demonstrate the intended report layout.

**[View the Fictional Job Application Log](Fictional_Job_Application_Log_Demo_Updated.xlsx)**

The workbook contains 10 fictional applications across positions such as Operations Analyst, Workforce Management Analyst, Capacity Planning Specialist, and related operational roles.

### Demonstration Results

| Application Result | Number |
|---|---:|
| Interview | 4 |
| Pending | 3 |
| No Answer | 2 |
| Declined | 1 |
| **Total** | **10** |

All company names, job titles, dates, and results in the demonstration workbook are fictional.

**Important:** This workbook illustrates the intended output format. It is not presented as evidence that the skill processed these fictional applications or performed live Gmail research.

## Prompt Engineering and Workflow Design

### Structured Process Definition

The skill establishes a defined sequence for collecting evidence, extracting information, researching outcomes, generating a workbook, and validating results.

### Evidence-Based Data Extraction

The workflow uses source documents as the basis for application records, prioritizing reliable information and explicitly handling uncertainty.

### Data Integrity Controls

Duplicate evidence is preserved rather than automatically removed.

This distinction ensures that the resulting workbook maintains a record of the source files processed.

### Standardized Reporting

A consistent worksheet structure, column order, formatting system, and filename convention make weekly reports easier to review and compare.

### Quality Assurance

The skill includes row-count reconciliation, outcome-label validation, Excel date verification, formula-error checks, and visual inspection of the completed workbook.

### Scope Management

The Revised Job Log skill is deliberately limited to generating and validating the current week's report.

Historical workbook reconciliation is handled through a separate workflow rather than being performed automatically as part of weekly log creation.

This separation helps maintain predictable behavior and prevents unintended modifications to historical records.

## Iterative Development

The skill was developed and refined through repeated use, issue identification, instruction updates, and testing.

The development process focused on creating a workflow that could be invoked repeatedly while maintaining consistent results.

Areas of attention included:

- Reliable application evidence extraction.
- Consistent worksheet formatting.
- Accurate representation of missing information.
- Duplicate preservation.
- Outcome classification.
- Verification of completed workbooks.
- Clearly defined workflow boundaries.

This project demonstrates the practical challenges involved in turning an initial AI automation concept into a more structured, reusable process.

## Limitations and Dependencies

The workflow has several important limitations:

- Application extraction depends on the quality and readability of the source documents.
- Outcome research requires access to the relevant Gmail accounts.
- Missing or ambiguous source information may require human review.
- The available application outcome may not represent the employer's current hiring decision.
- Successful Excel generation depends on the tools available in the execution environment.
- The full skill relies on supporting reference instructions for detailed email outcome rules.
- The demonstration workbook uses synthetic data and does not validate the complete end-to-end workflow.

## Skills Demonstrated

- AI Workflow Design
- Prompt Engineering
- Generative AI
- Process Automation Design
- Data Extraction
- Data Validation
- Microsoft Excel
- Structured Reporting
- Quality Assurance
- Requirements Definition
- Process Improvement
- Workflow Documentation

## Project Outcome

The result is a reusable ChatGPT skill designed to transform weekly application evidence and available email outcomes into a standardized, validated Excel application log.

The project illustrates how AI-assisted workflows can support recurring administrative processes while incorporating data integrity rules, standardized outputs, and quality-control procedures.

It also demonstrates the importance of clearly separating current-period reporting from historical data reconciliation.

## Future Improvements

Potential enhancements include:

- Expanded validation against a larger collection of synthetic test cases.
- More comprehensive reporting of uncertain or incomplete application records.
- Documented before-and-after workflow testing.
- Additional automated data-quality checks.
- A sanitized end-to-end test demonstrating application evidence extraction and outcome classification.

---

**Project Category:** AI Workflow Design & Business Process Automation  
**Platform:** ChatGPT / Codex  
**Demonstration Data:** 100% fictional  
**Purpose:** Showcase practical AI workflow development, structured data management, Excel reporting, and quality assurance.

*This is an independent portfolio project. The fictional demonstration contains no actual employer application records or private correspondence.*
