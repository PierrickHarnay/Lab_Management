For Eco-Phys data, you want to be mindful and be managing your data at all stages of it's life. This is during the gathering process, analysis, and ultimately archival. Eco-phys data includes data such as shell size, ash-free dry weight, symbiont cell counts, bleaching score, total protein, and many others. Basically all data we generate/gather that is not DNA/RNA sequence based. Images are slightly different, although eco-phys data may come from them (ie. bleaching score) _wiki on image data management in process_
### Main steps for data management and gathering are depicted graphically below:
![](https://raw.githubusercontent.com/Putnam-Lab/Bioinformatic_and_Data_Resources/master/images/ecophys-data-preprocess-5.jpg)

**Stage 1** You will always have a raw data stage, although some data will be more "raw" than others. This is most likely written data, either in your notebook or on printed spread sheets. This could also be an original excel/csv file if data gathering came from imgageJ. This can also be data exported directly from equipment, such as the plate reader.
To the best of your ability, collect all the data you mean to collect! If you do fail to collect data for whatever reason, do not leave that observation or omit that sample in your data. Include that individual in your dataset and say NA in the cell for the value.
Your lab notebook is where the metadata lives for this stage, where all notes and steps taken for data collection are written down. If you have NA for some observation, the reason why goes here. You should also include the initials of the data collector for each observation (most important when it is multiple people).

**Stage 2** is a data organizing and compiling stage. You may need to add data from multiple days/weeks into one spreadsheet. You may need to re-format the output of a piece of equipment to be in a format that you can input into R or other analysis software.
At this stage, it is pertinent to follow [Best Practices for Spreadsheets](https://github.com/Putnam-Lab/Bioinformatic_and_Data_Resources/wiki/Best-Practices-for-Spreadsheets). When transferring data, whether it be from paper to computer or one spreadsheet to another, always triple check that everything transferred successfully. Be aware of the number of columns and rows you expect to have.
At this stage you also need to compile and organize your metadata. Include dates of collection, who collected the data, methods used, equipment specs, and a data dictionary for terms and abbreviations in your main data spreadsheet. Once you have done this you should save a write-protected version of this data as a cleaned initial dataset.

**Stage 3** This stage encompasses everything from the formal dataset onward. Once you are ready to explore and analyze your data, you are ready to create a Github repository and and R Project. At this point, all of our eco-phys data analysis is done in R, so an R Project is a necessity.
To create a github repository follow [these instructions](https://help.github.com/en/github/getting-started-with-github/create-a-repo). Use the README.md file to include an overview of your efforts for data collection and analysis. Inside your github repo you will create and RAnalysis folder. See [this great example](https://github.com/SamGurr/Juvenile_geoduck_OA) of a repo structure from Sam Gurr. Inside the RAnalysis folder your R project will live. When you go to start your analysis in R, you will create and [R Project](https://support.rstudio.com/hc/en-us/articles/200526207-Using-Projects). Look at that page to get a detailed description of what an R Project is. In short, using R projects provides a centralized location for all files associated with an analysis, and all scripts for doing an analysis.
If you were to give your RAnalsyis folder to any collaborator they could completely reproduce your results with everything provided in that folder. That folder will have 3 main components. A **Data** folder where your data spreadsheets and metadata are stored. A **Scripts** folder where all analysis scripts are stored. And an **Outputs** folder where all figures, tables, and other files generated in your scripts are written to.
It is your responsibility to push changes in these files after every time you save/create a file to Github for version control. 