# md_local_planner

Lyapunov function-based velocity planner plugin for differential-drive mobile robot.

## Lyapunov function for point stabilization

<img src="https://render.githubusercontent.com/render/math?math=V=\frac{1}{2}\lambda_1 r^2 %2B \frac{1}{2}\lambda_2 \|R(\alpha)\|_F^2 %2B \frac{1}{2}\lambda_3 \|R(\phi)\|_F^2">
<img src="https://github.com/MLCS-Yonsei/md_local_planner/blob/main/robot.png" width="640">

## Control law

<img src="https://render.githubusercontent.com/render/math?math=v=\gamma_1 r \cos\alpha">
<img src="https://render.githubusercontent.com/render/math?math=\omega=\gamma_1(\sin\alpha\cos\alpha-\frac{\lambda_3}{\lambda_2}\sin\phi\cos\alpha) %2B\gamma_2\sin\alpha">

## ROS parameters
- control_gain1: <img src="https://render.githubusercontent.com/render/math?math=\gamma_1">
- control_gain2: <img src="https://render.githubusercontent.com/render/math?math=\gamma_1\frac{\lambda_3}{\lambda_2}">
- control_gain3: <img src="https://render.githubusercontent.com/render/math?math=\gamma_2">
- look_ahead_distance: The maximum distance between local reference point and robot center, in meters.
