#### Contents

- [Installations](./Installations.md)
- [Project-creation](./ros-project-creation.md)
- [Auto-reload](./auto-reload.md)

#### Project structure 

```
ros2_ws/                              (WORKSPACE)
│
└── src/
    │
    ├── robot_control/                (PACKAGE)
    │   ├── package.xml
    │   ├── setup.py
    │   │
    │   └── robot_control/
    │       ├── __init__.py
    │       ├── controller.py         (NODE)
    │       └── safety.py             (NODE)
    │
    └── robot_sensors/                (PACKAGE)
        ├── package.xml
        ├── setup.py
        │
        └── robot_sensors/
            ├── __init__.py
            ├── camera.py             (NODE)
            └── lidar.py              (NODE)

```