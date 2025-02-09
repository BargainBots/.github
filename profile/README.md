# BargainBots

## How to run locally
Follow these steps to test BargainBots simulations locally.

### Negotiation Example
This example demonstrates two robots negotiating about who should go for maintenance first

**Simulation Setup** - 

![negoation](https://rose-melodic-felidae-510.mypinata.cloud/ipfs/bafybeidpbvfnt7yfvieeqdacf34syjyr2kfxqluw5jvehlhtlgtr6aqsqe)

1. Setup Gazebo Harmonic and ROS2 Rolling on your machine.
    [https://gazebosim.org/docs/harmonic/ros_installation/](https://gazebosim.org/docs/harmonic/ros_installation/)

2. ```
    git clone https://github.com/BargainBots/simulation.git
    cd simulation/src
    rosdep install -r --from-paths . --ignore-src --rosdistro $ROS_DISTRO -y
    cd ..
    colcon build
    ```
3. ```
    source install/setup.bash
    ros2 launch bargain_bots_demos diff_drive_example.launch.py
    ```
---
-**ZerePy Setup** -

![zerepy](https://rose-melodic-felidae-510.mypinata.cloud/ipfs/bafkreic2a4fargpzm244dpm3mix73vv445k4jrsoocvgt6w7aepionqjna)

1. ```
    git clone https://github.com/BargainBots/ZerePy.git
    ```
2. Configure ```ETH_PRIVATE_KEY``` and ```HYPERBOLIC_API_KEY``` in .env
3. Follow [ZerePy Docs](https://www.zerepy.org/docs/server-mode) to run the application
4. ```poetry run python bargain_bots.py```

\
After this, play the simulation and move the robot using Arrow Keys and see the example running upon any collision

---

### Governance Example
This example demonstrates 4 robots taking a decision about who should be their leader.

**Simulation Setup** -

![governance](https://rose-melodic-felidae-510.mypinata.cloud/ipfs/bafkreicojy7ps2pkdkb7234qotmcnkjtvkcprfkj76ltw5ekzzony4uibe)

1. Setup Gazebo Harmonic and ROS2 Rolling on your machine.
    [https://gazebosim.org/docs/harmonic/ros_installation/](https://gazebosim.org/docs/harmonic/ros_installation/)

2. ```
    git clone https://github.com/BargainBots/simulation.git
    cd simulation
    gz sim conference.sdf
    ```
---

**ZerePy** -

![gove](https://rose-melodic-felidae-510.mypinata.cloud/ipfs/bafybeid7yjkgrvqd5hmekdpwic3qlobop3wvcdelxcis5avvkzcod2pdtm)

![gove](https://rose-melodic-felidae-510.mypinata.cloud/ipfs/bafybeiafwntalh2r2trrnooi4n3y7a4o7rsrdckcc7ubekapgtucmfpts4)


1. Setup as specified previously
2. ```poetry run python robot_governance.py```

\
After this, take the robot to the black area and see the example running.
