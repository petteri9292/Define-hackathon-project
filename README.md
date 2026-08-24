# Define-hackathon-project
This is a repository for the Define hackathon organized 22-24 may 2025. The main object of the repository is to be able to approximate the wind speed and potentially the direction from visual information present in a video. 

The idea was to use a depth model to produce the distances to each pixel, and then using optical flow estimate the movement in the scene. Using these it is possible to get the size of the movement in the 3D scene
and then use this to calculate the speed of the wind.

depth_video shows the output of the depth model and flow_video the optical flow. The graph distance_changed shows a histogram of the absolute length of each movement vector between frames.

Code is omitted from this repository as the project was done locally and the code isn't cleaned enough to be presentable. It was written in a notebook that, due to the erratic nature of hackathons, doesn't have a logical execution order. 

## Limitations

The obvious problem that wasn't addressed was that even accurate scene movement vectors doesn't tell the direction of the wind. Most visual information in images comes from trees and these don't move in the direction of the wind, they bob back and forth. This is why only the magnitude was included. Still, using this approach might make a good prior for a machine learning system.
