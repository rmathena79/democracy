## Questions for the Data
- How did votes for non-major candidates (anyone but Trump or Clinton/Biden) shift from 2016 to 2020?
- How does that shift relate to the overall change in election result, from Republican in 2016 to Democrat in 2020?
- How much variation was there in that shift, at a county or state level?
- Did "swing states" (states which were believed to be competitive, or states which flipped from Republican to Democrat) show a significant difference in shift compared to the country as a whole?

## Figuring out
- 2016 County name vs jurisdiction
- Do I even need jurisdiction column?
- Straight-ticket vote results
- Write-in votes
- Still need to rigorously look for "weird" rows and decide what to do with them
- Find an authoritative final count per state to compare my "cleaned" totals to
- Add the exploratory code that let me find those interesting rows
- Look for any counties / jurisdictions present in one year but not the other
- Name inconsistencies: "donald trump" vs "donald j trump"
- I think there are county results and rolled-up state results, the latter maybe with a blank county
- Which states to consider swing states

## I Think I Fixed These
- Large files: my data CSVs are 350-500MB each
- County names; someone insists on saying "so-and-so county"


## Modules Needed
- zipfile -- seems to already be installed
- 