Tutorial:

1. Files and Folders:
    ./TraceData/ticker + ".csv":  Raw Trace Data of each firm, once we get new Trace Data, please rename them to symbol.csv format, and save to this folder;

    ./par_data_empty/ticker + "_par.csv":  Bloomberg Par Amount and Par Values empty files, then copy them to the "par_data" folder to pull the Bloomberg data;

    ./TraceData_modified/ticker + "_modified.csv":  Trace Data after outliers eliminating and combining par amount and par values, it will be used in the main file to plot prices;

    Codes:
    "Get_Par.py":                       Generating the cusip lists to get par data (executable file); 
    
    "Outliers_Processing.py":           Outliers eliminating code based on our criteria (executable file);
   
    "main.py":                          Main executable file.

    "./Debugging Notebooks":            This folder contains all the debugging and experimenting jupyter notebooks I have. 


2. How to run through
Step1: Run the "Get_Par.py" to get cusip lists of each firm, it will generate an empty excel template file in ".\Data\par_data_empty" folder to be used in Bloomberg.  

Step2: Duplicate that "par_data_empty" folder, and rename as "par_data". In the "par_data" folder, pull out Par_Amt and AMT_ISSUED from Bloomberg to fill those "_par.csv" files ;

Step3: Run the "Outliers_Processing.py" to filter price outliers of those bonds based on our criteria ;

Step4: Run the "main.py" code to aggregate all and plot the prices.

Step5: All the plots are saved in "PricePlot" folder and their data are saved in "PricePlot_data" folder.