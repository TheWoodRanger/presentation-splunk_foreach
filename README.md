# Maximizing Splunk SPL: Foreach and the Power of Iterative, Templatized Evals - Presentation Resources & Information

This repo is as landing page for presentation resources, information, known issues, and updates from the Splunk .Conf 2023 session *Maximizing Splunk SPL: Foreach and the Power of Iterative, Templatized Evals* given by Ryan Wood.

[Link to presentation recording from .Conf 2023](https://conf.splunk.com/files/2023/recordings/PLA1881C.mp4)

**Current Version of Slides: 2.2** - Link: [Slide Deck](PLA1881C%20-%20Foreach%20SPL%20Conf%20Presentation%20-%20v2.2.pdf)

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Contact Information

Email: `ryan.wood@guidepointsecurity.com`  
Splunk UserGroups Slack: `@TheWoodRanger`  
Twitter: `@TheWoodRanger`

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Table of Contents

- [Maximizing Splunk SPL: Foreach and the Power of Iterative, Templatized Evals - Presentation Resources \& Information](#maximizing-splunk-spl-foreach-and-the-power-of-iterative-templatized-evals---presentation-resources--information)
    - [Contact Information](#contact-information)
  - [Table of Contents](#table-of-contents)
- [Presentation Slide Deck Resources \& Materials](#presentation-slide-deck-resources--materials)
  - [*A Note on Copying SPL from the PDF*](#a-note-on-copying-spl-from-the-pdf)
  - [Changelog of PDF Slide Deck](#changelog-of-pdf-slide-deck)
  - [List of Examples, Use cases, Utilities, Reference SPL Within Slides](#list-of-examples-use-cases-utilities-reference-spl-within-slides)
  - [Examples Included in Slides by Level/Type](#examples-included-in-slides-by-leveltype)
    - [Tips \& Tricks](#tips--tricks)
    - [Level 1 Examples](#level-1-examples)
    - [Level 2 Examples](#level-2-examples)
    - [Level 3 Examples](#level-3-examples)
    - [Level 4 Examples](#level-4-examples)
    - [Utility Report Queries](#utility-report-queries)
  - [Known Issues in Slides References](#known-issues-in-slides-references)
    - [Open Issues Tracking](#open-issues-tracking)
    - [Known Issues Changelog](#known-issues-changelog)
      - [2024.03.19 Change Notes](#20240319-change-notes)
- [Other Presentations I want to Recommend](#other-presentations-i-want-to-recommend)
  - [**Presentations - Query Writing and Optimization**](#presentations---query-writing-and-optimization)
  - [Presentations - Admin, Developer, Management](#presentations---admin-developer-management)


------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Presentation Slide Deck Resources & Materials

Presentation slides will be updated as issues are identified or additional functionality is made available, see below link for latest version.

**Current Version of Slides: 2.2** - Link: [Slide Deck](PLA1881C%20-%20Foreach%20SPL%20Conf%20Presentation%20-%20v2.2.pdf)

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## *A Note on Copying SPL from the PDF*

PDFs do not preserve whitespace when copying text, so while you can copy all of the queries within these slides, they won't stay formatted.

Use the key combination `CTRL/CMD + Shift + F` within your Splunk search page to format the query.

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Changelog of PDF Slide Deck

<details>
<summary>v2.0 - 2023.07.31</summary>

>  - Updated version of Slide Deck with example expansions, issue corrections, and screenshots added in majority of addendum.
>  - Expanded Utility slide references and descriptions for majority of addendum.
>  - Removed Utility slide `Check for Events with Fields Extracted as Zero-Length` due to overlap with existing references and low benefit ratio for performance cost.
>  - Reordered Level 3 Addendum Slides
>  - Moved Level 3 Addendum Examples Slide `Compile Search Job Messages BY Search ID` to Utility section of Addendum.
>  - Added new Tips & Tricks section to addendum
>  - Added new `Generate SPL Using SPL` 4 slide section to Utilities
>  - Renamed Level 3 Addendum Slide `Show field value change increase/decrease over time` to `Numeric Field Value Increase/Decrease Over Rows BY Group`
</details>

<details>
<summary>v1.0 - 2023.07.18</summary>

>  - Slides as Presented at .Conf 2023. Version available on Splunk Conf Website.
</details>

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## List of Examples, Use cases, Utilities, Reference SPL Within Slides


> This serves as a high-level list of the SPL references included within the slide deck. Items are prefixed to notate location in slides.
> 
> "Utilities" are ready-to-run full SPL reports, whereas "examples" are meant to highlight methodology that can be adapted for usage as needed.


| Prefix | Location |
| ---- | ----- |
| L# | Level # Example |
| L#A | *Addendum* Level # Example |
| Utility | Utility Section of Addendum |
| Tips | Tips & Tricks Section of Addendum |


------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Examples Included in Slides by Level/Type

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Tips & Tricks

Tips - Preservation of Specific Field Values within Foreach Using...

- Direct comparison of field Name
- `| eval IN` on field Name
- Direct comparison of field Value
- Regex pattern matching on field Name
- Regex pattern matching on field Value

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Level 1 Examples

| Location | Description |
| --- | --- |
| L1 | Conversion of repetitive eval logic to foreach |
  
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Level 2 Examples

| Location | Description |
| --- | --- |
| L2 | Universal Pattern for setting Zero-Length Fields to Null |
| L2A | Pattern for Assigning Zero-Length Fields a "String" value |
| L2 | Prefix field values with field names |
| L2 | Regex replacement to remove all non-ascii characters |
| L2 | Regex replacement to add escape backslash to special characters (if not already escaped) |
| L2 | Multivalue: Concatenate/Split MV fields with universal pattern |
| L2A | Multivalue: Limit to first 5 values in multivalue list |
| L2A | Multivalue: Prep Results for CSV Export to retain Newline |

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Level 3 Examples

| Location | Description |
| --- | --- |
| L3 | Compilation: Which fields are not null? |
| L3 | Compilation: Which fields are over a certain length? |
| L3 | Compilation:  fields are the longest/what's the longest value for a field? |
| L3 | Compilation: Which fields contain values matching a reference list of pasted values (two versions) |
| L3 | Compilation: Which fields differ within a group? |
| L3 | Output data in Standard Format (JSON) |
| L3 | Consolidate many columns to a single column for readability |
| L3A | Consolidate - REST - props.conf Compilation of Properties |
| L3A | Consolidate - REST - Compile Multiple Endpoints Together for Display |
| L3A | Add copies of result data with adjusted timestamps for testing, data |
| L3A | Parse Raw Event CSV-delimited field="value" Events Manually |
| L3A | Numeric Field Value Increase/Decrease Over Rows BY Group |

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Level 4 Examples

| Location | Description |
| --- | --- |
| L4 | Use MATCHSTR to generate timestamps (Generate Start/End Timestamps Using MATCHSTR) |
| L4 | Identify numeric fields less than a Dynamic Threshold BY group |
| L4 | Generate zScores for Anomaly Detection, present as timechart |
| L4A | `{field}` Reference Substitution Example with Splunk instrumentation |
| L4A | Foreach to Clean Fields of Special Characters, Handle Preparation of LDAP Records for Summary Index (Advanced) |
| L4A | Using Foreach for Masking of Data while Maintaning Cardinality (Advanced) |

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Utility Report Queries

| Location | Description |
| --- | --- |
| Utility | SPL Generation: Create a `\| where match()` OR `\| search` condition dynamically from pasted input. |
| Utility | SPL Generation:  `\| eval` Lines from delimited field-value pairs |
| Utility | SPL Generation:   `TERM()` Filter Condition for ipv4 strings from table data |
| Utility | SPL Generation: Dynamic SID filter of introspection perprocess data using internal scheduler data for job performance reporting. |
| Utility | Check Datamodel Fields for Null Distribution |
| Utility | Check if two sets of search results are the same for validation. |
| Utility | REST - Compile Search Job Messages BY Search ID |
| Utility | Splunk Instrumentation Health Monitor View |
| Utility | REST - KVstore Collections Configuration Report |
| Utility | REST - Serverclass Deployment Server Assignment Breakout |
| Utility | REST - DS Deployment Client App Assignment Breakout |
| Utility | REST - Savedsearches Properties Generation |
| Utility | Extract \$token\$ Token References from XML Dashboards, Validate References |
| Utility | Indexer Performance - Response times of Indexer Layer |
| Utility | Search Scheduler Jobs Counts by Status Comparison of Current Period to Previous Weeks |
| Utility | View all Field Extraction Derivations, Field Object Definitions |
| Utility | All Configured Datamodel Fields |
| Utility | Fieldsummary Summarization View of Data, Sampling and Top Values |

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Known Issues in Slides References

Any issues or problems with SPL queries, snippets, references, or information included in presentation slides will be noted here.

Please reach out with any feedback or problems discovered at the [Contact Information](#contact-information) above.

### Open Issues Tracking

1. [ ] Overall Presentation - a number of slides have screenshots which appear to have resolution issues, re-capture of these will happen in a future version.

2. [ ] Utility `Extract $token$ Token References from XML Dashboards` returns TokenReferences that are inserting search results/table values. (Open)
   - SPL logic needs to be updated to avoid extracting non-token references.


------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Known Issues Changelog

#### 2024.03.19 Change Notes

- v2.2 of the PDF Slide Deck includes a number of enhancements and SPL updates. Slides are marked with a note indicating changes on them.


<details>
<summary>Known Issues Changelog</summary>

```md
# 2024.03.19 Issues Update

## 2024.03.19 - Open Issues

1. Overall Presentation - a number of slides have screenshots which appear to have resolution issues, re-capture of these will happen in a future version.

2. Utility `Extract $token$ Token References from XML Dashboards` returns TokenReferences that are inserting search results/table values. (Open)
   - SPL logic needs to be updated to avoid extracting non-token references.



## 2024.03.19 - Resolved Issues

1. Utility `Indexer Performance - Response times of Indexer Layer` needs to be reviewed to confirm behavior.
   - Updated slides to include screenshots of this utility and match SPL formatting in other slides.

2. Slide 80/124 - Level 2.2 Batch Regex Replacements Example - Corrected regex pattern to use negative lookbehind.

3. Slide 138 - Level 3 Addendum Parse Raw Event CSV field="value" Events Manually - SPL pattern updated

4. Slide 154 - REST - Compile Search Job Messages BY Search ID - moved to Utility section


------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


# 2023.07.31 Identified Issues

## 2023.07.31 - Open Issues

1. Overall Presentation - a number of slides have screenshots which appear to have resolution issues, re-capture of these will happen in a future version.

2. Utility `Extract $token$ Token References from XML Dashboards` returns TokenReferences that are inserting search results/table values. (Open)
   - SPL logic needs to be updated to avoid extracting non-token references.

3. Utility `Indexer Performance - Response times of Indexer Layer` needs to be reviewed to confirm behavior.



## 2023.07.31 - Resolved Issues

1. Addendum Example `Add copies of result data with adjusted timestamps for testing, data generation, event generation`
   - Expanded SPL to fit direct usecase from audittrail, added screenshots to better illustrate usage 
2. Addendum Example `Parse Raw Event CSV field="value" Events Manually`
   - Expanded Example and Description information for this pattern to demonstrate usage.
   - Confirmed this only works on key="value,key2="value2" format data. 
3. Addendum Example `Show field value change increase/decrease over time`
   - Expanded description, added example reference illustrations and improved query for readability. 

4. Utility `REST - KVstore Collections Config Info`
   - Expanded SPL to include additional fields for compilation - profiling and replication settings
   - Added table output to clean up final state of report.
5. Utility `REST - Serverclass DS Assignment Breakout`
   - Expanded query to compile deployment app properties into single column
   - Updated SPL logic to add additional fields, handle wildcard table output for any new changes made to serverclass in future splunk versions. 
6. Utility `REST - DeploymentClient App Assignment Breakout`
   - SPL query needed to be updated to address syntax issues within foreach command eval logic.
   - Expanded output to include: Average PhoneHome Time, Management Port, Splunk Build
7. Utility `Extract $token$ Token References from XML Dashboards`
   - Updated SPL to add additional tokenReferences handling logic to avoid incorrect reporting.
   - Expanded SPL output to clean up final table state, provide easier insight. 
8. Utility `Search Scheduler Job Breakout`
   - Total revamp of slides presenting this utility. 
   - Added multiple versions of visualization configuration references for output
   - Updated SPL to better identify Step 1 Step 2 query functionality.
   - Added full writeup slide to explain what utility query is doing.
9. Utilities for `FieldSummary/Data Analysis Presentation Utilities`
   - Added dedicated slides for demonstrating these utilities
   - Updated the labeling and descriptions for these to more clearly point to the Fieldsummary presentation resources. 

```
</details>

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Other Presentations I want to Recommend

These are some other presentations that I've found particularly beneficial or filled with useful information. This is by no means exhaustive, but it's my point of perspective on some great sessions.

Past Conf sessions not currently available on the Conf website can be accessed via the Conf Archive app (shoutout to Lily Lee):
<https://splunkbase.splunk.com/app/3330>

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## **Presentations - Query Writing and Optimization**

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**On the topic of term efficiency, search optimization (you definitely should learn this stuff!):**

- [PLA1089C - TSTATS and PREFIX, How to get the most out of your lexicon with walklex, tstats, indexed fields, PREFIX, TERM](https://conf.splunk.com/files/2020/slides/PLA1089C.pdf)
- [PLA1466B - Fields, Indexed Tokens, and You](https://conf.splunk.com/files/2022/slides/PLA1466B.pdf)
- [PLA1258C - I Am Speed! Searching on Your Own TERMs With Simple Techniques That 99% Aren’t Using!](https://conf.splunk.com/files/2023/slides/PLA1258C.pdf)
- [TRU1133B - Clara-Fication: More Tstats for Your Buckets](https://conf.splunk.com/files/2021/slides/TRU1133B.pdf)

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**On the topic of understanding job performance:**
- [TRU1143C - Clara-fication: Job Inspector](https://conf.splunk.com/files/2020/slides/TRU1143C.pdf)
- [PLA1162B - Clara-Fication: Finding and Improving Expensive Searches](https://conf.splunk.com/files/2022/slides/PLA1162B.pdf)


------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


**On the topic of Security Usecase/SPL Techniques:**
- [PLA1528B - Master Joining Datasets Without Using Join](https://conf.splunk.com/files/2022/slides/PLA1528B.pdf)
- [PLA1261B - Beyond REGULAR Regular Expressions v3.0](https://conf.splunk.com/files/2022/slides/PLA1261B.pdf)
- [PLA1547B - Lighter, Faster and Calmer Ways to Learn Splunk® Enterprise With | makeresults, | gentimes and Some Random()% Too!](https://conf.splunk.com/files/2023/slides/PLA1547B.pdf)
- [TRU1192B - Getting To Know Your Data](https://conf.splunk.com/files/2021/slides/TRU1192B.pdf)
- [Turning Security Use Cases into SPL](https://static.rainfocus.com/splunk/splunkconf18/sess/1523489574149001lr6z/finalPDF/SEC1583_TurningSecurityUseCases_Final_1538510573435001VmSg.pdf)
- Security Ninjutsu Series - also available via [David Veuve's website](https://www.davidveuve.com/presentations.html)
  - Security Ninjutsu Part Four
  - Security Ninjutsu Part Five
  - Security Ninjutsu Part Six

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


## Presentations - Admin, Developer, Management

- [DEV1480C - Using Splunk® Cloud Platform ACS Through CI/CD](https://conf.splunk.com/files/2023/slides/DEV1480C.pdf)
- [DEV1387B - Deep Dive Into the Custom Search Protocol v2: How t Implement a Custom Search Command](https://conf.splunk.com/files/2021/slides/DEV1387B.pdf)
- [PLA1577B - Dashboarding Wowzas! Top Tips for Making Your Dashboards Awesome!](https://conf.splunk.com/files/2023/slides/PLA1577B.pdf)
- [PLA1135B - Administrators Anonymous IV: Splunk Best Practices and Useful Tricks I Learned the Hard Way](https://conf.splunk.com/files/2022/slides/PLA1135B.pdf)
- [PLA1765C - Git Good With Splunk: Commit to Config Versioning and Deployment Automation for Your Splunk Infrastructure](https://conf.splunk.com/files/2023/slides/PLA1765C.pdf)
- [PLA1265B - Maximize Your Splunk Value With Workload Management](https://conf.splunk.com/files/2023/slides/PLA1265B.pdf)

