# ps7_kvc2

Modified version of cwru_pcl_utils; ps7_kvc2.cpp is derived from cwru_pcl_utils_color_test.cpp. Takes a selection of points in RViz and publishes coplanar points to within a set tolerance. 

## Example usage
In separate terminals, run:
-roslaunch cwru_baxter_sim baxter_world.launch
-roslaunch cwru_baxter_sim kinect_xform.launch
-rosrun ps7_kvc2 ps7_kvc2
-rosrun rviz rviz

In the left sidebar in RViz, ensure that kinect_depth_points is displaying as a PointCloud2 type. Change the Color Transform to AxisColor to see the relative Z values of the published points. Select Add>Topic>/pcl_cloud_display. On the top bar, click "Select", click and drag to select points in the RViz view, then click "Publish Selected Points" to publish the selection. 

Optionally, open a new terminal and enter "rostopic echo /pcl_cloud_display" to see the generated points. 
