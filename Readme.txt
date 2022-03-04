Please contact cuironlab@colorado.edu to gain access to the dataset.

Citation:
@inproceedings{hedayati2020reform,
  title={Reform: Recognizing f-formations for social robots},
  author={Hedayati, Hooman and Muehlbradt, Annika and Szafir, Daniel J and Andrist, Sean},
  booktitle={2020 IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS)},
  pages={11181--11188},
  organization={IEEE}
}


What's in the dataset:

\Images\
The "Images" folder has 3481 photos of the conversational group that has been taken roughly every second. The name of the file is the "frame number" followed by the time that the image was taken.  (e.g., "1687 2019-25-9--18-04-44.jpeg" means that the frame number is 1687 and the photo is taken on 2019/25/9 at 18:04:44)

The "frame number" is useful for accessing the position and orientation of people in the conversational group.

corrupted images: #26,3460,3461,3462,3463

Motion-capture-data.csv
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

