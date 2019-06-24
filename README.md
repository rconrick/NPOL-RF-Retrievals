# NPOL-RF-Retrievals

Random forest retrievals of DSD properties for NPOL radar. 

Added to GitHub for reproduction of results of Conrick et al. (2019) submitted to JTech on June 24, 2019.


<b>File Format</b>
The tar.gz file contains two Python pickle files (RF_D0.pickle and RF_LWC.pickle) each for retrieving D0 and LWC, respectively, from NPOL observations.

<b>Use</b>
1.   Unpack into a working directory.
2.   Load *.pickle files using Python.
3.   Each pickle file contains an instance of Scikit-learn's Random Forest Regressor object.
4.   Consult the Scikit-learn site for appropriate methods to use:  https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestRegressor.html
     To produce a retrieval from radar data, use: RF.predict(ZDR,Z) , where RF is the previously loaded instance for D0 or LWC.
        where ZDR is the NPOL Differential reflectivity. Z is the NPOL reflectivity.


<b>For Support or Questions, contact Robert Conrick (rconrick@uw.edu)</b>