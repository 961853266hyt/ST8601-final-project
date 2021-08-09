# ST8601-final-project

## Summary

####   Abstract



#### 1. Introduction

Augmented reality (AR) enables people to experience a 3D real-world environment where they can interact with 3D objects that exist in the real world. Augmented reality takes advantage of the information in the form of audio, graphics, and texts. The main goal of our project is to build an augmented reality application for android devices.  A social network is defined as several nodes that are tied by one or more types of relationships. Social networking applications, such as Facebook or Wechat, play an increasingly important role in accessing information and making contact with other individuals in our daily life. Our application aims to utilize social network services as our resources and collect profile photos from users. The application uses machine learning algorithms and deep-learning-based methods to capture, store, and analyze facial features to verify one's identity. Basically, the application can detect a person's face and render his/her name, followed by the name of a mutual friend of the person and the user. The scope of the application is allowing users to establish connections with new people by knowing their mutual friends in our application.

#### 2. Related Work 

 A Framework for Device–to–Device  Augmented Reality Social Networksummarize  

 They[2] defined two roles in an Augmented Reality Social Network (ARSN): promulgator and recipient.	It implemented the prototype on Android smartphones. To realize these functions, the most essential parts of the system are the Image Processing and the Dissemination Protocol.In this work, they designed and implemented Talk2Me, the first, to the best of our knowledge, distributed social network framework based on real–time augmented reality. Using Talk2Me, people can disseminate and receive information from people physically nearby in D2D fashion, and then view the information in an augmented reality way. 

#### 3. Solution Design

##### 3.1 face recognition module

face recognition module Face recognition is an innovative software that detects, analyzes, and verifies the identity of a face in a photo or video. It can be used as a face ID to unlock mobile phones or computers. As shown in the graph above, basically our face module has three phases of processing images that are captured by a camera. Detection is the process of finding an image: focusing on finding a human face based on the frame. Feature extraction is the second step that maps faces by determining the distinguishing elements of a unique face, including eyes distances, nose shapes, or lips. The final step is confirming the identity of a person and searching for the information of that specific person in our database. As deep learning methods can lead us accurate results, the team decide to apply Convolutional Neural Network (CNN) into our face recognition systems. [2] A convolutional neural network is made up of many layers and is mainly used for image processing, classification, and segmentation. The structure of CNN contains Convolutional, pooling, and fully connected layers. The figure below is shown how CNN works. 

##### 3.2 augmented reality module      

The augmented reality module is a significant part of our application to enhance the social connection, give our customers a clear, fresh, and wide view of the connection in daily communication. Our product more focuses on "discovering": base on the high-efficient facial capture technique combined with the camera, first the camera will capture a clear view of the object. By marking several points base on the face's capture, then the processor will build up a 3D model of the person and does a comparison. Once the comparison is done and the person has been recognized, for the user side, the user will get the name of the person and it friends or the people communicated recently. Furthermore, the user can determine if he wants to send a friend's add-on petition. 

#### 3.3 social network module

##### 3.3.1 definition of the social network

The social relationship network can be abstracted into an undirected graph without weight. Each person can be regarded as a node in the graph. If two people know each other directly, there is an edge between the two nodes. If two people know each other through several common friends, there is an indirect path between the two corresponding nodes.

![img](https://uploader.shimo.im/f/YHRROQ1Lgt7FpimG.png!thumbnail?accessToken=eyJhbGciOiJIUzI1NiIsImtpZCI6ImRlZmF1bHQiLCJ0eXAiOiJKV1QifQ.eyJhdWQiOiJhY2Nlc3NfcmVzb3VyY2UiLCJleHAiOjE2Mjc4MjAyODcsImciOiJLQ2tkcXhHUTZXVkdIOXFnIiwiaWF0IjoxNjI3ODE5OTg3LCJ1c2VySWQiOjI5MTA2NzcyfQ.LwsjdbdmhbRS_WLZDqy-d_q94OqgaQNgpYbWLTy2qY8)

3.3.2 

The above figure is a schematic diagram of the social network. Considering that there are two nodes A and C, we can see that the paths from A to C include A-D-C and A-D-B-C. although A and C can get to know each other through additional B, the path of A-D-C is the shortest, so we choose to display this relationship path in our application

#### 4. Solution implementation

4.1 client

We use unity as the main development software and vuforia as the SDK development package of AR.

4.3 server

We use alexnet in NVIDIA's digits for model training, and import the trained model into unity for use by the face recognition module. We haven't completed this part yet. 





##### 4.3.1 use of mysql database to store social network

MySQL Database Service is a fully managed database service to deploy cloud-native applications.**[3]**  We choose this databse because it has the advantages of small volume, high speed and low overall cost of ownership.Moreover, MySQL can run on multiple systems and supports multiple languages.

* design of table

![截屏2021-08-06 下午3.51.59](README.assets/截屏2021-08-06 下午3.51.59.png)There are mainly two tables in our MySQL database. One is called network, which stores the structure of social network in the form of adjacency matrix, and the other is userinfo, which stores some users' personal information. It is worth noting that we use blob instead of path to store users' personal photos, The reason is that once the physical way of storing pictures changes, it is troublesome to modify the face picture field in each piece of data.















4.3 Breadth-First Search used in finding the shortest path between two users

#### 5. lessons learned and beyond   

 Although we claim that the internet is "separate" people, the rise of social applications which insisted by powerful network uplink we can create looks separate but more dynamic and strongly close network-based society for all our customers. Furthermore, we will more focus on providing more convenient services, more interesting techniques and functionalities combine with improving screens, more reliable and advanced processors.  















#### 6. conclusion

This proposal presents a photo-based augmented reality application that can match phones against contents in a database of images. we aim to establish a connection between new people through face recognition and social network. In the future, we will focus on the development and improvement of our application within a limited time. our team will test the reliability and compatibility on the Android platform. We also plan to add more features to our application, such as showing the shared interest of a stranger and the user. Furthermore, we would take privacy issues into considerations since our application requires permission of accessing the address book on the mobile phone.  

#### 7. reference

[1] Talk2Me: A Framework for Device–to–Device  Augmented Reality Social Network

[2] Face Recognition Based on Convolutional Neural Network

[3] https://www.mysql.com/