# From ARTMO GPR to GEE.

Short tutorial demonstrating how to import ARTMO GPR models into GEE.

As done in 

https://doi.org/10.3390/rs14010146

![image](https://user-images.githubusercontent.com/9076763/169662944-b7b6f85d-8251-4839-9d97-0b65d3e882fa.png)

## Prerequisites
- ARTMO GPR model (.mat). As [this one](https://github.com/msalinero/ARTMOtoGEE/tree/main/exampleModel).
- [Matlab files](https://github.com/msalinero/ARTMOtoGEE/tree/main/src) that parse the .mat file into txt.
- Add the sample repository to your GEE account using this [link](https://code.earthengine.google.com/?accept_repo=users/msalinero85/ARTMOtoGEE). Refresh so you can see this repo under the Reader section.
![image](https://user-images.githubusercontent.com/9076763/201699108-03aff210-5a97-4500-b84b-010558e79f7b.png)

## Sample scenario for Sentinel-2.
1- Place the 2 .m files in the same folder.
![image](https://user-images.githubusercontent.com/9076763/201688583-46dc78b9-7ef7-4b93-ac91-d1fffabafe52.png)
2- Modify Main.m with the path of the ARTMO GPR .mat model and the desired suffix.
![image](https://user-images.githubusercontent.com/9076763/201688079-072433b8-6585-4879-b55a-c2234c5fd2a4.png)
3- Run Main.m. It will generate a folder in the same location as the ARTMO GPR .mat model with several .txt files.
4- Open overall_model_gee.txt. and copy its content. Paste it at the beggining of the GPRPredictedMean script in the GEE repository.
![image](https://user-images.githubusercontent.com/9076763/201699499-c7fac517-b48d-4e6c-81c0-e0973891b273.png)
5- Run it!

**Important** The correspondence between the variables in the veg_index_GPR function should be preserved if the suffix changes.  


