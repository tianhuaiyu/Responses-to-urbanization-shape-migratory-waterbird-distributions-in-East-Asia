# Responses-to-urbanization-shape-migratory-waterbird-distributions-in-East-Asia
Code for: Differential responses to urbanization shape migratory waterbird distributions in East Asia

## Abstract
Urbanization has profound impacts on the abundance and distribution of animals, exemplified by dramatic global declines of migratory bird abundance and biodiversity. Understanding how migratory animals interact with urban habitats during their annual cycles is crucial to their conservation, yet obtaining sufficient behavioral data at the individual level across species and landscapes has proved challenging. Here, we study the annual cycles of 19 species of migratory waterbirds across the imperiled East Asian flyway, a geographic region under intense threat from human activities that is understudied yet critically important for conservation. Data from miniaturized GPS devices reveal that birds’ interactions with urban areas depend strongly on the degree of development in the surrounding landscape. In urbanized east China, tracked birds were most likely to occur away from cities, whereas those in less developed and more arid western regions selected habitats close to cities during migration and wintering periods. Our results show that birds’ responses to developed areas are spatially heterogeneous and vary with surrounding habitat availability, and that wildlife may occur in close proximity to urbanization when local areas provide an otherwise limiting resource. Sustainable development must incorporate information on local landscapes and carefully consider environmental context. Furthermore, the opportunity to characterize individuals’ movements with respect to human activities embodies unique information for dynamic conservation at local, region, and continental scales.

## Notes on the code
To run, you need to configure the python environment: python version  3.6.12. We used the python packages pandas (v. 1.1.3), xgboost (v. 1.2.1), numpy (v. 1.19.2), matplotlib (v. 3.3.2), Seaborn (v. 0.11.0), scikit-learn (v. 0.23.2),  netCDF4 (v. 1.4.2), GDAL (v. 3.1.4), geopandas (v. 0.6.1), PDPbox (v. 0.2.0), Shapely (v. 1.6.4.post1),jupyter lab(v 2.2.0a1).

## Descriptions for the scripts
All scripts are placed in the Folder code. The following guides will help you to reproduce the main results in the paper. All code should run in jupyter lab or jupyter notebook.
1. Clone this project into your local directory
2. Reproduce the analysis in Fig.2a and Extended Data Figure 11-12. modeling/East_model.ipynb and modeling/West_model.ipynb.Results will be generated in the Folder result/figure/1d_pdp and result/figure/2d_pdp. In addition, the source data of these figure will be generated in the Folder result/figure_data.
3. Reproduce the analysis in Fig.2b. The first step is to add noise to gps points, spatial-scale-analysis/add-noise-gpspoints.ipynb accomplishes this step.Results will be generated in the Folder spatial-scale-analysis/noise-added-point;The second step is to match the random latitude and longitude coordinates of these points with various environment variable data, the result could be finded in the Folder spatial-scale-analysis/noise-added-dataset;The third step is modeling the dataset which was added some noise, modeling_noiseadded.ipynb accomplishes it, results will be generated in the Folder spatial-scale-analysis/noise-added-dataset/xxx/x/plot; finally, figure2b.ipynb generate figure2b and Extended Data Figure 7 in the folder spatial-scale-analysis/noise-added-dataset/noise_added_pdp.
4. The code reproduce the analysis in Extended Data Figure 2 was stored in code/modeling/ArcossChina_model.ipynb.Results will be generated in the Folder result\figure\Different-ALAN.
5. The code reproduce the analysis in Extended Data Figure 3 was stored in code/modeling/season_group_east.ipynb, code/modeling/season_group_east.ipynb and the draw code was code/modeling/plot_season_pdp.ipynb.Results will be generated in the Folder result/figure/season_pdp.The source data of these figure will be generated in the Folder result/figure_data/season_pdp.
6. The code reproduce the analysis in Extended Data Figure 9 was stored in code/importance/importance_plot.ipynb.Results will be generated in the Folder result/figure/importance.The source data of these figure will be generated in the Folder result/figure_data/importance
7. The code reproduce the analysis in Extended Data Figure 13 was stored in code/modeling/Threshold-value-ALAN.ipynb.Results will be generated in the Folder result/figure/importance.


## Descriptions for folders
Folder data contains the main data used in this study.  
Folder code contains the main analysis code used in this study.  
Folder result contains outputs of the scripts.  

## Data
### GPS trajectory data
We used the bird trajectory dataset collected by the Chinese Academy of Forestry from October 2006 to April 2019. The logger devices include YH-GTG0306, YH-GTG0312, YH-GTG0317, YH-GTG0325, YH-GTG0330 for migratory bird species with different body mass (Hangzhou Yuehai Technology of China, Zhejiang), the devices were solar powered and programmed to position by Global Position System (GPS) every 2 hrs, continuously document location data acquisition via the global system for mobile communications (GSM). These logger devices have different recording frequencies according to the type. The trajectory dataset includes major large and medium-sized waterbirds such as Anseriformes, Storks, Cranes, Gulls, Plovers, covering major migratory bird habitats throughout China.

#### Due to some reasons, all accurate points, including GPS points without preprocessing,GPS points with species, object and device ID, cannot be disclosed. Therefore, the dataset  of supplementary Figure 4-6,10 cannot be disclosed. If you have needs, please contact tianhuaiyu@gmail.com (H.T.)

