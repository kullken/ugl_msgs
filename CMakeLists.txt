cmake_minimum_required(VERSION 3.10.2)
project(ugl_msgs)

find_package(catkin REQUIRED
  COMPONENTS
    message_generation
    std_msgs
    geometry_msgs
)
################################################
## Declare ROS messages, services and actions ##
################################################

# Generate messages in the 'msg' folder
add_message_files(
  FILES
    Bezier.msg
    BezierStamped.msg
    BezierSequence.msg
    BezierSequenceStamped.msg
    SlerpSegment.msg
    SlerpSegmentStamped.msg
    SlerpSequence.msg
    SlerpSequenceStamped.msg
    Trajectory.msg
)

## Generate services in the 'srv' folder
# add_service_files(
#   FILES
# )

## Generate actions in the 'action' folder
# add_action_files(
#   FILES
# )

generate_messages(
  DEPENDENCIES
    geometry_msgs
    std_msgs
)

catkin_package(
  CATKIN_DEPENDS 
    message_runtime
    geometry_msgs
    std_msgs
)
