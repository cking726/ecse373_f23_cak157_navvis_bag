# Navvis Bag Instructions

## Launch Argument Options

To launch the file with mostly the same settings as the previous lab, simply use

>roslaunch navvis_bag bag.launch

If you have a different bag file to run use this can be included in the arguments as such:

>roslaunch navvis_bag bag.launch file:=<bag_file_name>.bag

You can also display the navvis with the recording of the glennan 5th floor through the sensors. This can be done with the laser output, or the laser and map overlay together. To see the laser data from the bag file use the following launch:

>roslaunch navvis_bag bag.launch rviz_config_file:=laser_config.rviz

To see the laser data overlayed on the map use this launch instead:

>roslaunch navvis_bag bag.launch rviz_config_file:=map_config.rviz

## Important Directory Setup Information

In order for this package to work the maps_glennan, map_server, and navvis_description packages must be installed within the same workspace. Additionally the bag file that is to be played back needs to be placed within the `navvis_bag/bag_files directory/<bag_file_name>.bag`. The default file it looks for is `navvis_bag/bag_files/glennan_5_basic_short.bag`, but as long as a bag file is placed within this directory you can pass it in through the arguments shown above to run different files.



