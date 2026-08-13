#### Auto-reload

- Every time you make a code change you need to run following
```
colcon build
source install/setup.bash
ros2 run <package_name> <script_name>
```

- Instead you can follow symlink. Do the following once
```
colcon build --symlink-install
source install/setup.bash
ros2 run <package_name> <script_name>
```

- Now evertime you make a code change, all you need to run is 

```
ros2 run <package_name> <script_name>
```