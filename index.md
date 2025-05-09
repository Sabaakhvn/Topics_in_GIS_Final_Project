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
    <h2>Case Study: Clifton Railroad Corporation Site</h2>
    
    <div class="finding">
        <h3>Historical Evolution of a Key Redevelopment Opportunity</h3>
        <p>This analysis examines the Clifton Railroad Corporation property, a significant industrial site located in central Clifton that presents a compelling opportunity for affordable housing development. Through historical satellite imagery spanning from 1995 to 2024, we can observe how this site has transformed over time and envision its potential future.</p>
        
        <div class="timeline-container">
            <h4>Historical Transformation (1995-2024)</h4>
            <div class="timeline-grid">
                <div class="timeline-item">
                    <img src="images/site-1995.jpg" alt="Clifton Railroad Corp site in 1995">
                    <p class="timeline-caption">1995: Active railyard operations with extensive vehicle storage and warehouse facilities</p>
                </div>
                <div class="timeline-item">
                    <img src="images/site-2010.jpg" alt="Clifton Railroad Corp site in 2010">
                    <p class="timeline-caption">2010: Continued industrial activity with visible storage patterns</p>
                </div>
                <div class="timeline-item">
                    <img src="images/site-2020.jpg" alt="Clifton Railroad Corp site in 2020">
                    <p class="timeline-caption">2020: Signs of declining operations and partial vacancy appearing</p>
                </div>
                <div class="timeline-item">
                    <img src="images/site-2024.jpg" alt="Clifton Railroad Corp site in 2024">
                    <p class="timeline-caption">2024: Further reduction in activity with underutilized space</p>
                </div>
            </div>
        </div>
        
        <div class="site-analysis">
            <h4>Site Analysis</h4>
            <div class="site-features">
                <div class="feature-box">
                    <h5>Past: Industrial Heritage</h5>
                    <ul>
                        <li>Multiple warehouse structures aligned parallel to railroad tracks</li>
                        <li>Extensive paved areas for vehicle and container storage</li>
                        <li>Railroad sidings and spurs connecting to the main line</li>
                        <li>Material storage areas and loading zones</li>
                        <li>Part of Clifton's 20th century industrial development</li>
                    </ul>
                </div>
                
                <div class="feature-box">
                    <h5>Present: Declining Activity</h5>
                    <ul>
                        <li>Continued operation but with reduced activity</li>
                        <li>Fewer vehicles and containers stored on property</li>
                        <li>Some areas showing signs of disuse</li>
                        <li>Railroad connection remains but with diminished operations</li>
                        <li>Stable residential neighborhoods to east and west</li>
                    </ul>
                </div>
                
                <div class="feature-box">
                    <h5>Future Potential</h5>
                    <ul>
                        <li>Transit-oriented affordable housing development</li>
                        <li>Mixed-use development with community amenities</li>
                        <li>Brownfield redevelopment opportunity</li>
                        <li>Adaptive reuse of industrial structures</li>
                        <li>Green infrastructure and sustainable design</li>
                    </ul>
                </div>
            </div>
        </div>
        
        <div class="transit-advantages">
            <h4>Transit Accessibility Advantages</h4>
            <p>The site is ideally situated for transit-oriented development, with excellent accessibility to public transportation:</p>
            <ul>
                <li>Multiple NJ Transit bus routes within walking distance</li>
                <li>Strategic location between residential neighborhoods</li>
                <li>Proximity to commercial corridors and services</li>
                <li>Potential to strengthen transit connectivity in the area</li>
                <li>Aligns with state and regional transit-oriented development goals</li>
            </ul>
        </div>
        
        <div class="conclusion-box">
            <p>The Clifton Railroad Corporation site represents a significant opportunity to repurpose underutilized industrial land for affordable housing in a transit-accessible location. With thoughtful planning and community engagement, this property could become a model for transit-oriented affordable housing development that respects Clifton's industrial past while addressing present-day housing needs.</p>
        </div>
    </div>
</section>

<style>
    /* Styles for the vacant site analysis section */
    .timeline-container {
        margin: 30px 0;
    }
    
    .timeline-grid {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        grid-gap: 20px;
        margin-top: 15px;
    }
    
    .timeline-item {
        display: flex;
        flex-direction: column;
    }
    
    .timeline-item img {
        width: 100%;
        height: auto;
        object-fit: cover;
        border: 1px solid #ddd;
    }
    
    .timeline-caption {
        text-align: center;
        font-size: 0.9em;
        font-style: italic;
        margin-top: 8px;
    }
    
    .site-analysis {
        margin: 30px 0;
    }
    
    .site-features {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        grid-gap: 20px;
        margin-top: 15px;
    }
    
    .feature-box {
        background-color: #f5f5f5;
        border-left: 4px solid #3498db;
        padding: 15px;
    }
    
    .feature-box h5 {
        margin-top: 0;
        margin-bottom: 10px;
        color: #2c3e50;
    }
    
    .feature-box ul {
        padding-left: 20px;
        margin-bottom: 0;
    }
    
    .feature-box li {
        margin-bottom: 5px;
    }
    
    .transit-advantages,
    .development-recommendations {
        margin: 30px 0;
    }
    
    .conclusion-box {
        background-color: #e8f4f8;
        padding: 20px;
        border-left: 4px solid #3498db;
        margin: 30px 0;
    }
    
    @media (max-width: 768px) {
        .timeline-grid,
        .site-features {
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
                <li>Detailed parcel-level ownership information</li>
            </ul>
        </section>
    </main>
    
    <footer>
        <p>Created by Saba Akhavansadr | Topics in GIS | Spring 2025 | Professor Will Payne | Bloustein School of Planning and Public Policy, Rutgers University</p>
    </footer>
</body>
</html>
