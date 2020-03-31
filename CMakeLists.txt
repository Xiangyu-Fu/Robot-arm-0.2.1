cmake_minimum_required(VERSION 2.8.3)
project(arm1)

find_package(catkin REQUIRED COMPONENTS
        std_msgs
        message_generation
)

add_service_files(
   FILES
   GoToPosition.srv
)

generate_messages(
   DEPENDENCIES
   std_msgs  
)

catkin_package()

find_package(roslaunch)



foreach(dir config launch meshes urdf)
	install(DIRECTORY ${dir}/
		DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/${dir})
endforeach(dir)
