# Resolve conflict between python3.x openCV and Ros python2.x (Temporary fix)

I couldn't find the permenent fix for this issue. However, add the following line at the beginning of your python code which will work for the current project.

```>> import sys ```

```>> print(sys.path)```

Depending on which ROS package are you using, you will see one of the ROS path like below.

*'/opt/ros/kinetic/lib/python2.7/dist-packages'*

Copy that path and remove it from the system path.

```>> sys.path.remove('/opt/ros/kinetic/lib/python2.7/dist-packages')```

You are done and now be able to use CV.
