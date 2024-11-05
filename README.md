# Overview
The project aims to create a biceps curl counter that uses human pose estimation to detect the full range of motion and provides real-time feedback. The counter is designed to track bicep curls only when the movement spans the complete range of motion, i.e., from 30 to 160 degrees, ensuring proper technique. This helps users, particularly beginners, avoid poor form that could lead to ineffective workouts or even muscle strain or injury over time. By receiving immediate feedback, users can adjust their posture without needing a workout partner, supporting a safer and more effective training experience.

## Description
This project leverages Mediapipe's Blazepose model for pose estimation, which powers the backend by calculating the 3D coordinates of key body points. We extract three keypoints—the wrist, elbow, and shoulder form two lines: one connecting the shoulder and elbow (line A) and another connecting the elbow and wrist (line B). By calculating the angle between lines A and B, we determine the elbow’s angle, which serves as the basis for counting repetitions. A binary variable, 'stage,' tracks the hand position during each curl, indicating whether it’s in the UP or DOWN position. Each successful transition from DOWN to UP increases the counter by 1. Counters are maintained separately for both the right and left arms.


<img width="350" alt="Demo" src="https://github.com/user-attachments/assets/acdc59ab-3f74-45e5-b7a9-3a2fc30da7c6">

## Future Improvements:
### Customizable Range of Motion
Allow users to set their own range of motion, rather than keeping it fixed at 30 to 160 degrees. This flexibility would enable users to adjust the counter for various types of curls or personal preferences, making the tool adaptable for different training needs and levels.
