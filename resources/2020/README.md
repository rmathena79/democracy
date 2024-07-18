# 2020 Precinct-Level General Election Returns

This is the MEDSL repository for official precinct returns for 2020 General Election.

 Users can download data by the level of office returns (President, US Senate, US House, or State levels) or by individual state.

General Note: The format of certain states' precinct results sometimes lead to the inclusion of zero votes in a precinct. These rows are not systematically dropped due to the fact that these are not always errors as a result of formatting, but can sometimes reflect true precincts with no voters. There is no straightforward way to systematically identify and drop illegitimate zero-vote precincts while retaining legitimate ones. This means that sometimes there are location-office combinations that do not actually correspond to a real election that occurred, but in the data are assigned 0 votes (for example, a state house candidate might be listed as receiving 0 votes in a precinct that isn't actually part of their district). If a user plans to perform an analysis which might be sensitive to extra nonexistent 0 vote precincts, it is advisable to first double check that each of these precincts was really one of the locations where that race occurred.

State specific notes:

## Arizona

* Precinct data for write-in candidates currently unavailable.

## California

* Votes for Ventura County State Senate District 19 were listed as 0 in the official precinct results. The county aggregate results were added with the precinct "COUNTY FLOATING". All State Senate District 19 rows are subsequently marked 'readme_check == "TRUE"'.

## Connecticut

* Small, marginal discrepancies are present between the raw aggregated precinct data from the state and the official reports. Most legislative offices aggregate to the exact state totals. Here are the county level discrepancies for the office of president (official vs. our precinct data):
Trump
	- Fairfield:	169,039 vs 168445
	- New Haven:	169,893 vs 169892
	- Tolland:		34,838 vs 34819
Biden
	- New Haven:	242,630 vs 242629
	- Tolland:		44,151 vs 44006
	- Windham:		26,706 vs 26701

## Delaware

* The “precinct” field for Delaware’s cleaned results is formatted as “Election District #-State House District #”. This is following the format of Delaware’s Election District Structure as seen at https://elections.delaware.gov/districtmaps/pdfs/EDRD2012_2022v1.pdf This is reversed from the format of the precinct/election district name published in the official results, to remain consistent with previously cleaned election results from 2016/2018.

* Precincts 17-41 and 17-31 received 0 votes in the official results. These precincts are not present in previous election returns.

## District of Columbia

* For DC, the jurisdiction_name variable indicates ward number. 

## Florida

* Overvotes, Undervotes and some write-in candidate votes were not reported on offical canvas results so were not verified.

* There are a number of very small discrepancies between our precinct data and  in the Florida data. Most of the discrepancies, when looking at aggregate vote totals, are less than 10 votes. The discrepancies come from Monroe County, Seminole County, and for some of the elections that had recounts. Here is a list of offices and districts with small discrepancies:

	- All statewide offices, including us president, supreme court, and all of the constitutional amendments

	- CIRCUIT JUDGE		15TH JUDICIAL CIRCUIT, GROUP 30

	- US HOUSE			District 007

	- US HOUSE			District 026

	- STATE SENATE		District 009

	- STATE SENATE		District 037

	- STATE SENATE		District 039

	- STATE HOUSE			District 028

	- STATE HOUSE			District 029

	- STATE HOUSE			District 030

	- STATE HOUSE			District 120

## Idaho

* Updated 12-07-2021. Updated underlying raw data to fix previous discrepancy in votes for Constitutional Amendment HJR 4 in Power County.

## Illinois

* Official IL results report only certain individual write-in candidates, while precinct data reports scatter write-ins

* Judge McGlynn (District 020 Retention Race) is missing from official IL results. They were nominated and approved to serve in a federal district court in 2020.

## Indiana
* Only 53 of Indiana's 92 counties released precinct-level election results in 2020. Those counties are: ADAMS, ALLEN, BARTHOLOMEW, BLACKFORD, BOONE, BROWN, CARROLL, CASS, CLARK, CLINTON, CRAWFORD, DECATUR, DEKALB, DELAWARE, ELKHART, FRANKLIN, FULTON, GIBSON, GRANT, HAMILTON, HARRISON, HENRY, HOWARD, HUNTINGTON, JEFFERSON, JENNINGS, JOHNSON, KNOX, KOSCIUSKO, LAGRANGE, LAKE, MADISON, MARION, MARTIN, MIAMI, MONROE, OHIO, PIKE, PORTER, POSEY, PUTNAM, RUSH, SHELBY, STEUBEN, SULLIVAN, UNION, VANDERBURGH, VERMILLION, WABASH, WAYNE, WELLS, WHITE, WHITLEY

For all other counties, no precinct-level data are available. For counties that did release information at the precinct level, they released that information *only* at the precinct level, which means that we cannot compare the precinct-level vote totals to vote totals at any other level. The only exception is the US House, where we can compare precinct-level totals to the congressional report of votes at the candidate-district level. Here are those discrepancies, where the difference is theirs minus ours:
candidate 	district 	precinct-votes 	official-votes 	difference
       FRANK J MRVAN      001         172543         185180      12637
          MARK LEYVA      001         121563         132247      10684
     MICHAEL STRAUSS      001           8396           9521       1125
     JACKIE WALORSKI      002          88113         183601      95488
PATRICIA PAT HACKETT      002          36642         114967      78325
       CHIP COLDIRON      003          98499         104762       6263
           JIM BANKS      003         200129         220989      20860
           JIM BAIRD      004          81575         225531     143956
          JOE MACKEY      004          33674         112984      79310
      CHRISTINA HALE      005         189320         191226       1906
      KENNETH TUCKER      005          16276          16788        512
     VICTORIA SPARTZ      005         202672         208212       5540
          GREG PENCE      006         143836         225319      81483
   JEANNINE LEE LAKE      006          64951          91103      26152
      TOM FERKINHOFF      006           7795          11791       3996
        ANDRÉ CARSON      007         176422         176422          0
   SUSAN MARIE SMITH      007         106146         106146          0
 E THOMASINA MARSILI      008          46822          95691      48869
 JAMES D RODENBERGER      008           4792          10283       5491
     LARRY D BUCSHON      008          97837         214643     116806
           ANDY RUFF      009          88015         122566      34551
      TONYA L MILLIS      009           9217          14415       5198
  TREY HOLLINGSWORTH      009         131317         222057      90740

## Iowa

* Counts in the race for US HOUSE District 2 in Scott County are short by a total of 184 votes across all candidates.

* Updated 12-09-2021 so US HOUSE District 2 results in Scott County now match the official precinct results at https://sos.iowa.gov/elections/results/xls/2020/general/Scott.pdf.

## Kansas

* Judicial District Court data and not included at the moment. 

## Kentucky

* Kentucky precinct data source is: https://results.enr.clarityelections.com/KY/106379/web.264614/#/summary. These results are "unofficial", thus vote totals are marginally undercounted in certain counties/races. 

* Certain Kentucky counties do not report data at the precinct level, either aggregated by voting mode at the county level or total votes at the county level. Certain Kentucky counties chose to centralize voting at the county level, allowing voters to vote at any open polling location as a result of poll closures during the COVID-19 pandemic. Such counties are marked in the precinct field as "COUNTY FLOATING".

## Maine

* Maine reports election results at the township level, rather at the precinct level. Township/municipality is treated as precinct in the cleaned data. 

* Certain rows contain county-fips info in place of jurisdiction-fips info for one of two reasons: (1) Maine reports state UOCAVA vote totals for each candidate aggregated at the county level. (2) Township information for certain towns could not be matched to our jurisdiction-fips merger file. 

## Michigan

* Precinct data are taken from https://miboecfr.nictusa.com/cgi-bin/cfr/precinct_srch.cgi?elect_year_type=2020GEN&county_code=00&Submit=Search

* Precinct data contain precinct "9999", which are "statistical adjustments" rows that must be carefully considered when aggregating vote totals by office/county. 

* Vote totals aggregated by county that include this 9999 precinct do not match the official county totals for every race.

* Vote totals aggregated by county that DO NOT include this 9999 precinct do not match the official county totals for every race either, but are significantly closer to the official totals than when the 9999 precinct rows are kept.

* All rows that have a discrepancy when aggregated by county (with or without the 9999 precinct rows) are marked readme_check == "TRUE". 


## Mississippi

* Only includes US President, US Senate, and US House results at the moment.

* Many of the race totals are off by a handful of votes, and we are not able to identify the individual precincts which are off. 

* Here are some of the discrepancies reported for president. (Values in parentheses are how much higher or lower our data is relative to what is reported in official results, i.e. MEDSL total minus the official reported total.)

	* STATEWIDE
		- Trump (+102)
		- Biden (-1814)

* Counties with discrepancies:

	* Trump
		- AMITE (+80)
		- COAHOMA (+25)
		- KEMPER (-3)

	* Biden
		- BOLIVAR (-200)
		- COAHOMA (+111)
		- COVINGTON (-3)
		- HINDS (-1400)
		- SCOTT (-322)

## Nevada

* From the official Nevada 2020 Election results spreadsheet: "Note: In cases where the cumulative turnout for a precinct for a race or ballot question is greater than 0 but less than 10, the numbers have been replaced with an asterisk in order to protect the secrecy of a voter's ballot, as required by Nevada Law. As a result, the total for a precinct may be different from what is reported on official documents." 

* We have included these cases in our cleaned results, replacing the asterisk with -1 to preserve the votes values as ints. These results should be dropped when aggregating results at the state/county level. Certain county aggregated results in affected races are marginally different from the official reported vote totals due to the masking of votes for privacy purposes.

## New Hampshire

* Districts marked with an F are floterial districts.

* State House district numbers reset for every county. Thus, state house members need to have their districts concatenated with county when inspecting district information.

* Our aggregated results do not match official totals for certain races. Those races include (but may not be limited to):
	- All County Register of Probate candidates in Grafton County (Excel spreadsheet sum cells missed two rows).
	- Scatter candidates in State House District 18 in Strafford County (Sum cell is off by one).

* No full names could be found for writein candidates Teszler and Townsend for County Register of Probate in Grafton County.

* Recounts in the state do not seem to include scatter votes, so they were not included. This explicitly affects all races with stage 'GEN RECOUNT' but State Senate District 12 (which did not list any scatters for the original race either).

## New Jersey

* New Jersey reports election results at the township level, rather at the precinct level. Township/borough is treated as precinct in the cleaned data. 

## New Mexico

* New Mexico "masks" vote totals in precinct results for candidates with small vote tallies, to protect the privacy of voters. These masked votes are denoted as "-1" in the votes column.

## New York

* Only includes data for US President, US House, State House, and State Senate at the moment. Data contain some small discrepancies with official SOS data due to changes reflected in the "Revision History" of official county level data. These revisions are not matched to precincts and thus not reflected in our precinct data. Other small discrepancies NOT accounted for in the revision history are documented below.

* Counties with unaccounted discrepancies for US PRESIDENT (our data - SOS county data):
	- CAYUGA [Trump (REP) -1, Trump (Other) +1] 
	- PUTNAM [Biden (DEM) -6, Trump (REP) -6]
	- SUFFOLK [Trump (Other) -34, Hawkins (Other) -5, Jorgensen (LBT) -10, Pierce (Other) -14] 

* Counties with unaccounted discrepancies for US HOUSE (our data - SOS county data):
	- PUTNAM (district 18) [CHELE C FARLEY (REP) -6, SCOTT A SMITH (LBT) -1, SEAN PATRICK MALONEY (DEM) -4, SEAN PATRICK MALONEY (IND) -1]
	- LEWIS (district 21) [ELISE M STEFANIK (REP) -4, TEDRA L COBB (Working Families) -9] 
	- TOMPKINS (district 23) [TRACY MITRANO (DEM) -1]

* Counties with unaccounted discrepancies for STATE SENATE (our data - SOS county data):
	- LEWIS (district 47) [JOSEPH A GRIFFO (REP) -4, JOSEPH A GRIFFO (CON) -1]
	- SENECA (district 54) [PAMELA A HELMING (REP) +95, PAMELA A HELMING (CON) -206, PAMELA A HELMING (IND) +107, PAMELA A HELMING (SAM) +2, SHAUNA O'TOOLE (DEM) -646]

* Counties with unaccounted discrepancies for STATE HOUSE (our data - SOS county data):
	- LEWIS (district 117) [KENNETH BLANKENBUSH (REP) -4, KENNETH BLANKENBUSH (CON) -1]
	- DELAWARE (district 122) [JOE G ANGELINO (CON) +1]
	- CHENANGO (district 126) [DIA CARABAJAL (WF) -1]

## North Carolina

* Sorted precinct data within "individual_states" zipfile. The file "2020-nc-precinct-general-sorted.csv" contains the mode for transfer ballots. Matching these votes to specific precincts introduces small amounts of error to the overall vote totals when aggregating by office/county.

* The raw data source for the sorted precinct results is: https://dl.ncsbe.gov/?prefix=ENRS/2020_11_03/results_precinct_sort/

* The codebook for the original fields in the raw sorted precinct results is: https://s3.amazonaws.com/dl.ncsbe.gov/ENRS/2020_11_03/layout_results_precinct_sort.txt

* The raw data for the sorted precinct results contains two precinct columns (number and name). We combine these fields in the latest update, separating with an underscore "_" (name_code). If the fields match exactly or one is left blank, we only report one field that contains information.

* The raw data sorted precinct results contains a field for the "group number", which is related to the voting mode. This field was initially excluded, but this introduced error to our version of the results in the form of near duplicate rows. Therefore, we have added the "Group number" to the mode field, separated by an underscore "_" (voting method_group number).



## Ohio

* Ohio records its data with precincts on rows and candidates on columns. However, they record candidates that were not selectable in a particular precinct (because they did not run in a the associated district) as having received 0 votes, which is otherwise indistinguishable from candidates who ran in a precinct but received no votes. Keeping all these entries as is yields over 3 million records records and an extremely large file, so 0 vote records were manually dropped as follows:
	- Records for candidates running for US President were kept as is.
	- For all other records, entries with 0 votes were discarded.
* This leads to the situation where every other race (including US House, State Senate and State House elections, which are district based but do not list name of county) will have more records than needed removed (namely, records of candidates who ran in a precinct but got 0 votes there).

* Ohio does not provide precinct-based vote totals for writein candidates, but they do provide a county-based vote total for each writein. The cleaned dataset aggregates all writeins per office on a county basis.

## Oregon

* Only includes data for US President, US Senate, and US House at the moment.

## Pennsylvania

* The raw precinct data is provided by the Pennsylvania Department of State.

* The raw precinct data included a "Municipality Name" field, which has been stored in the "jurisdiction_name" field of our dataset. However, the "jurisdiction_fips" field is the same as the "county_fips" field, as there are no 10 digit jurisdiction FIPs codes associated with the provided municipalities. 

* There are marginal discrepancies between the aggregated precinct results and the results from the Secretary of State’s website. Precinct results are uncertified and uncorrected for later updates during the certification process, whereas the state website results reflect certified returns. Certified SOS results include “grace period” ballots (ballots postmarked and received by the Friday after election day), while the precinct results in many counties often do not.

* Here are the discrepancies by county for US President (aggregated precinct data - official SOS results)
	- ADAMS (Trump +44, Biden +53)
	- ALLEGHENY (Trump +765, Biden +1147)
	- DELAWARE (Trump +362, Biden +214)
	- FAYETTE (Trump +16, Biden +10)
	- MONROE (Trump -601, Biden -731)
	- NORTHUMBERLAND (Trump +314, Biden +75)
	- PHILADELPHIA (Trump -158, Biden -2011)
	- WESTMORELAND (Trump +904, Biden +357)

## South Dakota

* State house district 012 features original results and recount results. The two counts are differentiated by the mode field (either "GEN" or "GEN RECOUNT").

## Texas

* Raw data were obtained from the Texas Legislative Council (https://data.capitol.texas.gov/dataset/2020_general). 

* When comparing the precinct results to the official county results, MEDSL identified a list of precinct results (aggregated by county/office/candidate/district) that do not match the offical totals. The majority of discrepancies are insignificant relative to the total votes, but larger counties (eg Williamson), have more substantial discrepancies. Documentation containing the exact vote total discrepancies is available upon request. 

* The Texas Legislative Council data contains breakdown by Voting Tabulation District (VTD). This is treated as the precinct field in our data. The number of VTDs in a county do not always match the number of precincts in a given county (https://data.capitol.texas.gov/topic/about/elections)

* Races where candidates ran unopposed and recieved 100% of the votes were not included in the raw precinct data.

## Utah

* Duchesne county is short one vote compared to official sources (https://electionresults.utah.gov/elections/). As such, the county of Duchesne is flagged readme_check==True. 

## Vermont

* Vermont provides the township level data broken down further by representative districts within township. The precinct field is thus a combination of the "Township" and "Rep District" fields, separated by an underscore "_".

* For State Senate races, Vermont has floating towns: towns that are physically located in one county but vote for senator in another county, so special care must be taken care off when aggregating votes.
	- Addison State Senate: Huntington is in Chittenden County and votes for Addison State Senator.
	- Bennington State Senate: Wilmington is in Windham County and votes for Bennington State Senator.
	- Caledonia State Senate: Bradford, Fairlee, West Fairlee, Newbury, Topsham are in Orange County and vote for Caledonia State Senator.
	- Essex-Orleans State Senate: Wolcott is in Lamoille County and votes for Essex-Orleans State Senator.
	- Franklin State Senate: Alburgh is in Grand Isle County and votes for Franklin State Senator.
	- Grand Isle State Senate: Colchester is in Chittenden County and votes for Grand Isle State Senator.
	- Windsor State Senate: Londonderry is in Windham County and votes for Windsor State Senator.

## Virginia

* Many of the write-in candidates in the Virginia elections show small discrepancies between the vote totals reported on the Virginia SOS website (here: https://results.elections.virginia.gov/vaelections/2020%20November%20General/Site/Presidential.html) and the votes in the raw data sheets. 

## Wisconsin

* 9 Two towns in Wisconsin (Waukesha, Waukesha County; Vernon, Waukesha County) were upgraded to villages in 2020 [1](https://www.jsonline.com/story/communities/waukesha/news/2020/05/06/town-waukesha-residents-ok-incorporation-referendum-huge-margin/5175520002/) [2](https://www.villageofvernonwi.org/newsdetail_T2_R397.php). However, both the [Wisconsin](https://doa.wi.gov/DIR/Changes_in_WI_Munis_2000.xlsx) and [US Census]  (https://www.census.gov/programs-surveys/acs/technical-documentation/table-and-geography-changes.html) directories do not reflect the changes. For the moment, their jurisdiction FIPS code is listed as the one they had while they were a town.
