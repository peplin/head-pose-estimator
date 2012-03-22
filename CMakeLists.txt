cmake_minimum_required(VERSION 2.6)

SET( 	HEAD_DEMO
		CRForestEstimator.cpp
		CRTree.cpp
		main.cpp 
)

SET(CMAKE_BUILD_TYPE "Release")

#modify according to your opencv installation
SET( OPENCV_INCLUDES /include ) 
SET( OPENCV_LIB /lib ) 

INCLUDE_DIRECTORIES( . ${OPENCV_INCLUDES} )
LINK_DIRECTORIES( ${OPENCV_LIB} )

add_executable( head_pose_estimation ${HEAD_DEMO})

target_link_libraries (head_pose_estimation opencv_core opencv_highgui opencv_imgproc )




