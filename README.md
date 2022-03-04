# Babble Dataset

by Hooman Hedayati, Annika Muelbradt, Daniel Szafir and Sean Andrist


### Introduction

<p align="center">
    <img src="https://github.com/cu-ironlab/Babble/blob/master/media/Babble-gif.gif" width="900">
    <br>
    <sup>Babble Dataset</sup>
</p>

> *An F-formation arises whenever two or more people sustain a spatial and orientational relationship in which the space between them is one to which they have equal, direct, and exclusive access.*
> [A. Kendon, 1990]

The Babble dataset consists of a 35-minute recording of conversational interactions between 7 individuals with precisely recorded head and body positions and orientations via the Vicon motion-tracking system and a portion of it is labeled F-formations from two annotators. Babble dataset has a total of 3481 frames with 3 photos assigned to each frame.

### Citing Babble Dataset

If you find Babble useful in your research, please consider citing:

	@inproceedings{hedayati2020reform,
		title={Reform: Recognizing f-formations for social robots},
		author={Hedayati, Hooman and Muehlbradt, Annika and Szafir, Daniel J and Andrist, Sean},
		booktitle={2020 IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS)},
		pages={11181--11188},
		organization={IEEE}
	}


### Data


* \Images\
The "Images" folder has 3481 photos of the conversational group that has been taken roughly every second. The name of the file is the "frame number" followed by the time that the image was taken.  (e.g., "1687 2019-25-9--18-04-44.jpeg" means that the frame number is 1687 and the photo is taken on 2019/25/9 at 18:04:44)

The "frame number" is useful for accessing the position and orientation of people in the conversational group.

corrupted images: #26,3460,3461,3462,3463

* \Motion-capture-data.csv
There are 3482 lines in this file. The first row is the name of the columns. The next 3481 rows (2 to 3482) are the frames associated with the photos in the "Images" folder. 
Each row has the data of participants like the following: {[data of participant1],[data of participant2],[data of participant3] ... [data of participant7]}
Each participant has 10 fields as follows [Name,HeadX,HeadY,HeadRotation,TorsoX,TorsoY,TorsoRotation,Hieght,FrameNum,Time]

Name: This is the ID of the participant. This is the number written on their hat and upper body. This starts from 1 and goes to 7. The ID of the participant does not change and it's unique. 
HeadX: X position of the head which is in meters. (the 0,0 is the center of the room)
HeadY: Y position of the head which is in meters. (the 0,0 is the center of the room)
HeadRotation: Head orientation which in gradient.
TorsoX: X position of the torso which is in meters. (the 0,0 is the center of the room)
TorsoY: Y position of the torso which is in meters. (the 0,0 is the center of the room)
TorsoRotation: Torso orientation which in gradient.
Hieght: Z position of the head which is in meters.
FrameNum: This is the frame number provided by the Vicon System motion capture camera ( PLEASE IGNORE THIS FIELD as it might be confusing with what we called as "frame number")
Time: The timestamp of the frame provided by the Vicon system.

Important: Please note that when all the columns for a participant is [HeadX,HeadY,HeadRotation] or [TorsoX,TorsoY,TorsoRotation] is all zeros e.g.,{0,0,0] it means that either the participants is not in the scene or the motion capture camera can not detect it. 


* \features.mat
It is a cleaned-up version of the "Motion-capture-data.csv" file. Since we used the Graphcut algorithm as our baseline, we made the position and orientation of participants compatible with the Graphcut implementation in Matlab by Francesco Setti( can be found https://github.com/franzsetti/GCFF). If you copy it in the "GCFF" folder, it should work. The original "features.mat" by Setti has four columns : [ID, x, y, orientation]. Our features.mat hast 3 additional columns 
[ ID, Head x, Head y, Head orientation , Torso x, Torso y, Torso orientation]

* \annotated-frames.csv
It has the f-formations ground-truth annotated by two annotators. The first column is the "frame number" and the second column is the id of the participants who are in an F-formation. e.g.,  in the 75th row of the file, the data is 2675, {[3 4 7]} which means in the "frame number" 2675, there is only one F-formation and the participants with ids 3,4 and 7 are in it. 




### Contacts

For any problem by using this with the dataset, please send an email.







