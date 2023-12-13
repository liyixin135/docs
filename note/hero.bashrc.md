export ROS_IP=`ifconfig | grep -Eo 'inet (addr:)?([0-9]*\.){3}[0-9]*' | grep -Eo '([0-9]*\.){3}[0-9]*' | grep -v '127.0.0.1' | grep -v '172.17.0.1' | grep -v '192.168.100.2'`

if  test -z "${ROS_IP}"
then
        export ROS_IP=`dig +short localhost`
fi

export ROS_IP=192.168.100.2

export ROS_MASTER_URI=http://$ROS_IP:11311

export ROBOT_TYPE=hero
export IMU_TRIGGER=false
export HW_NAME=rm_can_hw
export CAMERA_TYPE=hk_camera
export CAMERA_CLASS=HKCameraNodelet

# >>> fishros initialize >>>
 source /opt/ros/noetic/setup.bash
 source /opt/intel/openvino_2021/bin/setupvars.sh
 source ~/rm_ws/devel/setup.bash
# <<< fishros initialize <<<

export MVCAM_SDK_PATH=/opt/MVS

export MVCAM_COMMON_RUNENV=/opt/MVS/lib
export LD_LIBRARY_PATH=/opt/MVS/lib/64:/opt/MVS/lib/32:$LD_LIBRARY_PATH


alias stop="sudo systemctl stop rm_can_start.service start_master.service"
alias stoprm="sudo systemctl stop rm_can_start.service"
alias stopst="sudo systemctl stop start_master.service"
alias startrm="sudo systemctl start rm_start.service"
alias startst="sudo systemctl start start_master.service"
alias statusrm="sudo systemctl status rm_start.service"
alias statusst="sudo systemctl status start_master.service"
alias bringup="mon launch rm_bringup start.launch"
alias manual="mon launch rm_config manual.launch"
alias referee="mon launch rm_config referee.launch"
alias load_controllers="mon launch rm_config load_controllers.launch"
alias hw="mon launch rm_config rm_hw.launch"
alias restart="sudo systemctl restart rm_can_start.service start_master.service vision_start.service"
alias stop='sudo systemctl stop rm_can_start.service start_master.servicision_start.service'
