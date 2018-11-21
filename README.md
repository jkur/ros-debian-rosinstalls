# ROS on Debian (sid as of 11/2018)

The (native) Debian packages for ROS are not fully complete. To install the full stacks some compilation from source is necessary.
These .rosinstall files can be used to create a workspace for ROS development on Debian with native packages only.


In your catkin workspace do:

`wstool init -j8 src {YOURSTACK}.rosinstall`

`wstool up -t src`

`catkin_make_isolated`


## Stacks so far
  * desktop-full
  * industrial-core
  
## Why .patch files?
I wanted to stay close to the rosinstall files that the rosinstall_generator would create. Most of the repositories are coming from upstream.
I could create forks, but these need to be maintained. A patch is easier and more transparent.

Debian unstable is moving fast, it's likely that most of the patches are not need in future version.


## Contribute
It would be helpful to see if these files would work on other installation than my own.
If you work with ROS and the Debian-based packages only, please provide your rosinstall files and eventually useful patches.
