cmake_minimum_required(VERSION 2.8)
project(std_msgs)

find_package(catkin)
find_package(genmsg)

add_message_files(
  DIRECTORY msg
  FILES Bool.msg Float32MultiArray.msg Int64MultiArray.msg
  UInt32.msg Byte.msg Float64.msg Int8.msg
  UInt32MultiArray.msg ByteMultiArray.msg
  Float64MultiArray.msg Int8MultiArray.msg UInt64.msg
  Char.msg Header.msg MultiArrayDimension.msg
  UInt64MultiArray.msg Int16.msg MultiArrayLayout.msg
  UInt8.msg ColorRGBA.msg Int16MultiArray.msg
  String.msg UInt8MultiArray.msg Duration.msg
  Int32.msg Time.msg Empty.msg Int32MultiArray.msg
  UInt16.msg Float32.msg Int64.msg
  UInt16MultiArray.msg)

generate_messages()

install_cmake_infrastructure(std_msgs
  VERSION 0.0.1
  MSG_DIRS msg
  )

catkin_package(std_msgs)
enable_python(std_msgs)
