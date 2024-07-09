# Exploring-Turtlesim-Package
This repository is going to explore turtlesim package and define nodes, topics, and services using this package.
# Nodes
- Follow the following steps/
1) Call the master node by typing: roscore
2) Open a new terminal and type this statement: rosrun turtlesim turtlesim_node
 - As shown in image, a turtle robot will appear.
     
![turtlesim](https://github.com/ProShaden/Exploring-Turtlesim-Package/assets/174384069/9747ce94-2541-4fb3-9001-1109f948d001)

3) To show all the nodes that turtlesim package has, open a new terminal and type rosrun turtlesim and click tab twice. 
  - As shown in image, these are the nodes of turtlesim package.

![nodes](https://github.com/ProShaden/Exploring-Turtlesim-Package/assets/174384069/0ec468b7-a3b2-4bdc-b18d-a9c29fe972f0)

4) Let's try the following node: turtle_teleop_key

- To use turtle_teleop_key, type the following statement: rosrun turtlesim turtle_teleop_key
- As shown in image, we used this node to draw from the arrows in the keyboard.

![teleop](https://github.com/ProShaden/Exploring-Turtlesim-Package/assets/174384069/82d06c57-5ac8-4f50-8632-86c1833d4094)

5) Finally, we can use this command: rqt_graph to graph the program. Let's see how it will graph nodes based on turtle_teleop_key program.
- As shown in image, we can see that nodes are represented as oval figure.

![rqt nodes](https://github.com/ProShaden/Exploring-Turtlesim-Package/assets/174384069/02b0ebfd-964e-48cf-bc32-0fa6426955f5)

- So what are ROS nodes? simply it is any program that you can create with code.

# Topics 
- Follow the following steps/
1) Call the master node by typing: roscore
2) Open a new terminal and type this statement: rosrun turtlesim turtlesim_node
 - As shown in image, a turtle robot will appear.
     
![turtlesim](https://github.com/ProShaden/Exploring-Turtlesim-Package/assets/174384069/9747ce94-2541-4fb3-9001-1109f948d001) 

3) To show all the nodes that turtlesim package has, open a new terminal and type rosrun turtlesim and click tab twice. 
  - As shown in image, these are the nodes of turtlesim package.

![nodes](https://github.com/ProShaden/Exploring-Turtlesim-Package/assets/174384069/0ec468b7-a3b2-4bdc-b18d-a9c29fe972f0)

4) Let's try the following node: draw_square

- To use draw_square, type the following statement: rosrun turtlesim draw_square
-  As shown in image, we used this node to make the turtle draw a square.

![turtle square](https://github.com/ProShaden/Exploring-Turtlesim-Package/assets/174384069/ca2a4255-76f3-41eb-a36c-2d95a41ea0b1)

5) Finally, we can use this command: rqt_graph to graph the program. Let's see how it will graph nodes and topics based on draw_square program.
- As shown in image, we can see that nodes are represented as oval and topics as rectangle.
  
![nodes-topics](https://github.com/ProShaden/Exploring-Turtlesim-Package/assets/174384069/f709541a-4208-4115-9695-6fb01ad1230e)

- From the rqt graph, we have a turtlesim node that is responssible for the turtle and graphical interface and another node which is draw_squre that controls the turtlesim node by publishing commands and also listening to topics.
- draw_square node will listen to the topic: position of the node (/turtle1/pose) where turtlesim sends its position to draw_square node.
- Then draw_sqaure node will publish command velocity(/turtle1/cmd_vel/) and turtlesim is a subscriber of cmd_vel topic so it'll receive new commands from draw_square node.

- So what are ROS topics? they are the way to communicate between different nodes because nodes don't directly communicate they just publish or subscribe.

# Services
- Follow the following steps/
1) Call the master node by typing: roscore
2) Open a new terminal and type this statement: rosrun turtlesim turtlesim_node
 - As shown in image, a turtle robot will appear.
     
![turtlesim](https://github.com/ProShaden/Exploring-Turtlesim-Package/assets/174384069/9747ce94-2541-4fb3-9001-1109f948d001)

3) To show all the services that turtlesim package has, open a new terminal and type rosservice list.
  - As shown in image, these are the services of turtlesim package.

![services](https://github.com/ProShaden/Exploring-Turtlesim-Package/assets/174384069/03541063-58a1-4ba8-a868-8e926f3762a8)

- Let's try the first service: /clear with turtle_teleop_key program.
- Before:

![c1](https://github.com/ProShaden/Exploring-Turtlesim-Package/assets/174384069/a0913fbd-5fad-499f-a240-893a9a487c72)

-After: 

![c2](https://github.com/ProShaden/Exploring-Turtlesim-Package/assets/174384069/baa20b00-0350-4f9b-a84f-ea8097fac8a5)

- So what are ROS services? they are requests to change settings.

# Good tutorials 
- ROS nodes: https://www.youtube.com/watch?v=4aUp2703FFY&t=7s
- ROS topics: https://www.youtube.com/watch?v=GAJ3c5XmJSA
- ROS services: https://www.youtube.com/watch?v=0nGzvefzl-U
