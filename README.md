# Soccer Prediction Project
The soccer project is aimed to predict soccer games using previous game results data. 

## Steps
1. uploading raw data
```
uploaded = files.upload()
for fn in uploaded.keys():
  print('User uploaded file "{name}" with length {length} bytes'.format(
      name=fn, length=len(uploaded[fn])))
```
2. Reading uploaded file
```
df = pd.read_csv("soccer.csv")
```
3. Change full-time and half-time result to numbers 
* Win = 1
* Loose = -1
* Draw = 0
4. Determine Home and Away strength of each team based on the goal scored and conceded.
 ###### Note: Home Attacking Strength(HAS), Home Defensive Strength(HDS), Away Attacking Strength(AAS), and Away Defensive Strength(ADS)
* HAS = (HGS / Number of Games) / Average of Home Scored
* AAS = (AGS / Number of Games) / Average of Home Scored
* HDS = (HGC / Number of Games) / Average of Home Scored
* ADS = (AGC / Number of Games) / Average of Home Scored
5. Visualiation of Team Strength (Eaxample with HAS)

![image](https://user-images.githubusercontent.com/37972518/118472298-e8792c80-b6c5-11eb-83db-58ae099b0548.png)

6. Setting the x_train and y_train to get the prediction model. Library used are:
* Tensorflow
* sklearn
* xgboost
7. Training and Testing the models
8. Used model to predict upcoming games. 

## Limitations
There so many recent developments team performance such as signing new player, signing new manager, Current form of the players, and unexpected injuries. We hope to consider this factors in the future.



