#### Project creation standard process

- Create `ros2-ws/src` folder
- Create ros2 project using `ros2 pkg create --build-type ament_python hello_ros2` under `ros2-ws/src` folder.
- Outer `hello_ros2` is your package and inner `hello_ros2` is where your python code goes.
- Create [hello_world.py](hello_world.py) in inner `hello_ros2` folder.
- Now we need to register our [hello_world.py](hello_world.py) under `setup.py`
```
    entry_points={
        'console_scripts': [
            'naga = hello_ros2.hello_world:main',
        ],
    }
```

- Then switch back to `ros2-ws`

#### Peform BI-RUN (Build, Install and Run)
- Then build workspace using `colcon build`. This will create package.
- Now install package using `source install/setup.bash`
- Run package using `ros2 run <package_name> <script_name>`
- Eg: `ros2 run hello_world naga`


