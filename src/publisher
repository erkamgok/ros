#include "ros/ros.h"
#include "std_msgs/String.h"

int main(int argc, char **argv) 
{
    ros::init(argc, argv, "publisher_node");
    ros::NodeHandle n;
    ros::Publisher chatter_pub = n.advertise<std_msgs::String>("chatter", 10);
    ros::Rate loop_rate(1);  // 1 Hz

    while (ros::ok()) 
    {
        std_msgs::String msg;
        msg.data = "Hello, ROS!";
        ROS_INFO("%s", msg.data.c_str());
        chatter_pub.publish(msg);
        ros::spinOnce();
        loop_rate.sleep();
    }

    return 0;
}