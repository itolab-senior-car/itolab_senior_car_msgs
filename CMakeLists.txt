cmake_minimum_required(VERSION 2.8.3)
project(itolab_senior_car_msgs)

find_package(catkin REQUIRED COMPONENTS
	message_generation
	std_msgs
	geometry_msgs
	sensor_msgs
	jsk_recognition_msgs
)


 add_message_files(
   DIRECTORY msg
   FILES
   Centroids.msg
   CloudCluster.msg
   CloudClusterArray.msg
   ControlCommand.msg
   ControlCommandStamped.msg
   DetectedObject.msg
   DetectedObjectArray.msg
   DTLane.msg
   JoyCon.msg
   Lane.msg
   LaneArray.msg
   RegionObserver.msg
   RegionObserverArray.msg
   Servo.msg
   VehicleStatus.msg
   Waypoint.msg
   WaypointState.msg
 )

 generate_messages(
   DEPENDENCIES
   std_msgs
   geometry_msgs
   sensor_msgs
   jsk_recognition_msgs  # Or other packages containing msgs
 )

catkin_package(
        CATKIN_DEPENDS
        message_runtime
        std_msgs
        geometry_msgs
        sensor_msgs
        jsk_recognition_msgs
)
