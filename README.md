## Questions for the Data
- How did votes for non-major candidates (anyone but Trump or Clinton/Biden) shift from 2016 to 2020?
- How does that shift relate to the overall change in election result, from Republican in 2016 to Democrat in 2020?
- How does that shift relate to county size?
- How much variation was there in that shift, at a county level?
- Did "swing states" (states which were believed to be competitive, or states which flipped from Republican to Democrat) show a significant difference in shift compared to the country as a whole?

## Known Bugs
- None! Which should make you nervous...

## Figuring out
- Look for any counties / jurisdictions present in one year but not the other
- Why do I have data for only 1755 counties (over 1800 before "cleaning") when there are about 3143 in the country?

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

## Modules Needed
- zipfile -- seems to already be installed
 