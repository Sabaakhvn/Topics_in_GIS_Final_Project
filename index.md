<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Affordable Housing Development Feasibility Analysis - Clifton, NJ</title>
    <script>
    // Remove unwanted hashtags from URL
    if (window.location.hash) {
        history.replaceState 
            ? window.history.replaceState(null, null, window.location.href.split('#')[0])
            : window.location.hash = '';
    }
    
    // Prevent automatic adding of hash to URL when clicking on headings
    document.addEventListener('DOMContentLoaded', function() {
        // Find all heading elements
        const headings = document.querySelectorAll('h1, h2, h3, h4, h5, h6');
        
        // For each heading
        headings.forEach(function(heading) {
            // Remove any existing links within the heading
            const links = heading.querySelectorAll('a');
            links.forEach(function(link) {
                // Replace the link with its inner content
                link.outerHTML = link.innerHTML;
            });
            
            // Prevent click events from adding hashtags
            heading.addEventListener('click', function(e) {
                e.preventDefault();
                return false;
            });
        });
    });
    </script>
    <style>
        /* Remove anchor links/clip icons from headings */
        .header-link, 
        h1 a, h2 a, h3 a, h4 a, h5 a, h6 a,
        h1 svg, h2 svg, h3 svg, h4 svg, h5 svg, h6 svg {
            display: none !important;
            visibility: hidden !important;
        }
        
        /* Main styles */
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            background-color: #f9f9f9;
        }
        
        .location-map {
            margin: 30px 0;
            text-align: center;
        }
        
        .location-map img {
            max-width: 70%;
            height: auto;
            margin: 0 auto;
            display: block;
            border: 1px solid #ddd;
            border-radius: 4px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }

        header {
            text-align: center;
            margin-bottom: 40px;
            padding: 30px 20px;
            background-color: #2c3e50;
            color: white;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }

        h1, h2, h3 {
            margin-bottom: 15px;
            color: #2c3e50;
        }

        header h1, header h2 {
            color: white;
        }

        section {
            margin-bottom: 40px;
            background-color: white;
            padding: 25px;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }

        .finding {
            margin-bottom: 30px;
        }

        img {
            max-width: 100%;
            height: auto;
            margin: 20px 0;
            border: 1px solid #ddd;
            border-radius: 4px;
            display: block;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
            font-size: 0.9em;
        }

        table, th, td {
            border: 1px solid #ddd;
        }

        th, td {
            padding: 12px;
            text-align: left;
        }

        th {
            background-color: #f2f2f2;
            font-weight: bold;
        }

        tr:nth-child(even) {
            background-color: #f9f9f9;
        }

        footer {
            text-align: center;
            margin-top: 50px;
            padding: 20px;
            color: #777;
            border-top: 1px solid #ddd;
        }

        .highlight-box {
            background-color: #e8f4f8;
            padding: 15px;
            border-left: 4px solid #3498db;
            margin: 20px 0;
        }

        .conclusion-item {
            margin-bottom: 15px;
            padding-left: 20px;
            position: relative;
        }

        .conclusion-item:before {
            content: "•";
            position: absolute;
            left: 0;
            color: #3498db;
            font-weight: bold;
        }

        @media (max-width: 768px) {
            body {
                padding: 10px;
            }
            
            header, section {
                padding: 15px;
            }
            
            table {
                font-size: 0.8em;
            }
            
            th, td {
                padding: 8px;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>Affordable Housing Development Feasibility Analysis</h1>
        <h2>Clifton, New Jersey</h2>
    </header>
    
    <main>
        <section id="introduction">
            <h2>Introduction</h2>
            <p>This project analyzes the potential for affordable housing development in Clifton, New Jersey through GIS-based spatial analysis. Using demographic, economic, and land use data, this study identifies priority areas for affordable housing development based on socioeconomic need, transit accessibility, and vacant land availability.</p>
            
            <div class="location-map">
                <h3>Study Area: Clifton, New Jersey</h3>
                <img src="images/NJ_Clifton.jpg" alt="Map showing the location of Clifton in New Jersey">
            </div>
        </section>

        <section id="key-findings">
            <h2>Key Findings</h2>
            
            <div class="finding">
                <h3>Land Use Distribution and Tax Revenue</h3>
                <p>The analysis of Clifton's land use reveals that residential properties dominate the landscape, covering 52.57% of the city's total land area, while generating approximately $222 million in annual tax revenue.</p>
                <img src="images/Property Class.jpg" alt="Categorical Map of Clifton Parcels by Property Class">
                
                <table>
                    <thead>
                        <tr>
                            <th>Property Class</th>
                            <th>Property Type</th>
                            <th>Land Area (Acres)</th>
                            <th>Percentage of Total</th>
                            <th>Annual Tax Revenue</th>
                            <th>Avg Tax per Sq. Ft.</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>1</td>
                            <td>Vacant Land</td>
                            <td>139.3</td>
                            <td>2.66%</td>
                            <td>$2,147,974.02</td>
                            <td>$0.35</td>
                        </tr>
                        <tr>
                            <td>15A</td>
                            <td>Public School Property</td>
                            <td>129.3</td>
                            <td>2.47%</td>
                            <td>$0</td>
                            <td>$0.00</td>
                        </tr>
                        <tr>
                            <td>15B</td>
                            <td>Other School Property</td>
                            <td>22.3</td>
                            <td>0.43%</td>
                            <td>$8,661.17</td>
                            <td>$0.01</td>
                        </tr>
                        <tr>
                            <td>15C</td>
                            <td>Public Property</td>
                            <td>315.3</td>
                            <td>6.01%</td>
                            <td>$19,467.84</td>
                            <td>$0.00</td>
                        </tr>
                        <tr>
                            <td>15D</td>
                            <td>Religious & Charitable Property</td>
                            <td>95.8</td>
                            <td>1.83%</td>
                            <td>$13,471.05</td>
                            <td>$0.00</td>
                        </tr>
                        <tr>
                            <td>15E</td>
                            <td>Cemeteries and Graveyards</td>
                            <td>189.9</td>
                            <td>3.62%</td>
                            <td>$0</td>
                            <td>$0.00</td>
                        </tr>
                        <tr>
                            <td>15F</td>
                            <td>Other Exempt properties</td>
                            <td>36.3</td>
                            <td>0.69%</td>
                            <td>$188,779.06</td>
                            <td>$0.12</td>
                        </tr>
                        <tr>
                            <td>2</td>
                            <td>Residential</td>
                            <td>2,755.9</td>
                            <td>52.57%</td>
                            <td>$222,104,426.30</td>
                            <td>$1.85</td>
                        </tr>
                        <tr>
                            <td>3A</td>
                            <td>Farms</td>
                            <td>14.4</td>
                            <td>0.28%</td>
                            <td>$17,295.09</td>
                            <td>$0.03</td>
                        </tr>
                        <tr>
                            <td>4A</td>
                            <td>Commercial</td>
                            <td>651.9</td>
                            <td>12.43%</td>
                            <td>$45,114,041.48</td>
                            <td>$1.59</td>
                        </tr>
                        <tr>
                            <td>4B</td>
                            <td>Industrial</td>
                            <td>668.0</td>
                            <td>12.74%</td>
                            <td>$31,322,155.54</td>
                            <td>$1.08</td>
                        </tr>
                        <tr>
                            <td>4C</td>
                            <td>Apartments</td>
                            <td>131.9</td>
                            <td>2.52%</td>
                            <td>$8,205,775.71</td>
                            <td>$1.43</td>
                        </tr>
                        <tr>
                            <td>5A</td>
                            <td>Class I Railroad Property</td>
                            <td>85.7</td>
                            <td>1.63%</td>
                            <td>$0</td>
                            <td>$0.00</td>
                        </tr>
                        <tr>
                            <td>5B</td>
                            <td>Class II Railroad Property</td>
                            <td>6.7</td>
                            <td>0.13%</td>
                            <td>$0</td>
                            <td>$0.00</td>
                        </tr>
                        <tr>
                            <td><strong>Total</strong></td>
                            <td></td>
                            <td><strong>5,242.7</strong></td>
                            <td><strong>100.0%</strong></td>
                            <td><strong>$309,142,047</strong></td>
                            <td></td>
                        </tr>
                    </tbody>
                </table>

                <div class="highlight-box">
                    <h4>Potential Additional Tax Revenue from Vacant Land Development:</h4>
                    <ul>
                        <li>If developed as Residential: $11,227,129.22</li>
                        <li>If developed as Commercial: $45,114,030.53</li>
                        <li>If developed as Industrial: $31,322,147.39</li>
                        <li>If developed as Apartments: $8,205,776.84</li>
                    </ul>
                </div>
            </div>
            
            <div class="finding">
                <h3>Socioeconomic and Housing Analysis</h3>
                <p>The following maps provide a comprehensive view of Clifton's socioeconomic patterns and housing characteristics, revealing important spatial relationships that inform affordable housing needs.</p>
                
                <style>
                    .map-grid {
                        display: grid;
                        grid-template-columns: 1fr 1fr;
                        grid-gap: 20px;
                        margin: 30px 0;
                    }
                    
                    .map-item {
                        display: flex;
                        flex-direction: column;
                    }
                    
                    .map-item img {
                        width: 100%;
                        height: auto;
                        object-fit: contain;
                    }
                    
                    .map-caption {
                        text-align: center;
                        font-weight: bold;
                        margin-top: 10px;
                    }
                    
                    @media (max-width: 768px) {
                        .map-grid {
                            grid-template-columns: 1fr;
                        }
                    }
                </style>
                
                <div class="map-grid">
                    <div class="map-item">
                        <img src="images/Race.jpg" alt="Racial and Ethnic Composition in Clifton, NJ">
                        <div class="map-caption">Racial and Ethnic Composition</div>
                    </div>
                    <div class="map-item">
                        <img src="images/Rent Burden.jpg" alt="Percent of Renter Households with Housing Cost Burden">
                        <div class="map-caption">Rent Burden Distribution</div>
                    </div>
                    <div class="map-item">
                        <img src="images/Income Distribution.jpg" alt="Income Distribution in Clifton, NJ">
                        <div class="map-caption">Income Distribution</div>
                    </div>
                    <div class="map-item">
                        <img src="images/Housing Occupancy.jpg" alt="Housing Occupancy and Vacancy Patterns">
                        <div class="map-caption">Housing Occupancy Patterns</div>
                    </div>
                    <div class="map-item" style="grid-column: span 2;">
                        <img src="images/Median Household Income.jpg" alt="Median Household Income in Clifton, NJ">
                        <div class="map-caption">Median Household Income</div>
                    </div>
                </div>
                
                <p>The maps reveal several key patterns:</p>
                <ul>
                    <li><strong>Housing Occupancy Patterns:</strong> Owner-occupied units (shown in teal) dominate the western portions of the city, while renter-occupied units (shown in peach) are concentrated in the eastern and central areas.</li>
                    <li><strong>Income Distribution:</strong> Significant income disparities exist across Clifton, with median household incomes ranging from over $119,300 in the western neighborhoods to less than $37,800 in the northeastern section.</li>
                    <li><strong>Housing Cost Burden:</strong> A substantial proportion of Clifton's renters experience housing cost burden, with several census tracts showing that over 66% of renter households spend 30% or more of their income on housing costs.</li>
                    <li><strong>Racial and Ethnic Patterns:</strong> Clifton's eastern neighborhoods show higher concentrations of Hispanic or Latino populations, correlating with areas of higher housing cost burden.</li>
                </ul>
            </div>
        </section>

        <section id="vacant-land-analysis">
            <h2>Vacant Land Analysis</h2>

            <div class="finding">
                <h3>Spatial Distribution of Vacant Parcels</h3>
                <p>Vacant parcels in Clifton are not randomly distributed but show distinct clustering patterns along major transportation corridors and in areas with lower land values. The choropleth map below shows the land value per square foot across Clifton, with vacant parcels highlighted in magenta.</p>
                <img src="images/Land Value.jpg" alt="Choropleth Map of Clifton Parcels by Land Value per Sq. Ft">
            </div>

            <div class="finding">
                <h3>Transit Accessibility</h3>
                <p>The analysis of transit accessibility was conducted using ESRI's Network Analyst tool to evaluate pedestrian connectivity to public transportation. Service areas were calculated to precisely delineate zones within a 0.25-mile walking distance of bus stops and a 1.0-mile walking distance of train stations, accounting for the actual street network rather than simple Euclidean distance. This methodology provides a more accurate representation of transit accessibility that reflects real-world pedestrian movement patterns.</p>
                <img src="images/Transit_Accessibility.jpg" alt="Map of Clifton Vacant Parcels by Transit Accessibility">
                
                <h3>Spatial Clustering of Public Transit</h3>
                <p>To further understand the spatial distribution of public transit in Clifton, Optimized Hot Spot Analysis was performed. This geostatistical method identifies statistically significant spatial clusters of high values (hot spots) and low values (cold spots) using the Getis-Ord Gi* statistic. The analysis reveals three distinct hot spot clusters of transit service concentration within Clifton, with the most intense clustering (99% confidence) appearing in the northeastern section of the city. These high-confidence hot spots represent areas where transit accessibility is significantly higher than would be expected by random chance, indicating strategic opportunities for transit-oriented affordable housing development.</p>
                <img src="images/Clifton OHSA.jpg" alt="Spatial Clustering of Public Transit Concentration in Clifton">
                
                <p>The hot spot analysis reinforces the transit accessibility findings by quantitatively identifying areas where multiple transit routes converge, creating nodes of exceptional connectivity. The northeastern cluster, in particular, corresponds with areas of higher housing need scores, creating an ideal intersection of transit access and affordable housing demand. These statistically significant clusters should be prioritized when considering locations for transit-oriented affordable housing development.</p>
            </div>
        </section>

        <section id="need-score">
            <h2>Affordable Housing Development Opportunities</h2>

            <div class="finding">
                <h3>Need Score Methodology</h3>
                <p>To identify priority areas for affordable housing development, a composite "Need Score" was created by normalizing and combining four key indicators:</p>
                
                <ol>
                    <li><strong>Rent Burden</strong>: Percentage of renter households spending 30% or more of income on rent</li>
                    <li><strong>Owner Burden</strong>: Percentage of owner households spending 30% or more on housing costs</li>
                    <li><strong>Low-Income Population</strong>: Percentage of households with annual income below $75,000</li>
                    <li><strong>Demographic Composition</strong>: Percentage of people of color</li>
                </ol>
                
                <p>Each indicator was normalized using min-max scaling to create a 0-1 scale:</p>
                <pre>Normalized_Value = (Raw_Value - Minimum_Value) / (Maximum_Value - Minimum_Value)</pre>
                
                <p>The Need Score was calculated as the average of the four normalized indicators:</p>
                <pre>Need_Score = (Norm_RentBurden + Norm_OwnerBurden + Norm_LowIncome + Norm_POC) / 4</pre>
            </div>

            <div class="finding">
                <h3>Priority Areas for Development</h3>
                <p>The combined analysis of Need Score and vacant parcel distribution identifies several high-priority areas for affordable housing development, particularly in the eastern and central portions of Clifton. In our site selection methodology, we prioritized municipally-owned vacant parcels to streamline development by avoiding potential condemnation proceedings and associated legal complexities. The analysis identified only two municipal vacant parcels within the study area, with the parcel located in the north-central region emerging as the optimal development site based on multiple criteria:</p>
                
                <ul>
                    <li>Strategic location within a census tract exhibiting high affordable housing need scores</li>
                    <li>Exceptional transit connectivity with proximity to multiple bus stops, enhancing accessibility for transit-dependent residents</li>
                    <li>Potential for integration with existing community infrastructure and services</li>
                </ul>
                
                <img src="images/Vacant_Parcels_Need_Score.jpg" alt="Target Areas for Affordable Housing Development">
            </div>

            <div class="finding">
                <h3>Where to Build Next? Multi-Criteria Evaluation of Housing Development</h3>
                <p>By overlaying transit accessibility with vacant parcels and Need Score, the analysis identifies specific opportunities for transit-oriented affordable housing development.</p>
                <img src="images/Transit_Oriented.jpg" alt="Identifying Transit-Oriented Affordable Housing Opportunities">
            </div>
        </section>


<section id="vacant-site-analysis">
    <h2>Historical Analysis of Clifton Railroad Corporation Site (1995-2024)</h2>
    
    <div class="finding">
        <h3>Introduction</h3>
        <p>This analysis examines the historical transformation of the Clifton Railroad Corporation site in Clifton, New Jersey, through a chronological study of satellite imagery spanning nearly three decades. The site, encompassing 3.076 acres of land, represents a significant opportunity for affordable housing development due to its location, moderate size, and evolving usage patterns over time.</p>
    </div>

    <div class="finding">
        <h3>Past: Active Industrial Operations (1995)</h3>
        <img src="images/site-1995.jpg" alt="Clifton Railroad Corporation site in 1995" class="full-width-image">
        <p>The 1995 black and white satellite image reveals an actively functioning industrial site characteristic of mid-to-late 20th century rail operations in northern New Jersey. Key features visible in this earliest image include:</p>
        
        <ul>
            <li>Multiple large warehouse structures with distinctive long, rectangular footprints</li>
            <li>Extensive paved areas used for vehicle and material storage</li>
            <li>Clear signs of industrial activity throughout the property</li>
            <li>A well-defined operational footprint extending across the full parcel</li>
            <li>Adjacent residential neighborhoods with clear boundaries from the industrial zone</li>
        </ul>
        
        <p>During this period, Clifton's industrial corridor, which includes this site, played an important role in the regional economy. The railroad infrastructure facilitated the movement of goods and materials, supporting manufacturing and distribution activities throughout Passaic County.</p>
    </div>
    
    <div class="finding">
        <h3>Transition Period: Early Signs of Change (2010)</h3>
        <img src="images/site-2010.jpg" alt="Clifton Railroad Corporation site in 2010" class="full-width-image">
        <p>By 2010, the color satellite imagery shows notable changes to the site, marking the beginning of a transition in its usage patterns:</p>
        
        <ul>
            <li>Warehouse structures remain intact, maintaining their original configuration</li>
            <li>More clearly defined storage areas and vehicle parking zones</li>
            <li>Some sections show reduced activity compared to the 1995 image</li>
            <li>Surrounding residential areas remain stable with little apparent change</li>
            <li>Increased vegetation visible along the site periphery</li>
        </ul>
        
        <p>This transition period coincides with broader economic shifts affecting industrial properties throughout northern New Jersey. While the site maintained operational functionality, the imagery suggests a less intensive use of certain areas compared to the earlier period.</p>
    </div>
    
    <div class="finding">
        <h3>Recent Past: Declining Industrial Activity (2020)</h3>
        <img src="images/site-2020.jpg" alt="Clifton Railroad Corporation site in 2020" class="full-width-image">
        <p>The 2020 satellite image demonstrates more pronounced changes to the site's usage:</p>
        
        <ul>
            <li>Continued operation of the main warehouse structures</li>
            <li>Significantly fewer vehicles and containers visible on the property</li>
            <li>Larger portions of the site appear underutilized</li>
            <li>Some areas showing apparent disuse or reduced maintenance</li>
            <li>Greater vegetation encroachment in peripheral areas</li>
            <li>Unchanged residential context surrounding the site</li>
        </ul>
        
        <p>This period reflects the continued decline in traditional industrial activities that has affected many similar properties in the region. While the site maintains some operational aspects, the imagery indicates substantial portions no longer support intensive industrial use.</p>
    </div>
    
    <div class="finding">
        <h3>Present Conditions: Underutilization and Opportunity (2024)</h3>
        <img src="images/site-2024.jpg" alt="Clifton Railroad Corporation site in 2024" class="full-width-image">
        <p>The most recent imagery from 2024 shows further evolution of the site:</p>
        
        <ul>
            <li>Warehouse structures still present but with visible signs of reduced activity</li>
            <li>Substantially decreased vehicle and material storage</li>
            <li>Large sections appear vacant or minimally utilized</li>
            <li>Maintained access to transportation infrastructure</li>
            <li>Stable surrounding residential context</li>
            <li>Continued integration with the urban fabric of Clifton</li>
        </ul>
        
        <p>The current state of the property reflects both the challenges and opportunities facing former industrial sites in urban New Jersey. While active operations have diminished, the site retains valuable characteristics including its size, location, and existing infrastructure.</p>
    </div>
    
    <div class="finding">
        <h3>Future Potential: Transit-Oriented Affordable Housing</h3>
        <p>Based on the observed transformation over nearly three decades, this site presents compelling opportunities for redevelopment, particularly for affordable housing. Key factors supporting this potential include:</p>
        
        <div class="potential-factors">
            <div class="factor-card">
                <h4>Strategic Location</h4>
                <ul>
                    <li>Positioned between established residential neighborhoods</li>
                    <li>Proximity to commercial corridors along major roadways</li>
                    <li>Access to transportation infrastructure</li>
                    <li>Integration with the existing urban fabric</li>
                </ul>
            </div>
            
            <div class="factor-card">
                <h4>Transit Accessibility</h4>
                <ul>
                    <li>Multiple NJ Transit bus routes serve the surrounding area</li>
                    <li>Connectivity to regional transportation networks</li>
                    <li>Potential for transit-oriented development</li>
                </ul>
            </div>
            
            <div class="factor-card">
                <h4>Development Potential</h4>
                <ul>
                    <li>Moderate site size of 3.076 acres - ideal for a compact, efficient housing development</li>
                    <li>Sufficient area to accommodate 90-150 affordable housing units (depending on density, design, and parking requirements)</li>
                    <li>Existing infrastructure including utilities and access points</li>
                    <li>Relatively flat topography suitable for construction</li>
                    <li>Potential for cohesive, single-phase development given the manageable site size</li>
                </ul>
            </div>
            
            <div class="factor-card">
                <h4>Community Integration</h4>
                <ul>
                    <li>Natural extension of surrounding residential zones</li>
                    <li>Opportunity to enhance neighborhood connectivity</li>
                    <li>Potential to add community amenities lacking in the area</li>
                </ul>
            </div>
        </div>
    </div>
    
    <div class="finding">
        <h3>Implementation Considerations</h3>
        <p>While the site offers significant potential, several important factors would need addressing in any redevelopment planning:</p>
        
        <div class="implementation-considerations">
            <div class="consideration">
                <h4>1. Environmental Assessment</h4>
                <ul>
                    <li>Former industrial sites typically require environmental study</li>
                    <li>Potential remediation needs based on historical rail usage</li>
                    <li>Opportunity for brownfield redevelopment funding</li>
                </ul>
            </div>
            
            <div class="consideration">
                <h4>2. Community Engagement</h4>
                <ul>
                    <li>Involvement of surrounding neighborhoods in planning process</li>
                    <li>Assessment of local housing needs and preferences</li>
                    <li>Integration with existing community character</li>
                </ul>
            </div>
            
            <div class="consideration">
                <h4>3. Infrastructure Capacity</h4>
                <ul>
                    <li>Evaluation of utility systems to support residential conversion</li>
                    <li>Transportation impact analysis</li>
                    <li>Stormwater management assessment</li>
                </ul>
            </div>
            
            <div class="consideration">
                <h4>4. Development Efficiency</h4>
                <ul>
                    <li>At 3.076 acres, the site is an optimal size for a single-phase affordable housing project</li>
                    <li>Small enough to be financially manageable for municipal or non-profit developers</li>
                    <li>Large enough to achieve economies of scale in construction</li>
                    <li>Suitable for comprehensive rather than phased development</li>
                    <li>Potential for quicker implementation timeline compared to larger properties</li>
                </ul>
            </div>
        </div>
    </div>
    
    <div class="finding">
        <h3>Conclusion</h3>
        <div class="conclusion-box">
            <p>The Clifton Railroad Corporation site illustrates the evolution of industrial properties in northern New Jersey over recent decades. From active industrial operations in 1995 to the current underutilized state in 2024, the changes visible in satellite imagery reflect broader economic transitions affecting similar properties throughout the region.</p>
            <p>The site now presents a significant opportunity for affordable housing development that could leverage existing infrastructure and transit accessibility while addressing community needs. At 3.076 acres, it offers an ideal scale for an efficient affordable housing project - large enough to make a meaningful impact on housing availability but small enough to be financially feasible for municipal or non-profit developers. Through thoughtful planning that respects both the site's industrial heritage and its urban context, this compact property could transform from an underutilized industrial remnant to a vibrant residential community serving Clifton's future.</p>
        </div>
    </div>
</section>

<style>
    /* Styles for the vacant site analysis section */
    #vacant-site-analysis {
        margin: 40px 0;
        padding: 20px;
        background-color: white;
        border-radius: 8px;
        box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    }
    
    #vacant-site-analysis h2 {
        color: #2c3e50;
        margin-bottom: 30px;
        border-bottom: 2px solid #f5f5f5;
        padding-bottom: 10px;
    }
    
    #vacant-site-analysis h3 {
        color: #2c3e50;
        margin: 25px 0 15px 0;
    }
    
    #vacant-site-analysis h4 {
        color: #3498db;
        margin: 15px 0 10px 0;
    }
    
    .finding {
        margin-bottom: 30px;
    }
    
    .full-width-image {
        width: 100%;
        height: auto;
        margin: 15px 0;
        border: 1px solid #ddd;
        border-radius: 4px;
    }
    
    .potential-factors {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        grid-gap: 20px;
        margin: 20px 0;
    }
    
    .factor-card {
        background-color: #f5f5f5;
        border-left: 4px solid #3498db;
        padding: 15px;
        border-radius: 0 4px 4px 0;
    }
    
    .implementation-considerations {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        grid-gap: 20px;
        margin: 20px 0;
    }
    
    .consideration {
        background-color: #f5f5f5;
        border-left: 4px solid #2ecc71;
        padding: 15px;
        border-radius: 0 4px 4px 0;
    }
    
    .conclusion-box {
        background-color: #e8f4f8;
        padding: 20px;
        border-left: 4px solid #3498db;
        border-radius: 0 4px 4px 0;
    }
    
    ul {
        padding-left: 20px;
        margin-bottom: 15px;
    }
    
    li {
        margin-bottom: 5px;
    }
    
    @media (max-width: 768px) {
        .potential-factors,
        .implementation-considerations {
            grid-template-columns: 1fr;
        }
    }
</style>

        <section id="limitations">
            <h2>Limitations and Further Research</h2>
            
            <p>This analysis has several limitations that could be addressed in future research:</p>
            
            <ul>
                <li><strong>Data Currency</strong>: Some demographic data may not capture recent changes in population or housing patterns.</li>
                <li><strong>Zoning Constraints</strong>: This analysis does not incorporate current zoning regulations that may limit development potential.</li>
                <li><strong>Environmental Factors</strong>: Potential environmental constraints on vacant parcels are not considered.</li>
                <li><strong>Market Dynamics</strong>: Current market conditions and developer interest are not fully captured.</li>
            </ul>
            
            <p>Additional data sources that would enhance the analysis include:</p>
            
            <ul>
                <li>Detailed zoning and land use regulations</li>
                <li>Utility infrastructure capacity</li>
                <li>Brownfield or contamination site data</li>
                <li>Housing permits and pipeline projects</li>
                <li>School enrollment and capacity data</li>
            </ul>
        </section>
    </main>
    
    <footer>
        <p>Created by Saba Akhavansadr | Topics in GIS | Spring 2025 | Professor Will Payne | Bloustein School of Planning and Public Policy, Rutgers University</p>
    </footer>
</body>
</html>
