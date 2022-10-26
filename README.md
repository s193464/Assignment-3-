# Assignment 3
## Group 6 
## Gabriela Miti Tsuge Costa (s220075) & Kirstine Mia Odgaard (s193464) 

### Goal
The goal is to support the user to calculate the transmission loss, while making sure that the U-value is complied with BR18. 


### Use case
Finding the transmission loss is part of an energy analysis. This process is part of the BIM USE "Analyze", since it gives information about how much energy there is needed, to heat up the building. 
In order to analyze, it is necessary to gather information about the materials and thickness in the external walls.
With this analysis it is possible to validate if the U-value of the building complies with BR18.   

### Workflow 
3 BPMN
4 Description of BPMN 


### Information exchange 
5 Excel sheet 


#### IFC data: 
Being able to calculate the U-value and thereby transmission loss, it is necessary to get knowledge of the material layer and thickness in the externall wall. The transmission loss is also depended of the area of the externall wall, without the area of the windows. 

#### External sources: 
To find the U-value, the thermal conductivity (lambda value) must be found for each material. For this, DS418 is used. Furthermore, a knowledge of an internal and external transition insulation is needed. 
To validate if the U-value is low or high, BR18 is used, as this external source must be complied with.
 
#### Assumptions: 
To calculate the transmission loss, an indoor and outdoor temperature is also needed. It is assumed that the indoor temperature is 20 deg. and the outdoor temperature is -5 deg., as this is a standard for dimensioning temperatures in Denmark. 


### Value 
#### Business value
The tool will save the employees time when finding the thickness and materials of the wall. When using IFC, the risk of mistakes will be decreased, compared to finding the data manually by looking at drawings etc. 

#### Social value 
By ensuring that transmission loss complies with BR18, it is known, that an unnecessary amount of energy is not used to heat up the building. This helps to reduce the emission of CO2, which helps global warming.
in addition, it provides an economic advantage for the users of the building, as less energy is used and therefore less money on heating the building.


### Delivery 
#### Tools and use case 
In order to support the user to calculate the transmission loss, is the tool used to look up informartion of the external walls and their materials and thickness. When this data is used in combination with the thermal conductivity, it is possible to calculate an U-value. 
By extracting information about the area of the external wall, by IFC, along with the dimensioning temperatures and U-value, is it possible to calculate the transmission loss. 
The tool presents the transmission loss for the user.  

#### Steps 
To make this possible, following steps are needed: 
1. Check that the IFC file (Duplex A 20110907) contains necessary data regarding the external walls. 
2. Validate that wanted data is accessible in the external sources. 

Will use following to build the tool:

3. Python 
4. IFC openshell


Will use following equations:

5. U-value: 

![u-value](https://user-images.githubusercontent.com/112421127/197871610-8e1b2cac-8d11-4391-af1f-7c9930276962.jpg)

6. Transmission loss:   

![transmission loss](https://user-images.githubusercontent.com/112421127/197871580-e687ade0-2d40-458c-a4e3-5b4a77e3e419.jpg)

