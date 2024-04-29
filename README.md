[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/g_e38bz1)
# Final Project for ENV 617 2024

## Importance of the project 
Urban tree cover is important for many reasons, ranging from public health to climate adaptation and mitigation. In New Haven, CT, one of the major agents in urban greening and tree planting is the Urban Resources Initiative (URI), a university-non profit partnership with Yale University. URI has been planting trees along streets and in parks across New Haven for almost 20 years, while also producing research focused on the practice of urban forestry. Recently, URI received a large ($2.6 million) grant from the United States Department of Agriculture’s Urban and Community Forestry Grant Program to plant more trees, specifically focusing on historically underserved, low-canopy neighborhoods. This essentially doubles the tree-planting goals that URI has, in terms of the number of trees planted, over the next five years. With this context, our aims in this project are understand how street trees vary across New Haven, particularly as a result of specific management and planting choices, to both understand the impact of URI's work, and to provide insights that might guide planting decisions in the future.

We do this through three seperate analyses. 



   



### Wire component 
URI only plants shade trees (trees which will grow very tall) in sites that do not have powerlines overhead, because conflict with powerlines are thought to lead to lower tree health due to heavy pruning. This analysis explores the impact of powerlines on tree health, as well as the implications of URI's decision to not plant tall trees under powerlines. A more detailed narrative can be read within the notebook.

### Biodiversity component 
URI prioritizes the diversity of tree species, avoiding planting too many individual trees of a single species or even a single genus in a small, localized area. The impact of emerald ash borer on white ash can exemplify the reason for this strategic approach. The outbreak of a pest or disease can cause detrimental effects on tree canopies when too many individuals are susceptible to that pest or disease and are planted in one location. 

Throughout the years, New Haven has experienced almost total canopy loss of affected species from different pests and diseases such as emerald ash borer, chestnut blight, and Dutch elm disease. 

URI aims to protect the trees by maintaining high levels of biodiversity, which will reduce and spread out the impact of future disturbances.
The biodiversity component of our project aims to understand the current levels of biodiversity and tree conditions in New Haven and to assess to what degree URI has succeeded.

#### Questions:
•	What is the most common tree species in New Haven?

•	What is the most biodiverse neighborhood in New Haven (street trees)?

•	What is the condition of street trees in New Haven?

### Canopy component
(Allen's part)

## Data Sources 
1. all_trees_58_1712257580.csv: This is a csv containing all the tree datapoints from New Haven's online tree inventory (https://newhavenct.treekeepersoftware.com). It contains the following information:
    # Site_ID: A unique identification number for each individual tree point
    ### Latitude: Latitude of the tree point
    ### Longitude: Longitude of the tree point
    ### Latin_Name: Latin (scientific) name of the tree at the point
    ### Common_Name: Common name of the tree at the point.
    ### Condition: A semi-qualitative assessment of the tree.
     Values are Stump, Standing Dead (a dead or nearly dead tree <10% of canopy remaining), Very poor (a badly declining tree, <50% of canopy remaining,       likely hazardous), Poor (a declining tree, <60% of canopy remaining, possibly hazardous), Fair (A stable tree, <75% canopy remaining), Good (A            healthy tree, at least 90% of canopy remaining), and Excellent (An exceptional tree, full or nearly full canopy).
     NOTE: Canopy percentages are guidelines and not hard rules, especially since assessments are estimates by trained students and not formal                 measurements. Other criteria can be incorportated, such as the presence and load of pests or pathogens, structural injury, and misshappenness
    ### DBH: Diameter (in inches) at Breast Height (1.3m above the ground)
    ### Wire: yes= utility wires above the tree, no= no utility wires above the tree
    ### Grow_Space: The type of space (e.g., tree pit, yard) the tree is in.
    ### Organization: The organization which planted the tree
    ### Neighborhood: The neighborhood the tree is planted in
    ### Planted_Date: The date, if known, of planting
    ### Department: The juristriction overseeing a tree (e.g. Yale Facilities, Parks Dept.)
    ### Latin_Genus: Genus of tree
    ### Common_Genus: Common name genus of tree
    ### Last_Editor: Editor who last made changes to the point in the treekeeper software
    ### Sites: Duplicate variable of Site_ID

2. all_trees_58_1713995132.csv: This CSV is a duplicate of all_trees_58_1712257580.csv, but with the additional field:
    ### Valuation_Total: An estimate of the value of the tree (in USD). Calculated using the I-tree eco tool which is intregated into the treekeeper           software. (information about I-tree eco: https://www.itreetools.org/tools/i-tree-eco)
   
3. Neighborhoods.zip: A .zip containing shapefiles for neighborhoods in New Haven.

## Notebooks 
The project is organized in three notebooks:
1. Wire Component: Les_UtilityLines.ipynb
2. Biodiversity Component: Final_Project_URI_trees
3. Canopy Component: 
