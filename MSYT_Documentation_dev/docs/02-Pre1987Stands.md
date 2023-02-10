# Stands Harvested prior to 1987

**Pre January1, 1982**  

*With a few exceptions, before 1982, persons who harvested on provincial forest land had no obligation to reforest.  The Ministry of Forests managed the reforestation activities.*  

**January 1, 1982 to October 1, 1987**  

*With a few exceptions, before October 1, 1987, persons who harvested on provincial forest had no obligation to reforest. This era is complicated in that there was an expectation for the licensees to manage reforestation activities, but for the Ministry of Forests to fund the activities.*  


- Prior to 1987 there was no legal obligation to achieve a stocking standard
- Prior to 1987 there was no check to see if a standard had been achieved
- Prior to 1987, there were a high number of plantation failures.  
- At this point in time, it is difficult to identify the planted trees.   
- Significant improvements have been made both in genetic stock and planting techniques since 1987.


## Categorization

The question is:  even if we called a stand like this planted, would we expect it to perform the same as a stand planted at the same density and site index today?

The data sometimes shows that yes there were planted stands, but there is some question about their performance.  

It has been problematic to use the RESULTS forest cover species composition due to the age and source of the data (MLSIS,ISIS).  Data is missing or incomplete.

Previous TSRs used a VDYP curve for these types of stands thus in essence not recognizing any management for these types of stands. We want to recognize that these stands are managed and thus differ from an existing natural, but we can't give them the full weight of a planted curve.


## Yield options 

There are basically 4 options for yield assignment:

- VDYP (existing natural)
- TIPSY even (planted)
- TIPSY random (natural)
- TIPSY clustered (not generally used)


We can discount using VDYP as it is too conservative.  We can also discount using planted as it is probably optimistic.  Therefore, using a TIPSY natural (random spacing) seems a reasonable choice.

## Stand Information

To generate a MSYT we require species composition and density at the time of stand_initiation.

In general, stand information available in RESULTS for pre 87 stands is poor.  

In addition, there has usually been a VRI update of these stands since 1987.  Therefore, a more current assessment of a stand description exists. 

Since these stands initiated prior to 1987, the stand information in VRI is well past initiation.  However, there is an option in TIPSY that allows us to backgrow a stand.  TIPSY can be provided with a species composition and a density at a given reference year.  Tipsy will then backgrow the density to time 0 and provide a MSYT based on the initiation density.

In VRI, this density is defined at what is know as the reference year of the VRI.  That is the year when the photos used for classification were taken.  

So, knowing the reference year and the density at the reference year, TIPSY can produce a MSYT from VRI projected attribution.



## Photo classification

When an interpreter looks at an area that was harvested prior to 1987, they use a variety of information  

- air photo
- RESULTS Forest Cover information

The interpreter uses the RESULTS information (age/species) as a reference but can also chose to select different values.  

| Attribute | Comment |
|:--|:--|
|Age| Age can come either from RESULTS or from a surrounding similar area.  |
|Height| In general the height will come from the photo.  |
|Species| Species can come from RESULTS if it is similar to the photo.|
|Density| Interpreter calls the original estimate at the reference year|

Note that density may be further "adjusted" by the VDYP projection process.



## Attribution for Generating a yield table

- attribution from VRI
  - reference age (age of photo)
  - density (live stems) at reference age
  - species composition

## Representation in BTC

- past planting is ignored
- therefore no planting delay
- treated as Natural (random spacing)

- backgrown from reference year to determine stand initiation conditions

## Stand Reference Age

Reference age is determined (for an opening) as the difference between:

- reference year
- harvest year


- generally select year from the largest feature

First choice is to use the RESULTS harvest date.  
If the RESULTS harvest date is missing, then use the VRI harvest date.  

## Data details

### age ranges within an opening

features within an opening can have different ages.  
the assignment of reference age is based on the opening in aggregate form.

| feature_id | opening_id | area | proj_age_1 |sph |vri_ref_age |
|:-----------|:------------|:----|:----------|:---|:---------|
|   16710801 | -612660000 | 7.0 |        35 | 1701 |31|
|   16710818 | -612660000 | 20.3 |      35 | 1701 |  31|
|   16710777 | -612660000 | 3.0 |       15 | 600 |  31|

As an example, here we see an opening with 3 features.  
The largest feature has an area of 20.3  

However, note that there is a feature with an age less than what we might expect for a stand harvested prior to 1987.  

This is just a fact of how stands develop over time and structure is altered.  

### reference age and density

The opening based assignment of MSYT, uses an area weighted density derived based on all opening features.


| opening_id | harvest_year | reference_year | vri_ref_age | vri_ref_sph |
|:----------|:-------|:------|:-------------|:--|
| -612660000 | 1985 |   2016 |      31 |        1592|




