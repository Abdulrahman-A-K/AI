# AI
# first task  
* **OverVeiw**
    * This guide will walk you through the steps to install ROS Noetic on Ubuntu 20.04 (Focal Fossa).



* **Installtion Steps**
    * Install Ubuntu 20.04
Ensure that you have Ubuntu 20.04 (Focal Fossa) installed on your system. ROS Noetic is designed to work with this specific version of Ubuntu.
    
    * second Set Up the ROS Package Sources
Open a terminal and add the ROS package repository to your system:
        ```bash
            sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
        ```  
    
    * third Add the ROS GPG Key
To authenticate the packages, add the ROS GPG key:
        ```bash
            sudo apt install curl # if you haven't already installed curl
            curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
        ```  
        if downloaded successfully it you will see this output  
        ![photo](./image1.png)

    * forth update the debian packages and i recommended to download the fully version of ros-noetic
        ```bash
            sudo apt update
            sudo apt install ros-noetic-desktop-full
        ```
        **Be carful it will take long time to install because it depends on your WiFi connection speed**  
        after it installed your working directory and run this command
        ```bash
            cd /opt/ros/noetic
            source /opt/ros/noetic/setup.bash
            roscore
        ```
        this output look like this  
        ![photo](./image2.png)

    * finally is setup enviroment because if you want use ros will need run this script every time you lunch new terminal
    ```bash
        source /opt/ros/noetic/setup.bash
    ```
    so you need embeded this script in your bash and you can run roscore command from any new terminal you opened  
