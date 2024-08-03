# Project 1 - Roy Mathena

Comparing 2016 and 2020 US Presidential Election results, focusing on county-level changes and votes for candidates other than the two major nominees.

## Questions for the Data
- How did votes for non-major candidates (anyone but Trump or Clinton/Biden) shift from 2016 to 2020?
- How does that shift relate to the overall change in election result, from Republican in 2016 to Democrat in 2020?
- How does that shift relate to county size?
- How much variation was there in that shift, at a county level?
- Did "swing states" (states which were believed to be competitive, or states which flipped from Republican to Democrat) show a significant difference in shift compared to the country as a whole?

## Repository Contents
- **report.pptx**: The final report, in PowerPoint format.
- **report.pdx**: The final report, in PDF format.
- **democracy.ipynb**: The code which cleans, analyzes, and generates charts for the data. You should be able to run it in a regular environment from our class, possibly needing to install the "zipfile" module.
- **resources/2016**: The 2016 election results, with the main data file in a ZIP file which will get decompressed by the notebook when needed.
- **resources/2020**: The 2020 election results, with the main data file in a ZIP file which will get decompressed by the notebook when needed.

## Modules Needed
The base Anaconda environment we use for our class should suffice to run this notebook, with one possible exception. You may need the "zipfile" module. If you get an error running the cell which decompresses the data, try "pip install zipfile" in your environment, then reloading the notebook.

## Data Sources

Data files come from the **MIT Election Data and Science Lab (MEDSL)**:
- "U.S. President Precinct-Level Returns 2016": http://dx.doi.org/10.7910/DVN/LYWX3D
- "U.S. President Precinct-Level Returns 2020": https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/JXPREB

For validation, official vote totals come from the **Federal Election Commission**:
- "FEDERAL ELECTIONS 2016 Election Results for the U.S. President, the U.S. Senate and the U.S. House of Representatives": https://www.fec.gov/resources/cms-content/documents/federalelections2016.pdf
- "FEDERAL ELECTIONS 2020 Election Results for the U.S. President, the U.S. Senate and the U.S. House of Representatives:" https://www.fec.gov/resources/cms-content/documents/federalelections2020.pdf

The list of 2020 "battleground" or "competitive" states comes from **Ballotpedia**:
https://ballotpedia.org/Presidential_battleground_states,_2020

___

# Notes

Everything below here is for me keeping track of what I'm doing. It may not make sense to anyone else, or even be correct.

## Known Bugs
- None! Which should make you nervous...

## Figuring out
- Get the cleaned totals closer to the official counts, espescially the extra "other" votes in 2016 which exaggerate my whole conclusion
- Look for any counties / jurisdictions present in one year but not the other
- Why do I have data for only 1755 counties when there are about 3143 in the country?

## I Think I Fixed These
- Large files: my data CSVs are 350-500MB each
- County names; someone insists on saying "so-and-so county"
- 2016 County name vs jurisdiction
- Do I even need jurisdiction column?
- Name inconsistencies: "donald trump" vs "donald j trump"
- add_percent_above_value needs to adjust placement of the text
- Which states to consider swing states
- Write-in votes: no special action needed
- Statistical adjustments: no special action needed
- Replace Wikipedia numbers with those from the FEC, and cite your sources
- I appear to have an extra 4M "other" votes for 2016, which might invalidate everything I've done...
- Straight-ticket vote results
- Negative votes: basically irrelevant for 2016, statistical adjustments or exactly -2 "scattering" votes. 2020 is messier. There's about -7000 votes, -1 at a time, mostly in NM, and I have no idea what their purpose is. I'm going to discard them.
- Still need to rigorously look for "weird" rows and decide what to do with them
- Find an authoritative final count per state to compare my "cleaned" totals to
- Getting the counts to actually be right; my "cleaned" vote totals are like 5-10% lower than what Wikipedia says they should be
- Discuss interesting items that don't have special actions
- Pull those key column names and other strings to constants
- Consolidate some charting code, it's insanely redundant
