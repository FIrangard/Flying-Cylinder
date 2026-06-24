Flying-Cylinder

This repository contains the simulation environment and control codebase for a custom flying cylinder robot, designed for research and testing of autonomous flight control and sensor fusion algorithms.

The project leverages Blender for high-fidelity 3D modeling and Gazebo Harmonic for physics-based simulation.



🛠 Prerequisites & Installation

To run this simulation, you need to install Gazebo Harmonic and Blender. Follow the instructions below for Ubuntu (recommended).

1. Install Gazebo Harmonic

Gazebo Harmonic is the latest stable release of the Gazebo simulation environment.

# Install necessary tools
sudo apt-get update
sudo apt-get install lsb-release wget gnupg

# Download the Gazebo GPG key
sudo wget https://packages.osrfoundation.org/gazebo.gpg -O /usr/share/keyrings/pkgs-osrf-archive-keyring.gpg

# Add the repository to your sources list
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/pkgs-osrf-archive-keyring.gpg] http://packages.osrfoundation.org/gazebo/ubuntu-stable $(lsb_release -sc) main" | sudo tee /etc/apt/sources.list.d/gazebo-stable.list > /dev/null

# Install Gazebo Harmonic
sudo apt-get update
sudo apt-get install gz-harmonic


For detailed installation instructions, visit the official Gazebo installation guide.

2. Install the Latest Blender

To ensure compatibility with the latest 3D modeling features, it is recommended to install Blender via Snap to get the most recent version.

sudo snap install blender --classic


Alternatively, you can download it directly from blender.org.



⚙️ Environment Configuration

For Gazebo to find your custom models and world files, you must add the repository paths to your environment variables.





Open your .bashrc file:

nano ~/.bashrc




Scroll to the bottom of the file and add the following lines (replace path/to/your/repo with the actual path where you cloned this repository):

# Flying Cylinder Simulation Paths
export GZ_SIM_RESOURCE_PATH=$GZ_SIM_RESOURCE_PATH:~/path/to/your/repo/models:~/path/to/your/repo/worlds




Save and exit (Ctrl+O, Enter, Ctrl+X), then source the file to apply changes:

source ~/.bashrc




🚀 Getting Started

Clone the Repository

git clone https://github.com/FIrangard/Flying-Cylinder.git
cd Flying-Cylinder


Running the Simulation

(Add your specific launch commands here, for example:)

gz sim worlds/your_world_file.sdf




🧪 Project Goals





Sensor Examination: Testing IMU, Lidar, and Camera data in a controlled physics environment.



Control Algorithms: Implementation and analysi PID and advanced control strategies for cylindrical flight dynamics.ics.
