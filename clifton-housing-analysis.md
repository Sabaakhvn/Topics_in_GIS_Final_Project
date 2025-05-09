# Affordable Housing Development Feasibility Analysis
## Clifton, New Jersey

### Introduction
This project analyzes the potential for affordable housing development in Clifton, New Jersey through GIS-based spatial analysis. Using demographic, economic, and land use data, this study identifies priority areas for affordable housing development based on socioeconomic need, transit accessibility, and vacant land availability.

### Key Findings

#### Land Use Distribution and Tax Revenue
The analysis of Clifton's land use reveals that residential properties dominate the landscape, covering 52.57% of the city's total land area, while generating approximately $222 million in annual tax revenue.

![Categorical Map of Clifton Parcels by Property Class](https://raw.githubusercontent.com/yourusername/clifton-housing-analysis/main/images/property-class-map.jpg)

**Table: Land Use Distribution and Tax Revenue in Clifton, NJ**

| Property Class | Class Type | Land Area (Acres) | Percentage of Total | Last Year Tax | Avg Tax per SqFt |
|----------------|------------|-------------------|---------------------|---------------|------------------|
| 1 | Vacant Land | 139.3 | 2.66% | $2,147,974.02 | $0.35 |
| 15A | Public School Property | 129.3 | 2.47% | $0 | $0.00 |
| 15B | Other School Property | 22.3 | 0.43% | $8,661.17 | $0.01 |
| 15C | Public Property | 315.3 | 6.01% | $19,467.84 | $0.00 |
| 15D | Religious & Charitable Property | 95.8 | 1.83% | $13,471.05 | $0.00 |
| 15E | Cemeteries and Graveyards | 189.9 | 3.62% | $0 | $0.00 |
| 15F | Other Exempt properties | 36.3 | 0.69% | $188,779.06 | $0.12 |
| 2 | Residential | 2,755.9 | 52.57% | $222,104,426.30 | $1.85 |
| 3A | Farms | 14.4 | 0.28% | $17,295.09 | $0.03 |
| 4A | Commercial | 651.9 | 12.43% | $45,114,041.48 | $1.59 |
| 4B | Industrial | 668.0 | 12.74% | $31,322,155.54 | $1.08 |
| 4C | Apartments | 131.9 | 2.52% | $8,205,775.71 | $1.43 |
| 5A | Class I Railroad Property | 85.7 | 1.63% | $0 | $0.00 |
| 5B | Class II Railroad Property | 6.7 | 0.13% | $0 | $0.00 |
| **Total** | | **5,242.7** | **100.0%** | **$309,142,047** | |

**Potential Additional Tax Revenue from Vacant Land Development:**
- If developed as Residential: $11,227,129.22
- If developed as Commercial: $45,114,030.53
- If developed as Industrial: $31,322,147.39
- If developed as Apartments: $8,205,776.84

#### Housing Occupancy Patterns
Clifton exhibits distinct patterns of housing occupancy, with owner-occupied units (shown in teal) dominating the western portions of the city, while renter-occupied units (shown in peach) are concentrated in the eastern and central areas.

![Housing Occupancy and Vacancy Patterns in Clifton, NJ](https://raw.githubusercontent.com/yourusername/clifton-housing-analysis/main/images/housing-occupancy-map.jpg)

#### Income Distribution
The analysis reveals significant income disparities across Clifton, with median household incomes ranging from over $119,300 in the western neighborhoods to less than $37,800 in the northeastern section.

![Median Household Income in Clifton, NJ](https://raw.githubusercontent.com/yourusername/clifton-housing-analysis/main/images/median-income-map.jpg)

#### Housing Cost Burden
A substantial proportion of Clifton's renters experience housing cost burden, with several census tracts showing that over 66% of renter households spend 30% or more of their income on housing costs.

![Percent of Renter Households with Housing Cost Burden](https://raw.githubusercontent.com/yourusername/clifton-housing-analysis/main/images/rent-burden-map.jpg)

### Vacant Land Analysis

#### Spatial Distribution of Vacant Parcels
Vacant parcels in Clifton are not randomly distributed but show distinct clustering patterns along major transportation corridors and in areas with lower land values. The choropleth map below shows the land value per square foot across Clifton, with vacant parcels highlighted in magenta.

![Choropleth Map of Clifton Parcels by Land Value per Sq. Ft](https://raw.githubusercontent.com/yourusername/clifton-housing-analysis/main/images/land-value-map.jpg)

#### Transit Accessibility
The analysis of transit accessibility reveals that many vacant parcels are well-served by public transportation, with numerous bus stops throughout the city and several train stations in neighboring communities.

![Map of Clifton Vacant Parcels by Transit Accessibility](https://raw.githubusercontent.com/yourusername/clifton-housing-analysis/main/images/transit-accessibility-map.jpg)

### Affordable Housing Development Opportunities

#### Need Score Methodology
To identify priority areas for affordable housing development, a composite "Need Score" was created by normalizing and combining four key indicators:

1. **Rent Burden**: Percentage of renter households spending 30% or more of income on rent
2. **Owner Burden**: Percentage of owner households spending 30% or more on housing costs
3. **Low-Income Population**: Percentage of households with annual income below $75,000
4. **Demographic Composition**: Percentage of people of color

Each indicator was normalized using min-max scaling to create a 0-1 scale:
```
Normalized_Value = (Raw_Value - Minimum_Value) / (Maximum_Value - Minimum_Value)
```

The Need Score was calculated as the average of the four normalized indicators:
```
Need_Score = (Norm_RentBurden + Norm_OwnerBurden + Norm_LowIncome + Norm_POC) / 4
```

#### Priority Areas for Development
The combined analysis of Need Score and vacant parcel distribution identifies several high-priority areas for affordable housing development, particularly in the eastern and central portions of Clifton.

![Target Areas for Affordable Housing Development](https://raw.githubusercontent.com/yourusername/clifton-housing-analysis/main/images/target-areas-map.jpg)

### Transit-Oriented Development Opportunities
By overlaying transit accessibility with vacant parcels and Need Score, the analysis identifies specific opportunities for transit-oriented affordable housing development.

![Identifying Transit-Oriented Affordable Housing Opportunities](https://raw.githubusercontent.com/yourusername/clifton-housing-analysis/main/images/transit-oriented-opportunities-map.jpg)

### Racial and Ethnic Composition
The demographic analysis shows that Clifton has distinct patterns of racial and ethnic distribution, with Hispanic or Latino populations concentrated in the eastern portions of the city.

![Racial and Ethnic Composition in Clifton, NJ By Census Tract](https://raw.githubusercontent.com/yourusername/clifton-housing-analysis/main/images/racial-composition-map.jpg)

### Conclusions and Recommendations

Based on the comprehensive analysis, the following recommendations are proposed for affordable housing development in Clifton:

1. **Prioritize Eastern Census Tracts**: Focus affordable housing development in eastern Clifton where Need Scores are highest and multiple vacant parcels are available.

2. **Leverage Transit-Oriented Development**: Target vacant parcels within 0.25 miles of bus stops or 0.5 miles of train stations to maximize accessibility for lower-income residents without vehicles.

3. **Diversify Housing Stock**: Develop a mix of housing types, including apartments and multi-family residential buildings, particularly in areas currently dominated by single-family homes.

4. **Public-Private Partnerships**: Establish partnerships with private developers to maximize the development potential of vacant land, particularly where corporate ownership is present.

5. **Tax Revenue Optimization**: Consider mixed-use developments that include commercial components to optimize tax revenue generation while still providing affordable housing units.

6. **Inclusionary Zoning**: Implement inclusionary zoning policies requiring a percentage of affordable units in new residential developments, particularly in areas with high median incomes.

### Limitations and Further Research

This analysis has several limitations that could be addressed in future research:

- **Data Currency**: Some demographic data may not capture recent changes in population or housing patterns.
- **Zoning Constraints**: This analysis does not incorporate current zoning regulations that may limit development potential.
- **Environmental Factors**: Potential environmental constraints on vacant parcels are not considered.
- **Market Dynamics**: Current market conditions and developer interest are not fully captured.

Additional data sources that would enhance the analysis include:

- Detailed zoning and land use regulations
- Utility infrastructure capacity
- Brownfield or contamination site data
- Housing permits and pipeline projects
- School enrollment and capacity data
- Detailed parcel-level ownership information

### Acknowledgments

This project was completed as part of the Topics in GIS course. Special thanks to the professor Will Payne and the City of Clifton for providing access to the necessary data.

### Contact

For more information about this analysis, please contact [Saba Akhavansadr] at [saba.akhavansadr@rutgers.edu].
