# undergraduate_sustainability
Code for assessing undergraduate teaching lab experiments by relevant sustainability metrics.

This code is set up to calculate the Average Yield, Product Mass, Mass Efficiency, Effective Mass Yield, Mass Intensity, Sum of Waste and E-factor for each of the experiments using data about the yields achieved and the experiments input from the csv files. 

The example csv files "Y1_Yield_data" and "Y1 Reactions" show how the data needs to be organised for the percentage yield data and reaction data respectively, to then be used by the code. 

"Y1_Yield_data" contains 2 columns, the first containing the reaction codes, and the second containing the percentage yield values.

"Y1 Reactions" contains 5 columns, titled "Reaction", "Theoretical yield", "Mass of reactants", "Mass of hazardous reagents", and "Total mass in process".

- "Reaction" - the reaction code for the experiment, which will be the same as the one used for the yield values.
- "Theoretical yield" - the theoretical yield of the reaction, if 100% yield was achieved.
- "Mass of reactants" - the mass of the reactants used in the experiment - excludes solvents, work up and purification.
- "Mass of hazardous reagents" - the mass of reagents that are hazardous - excludes solvents, work up and purification.
- "Total mass in process" - the total mass used in the experiment - includes solvents, work up and purification.

You can input your reactions into the AI4Green ELN (https://ai4green.app/) as a useful tool to highlight which reagents are hazardous, and it will also be able to provide more insights about sustainability of your reaction, including atom economy, as well as highlighing the impacts of conditions of reactions. 

To use the code, copy the two file locations into the bracets of df_yield_data = pd.read_csv(r"C:\Users\imoge\Y1_Yield_Data.csv")  and df_exp = pd.read_csv(r"C:\Users\imoge\Y1 Reactions.csv") in the first cell to replace "C:\Users\imoge\Y1_Yield_Data.csv" and "C:\Users\imoge\Y1 Reactions.csv". 

Then run all cells, and this will produce a csv file called "metrics.csv" and will generate a set of graphs that can be downloaded. 
