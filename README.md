# NPOL-RF-Retrievals

Random forest retrievals of DSD properties for NPOL radar. 

Added to GitHub for reproduction of results of Conrick et al. (2019).<br /><br />
If you use these objects, please cite: <br />
<i>Conrick, R., J.P. Zagrodnik, and C.F. Mass, 2020: Dual-polarization radar retrievals of coastal Pacific Northwest rain drop size distribution parameters using random forest regression. J. Atmos. Oceanic Technol., 37, 229–242.</i>
<br />

<b><u>Update</u> January 26, 2022</b>
Please ensure scikit-learn version 0.21.3 is installed prior to use. Newer versions of scikit-learn have changed the way that random forests are called, so loading the pickle files will throw an error.



<b><u>Update</u>:  August 29, 2019</b>
GitHub does not allow large files, so the TAR.GZ file is now hosted on UW Atmospheric Sciences Servers:  https://www.atmos.washington.edu/~rconrick/RF/
Download it there and follow the instructions below.



<b>File Format</b>
The tar.gz file contains three Python pickle files (RF_D0.pickle, RF_RR.pickle, RF_LWC.pickle) each for retrieving D0, Rain rate (RR), and LWC, respectively, from NPOL observations of Z,ZDR.

<b>Use</b>
1.   Unpack into a working directory.
2.   Load *.pickle files using Python.
3.   Each pickle file contains an instance of Scikit-learn's Random Forest Regressor object.
4.   Consult the Scikit-learn site for appropriate methods to use:  https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestRegressor.html
     To produce a retrieval from radar data, use: RF.predict(ZDR,Z) , where RF is the previously loaded instance for D0 or LWC.
        where ZDR is the NPOL Differential reflectivity. Z is the NPOL reflectivity.


<b>For Support or Questions, contact Robert Conrick (rconrick@uw.edu)</b>
