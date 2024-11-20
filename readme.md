# ros作业

自学rosbag，之后播放这个bag文件，实现：

1. cpp和python的话题订阅和发送

2. 分析这个bag内部的数据的属性，如：话题，话题数据含义等，写到readme.md


path:        jiantu2.bag
version:     2.0
duration:    1:43s (103s)
start:       Sep 21 2024 06:52:48.60 (1726872768.60)
end:         Sep 21 2024 06:54:32.41 (1726872872.41)
size:        36.9 MB
messages:    91348
compression: none [48/48 chunks]
types:       nav_msgs/Odometry         [cd5e73d190d741a2f92e81eda573aca7]
             sensor_msgs/Imu           [6a62c6daae103f4ff57a132d6f95cec2]
             sensor_msgs/LaserScan     [90c7ef2dc6895d81024acba2ac42f369]
             sensor_msgs/MagneticField [2f3b0b43eed0c9501de0fa3ff89a45aa]
topics:      /driver/encoder    4758 msgs    : nav_msgs/Odometry        
             /driver/eul       28635 msgs    : sensor_msgs/Imu          
             /driver/imu       28469 msgs    : sensor_msgs/Imu          
             /driver/mag       28469 msgs    : sensor_msgs/MagneticField
             /driver/scan       1017 msgs    : sensor_msgs/LaserScan
             

    path： rosbag 文件的路径。
    version：版本号 2.0。
    duration：给出了 rosbag 记录数据的持续时间，这里是 1:43。
    start：记录了 rosbag 开始记录数据的时间，括号里的 1726872768.60 是对应的时间戳，从某个特定起始时间开始计算到此刻所经过的秒数。
    end：结束记录数据的时间。

    size：文件的大小，这里是 36.9 MB。
    messages：消息总数，这里是 91348 条消息。

    compression：该文件没有进行压缩处理。不压缩数据也会分成 48 块。

    types：
        nav_msgs/Odometry：其唯一标识符为 [cd5e73d190d741a2f92e81eda573aca7]。nav_msgs/Odometry 类型的消息通常用于表示机器人的里程计信息，比如机器人的位置、姿态以及速度等。
        sensor_msgs/Imu：标识符是 [6a62c6daae103f4ff57a132d6f95cec2]。sensor_msgs/Imu 传递惯性测量单元（IMU）的数据，包括加速度、角速度等。
        sensor_msgs/LaserScan：对应的标识符为 [90c7ef2dc6895d81024acba2ac42f369]。sensor_msgs/LaserScan 激光雷达等测距设备发出的，它包含了关于周围环境的激光扫描数据，比如扫描角度范围、每个角度对应的距离值等。
        sensor_msgs/MagneticField：其标识符为 [2f3b0b43eed0c9501de0fa3ff89a45aa]。sensor_msgs/MagneticField 传递磁场相关的数据，进行磁场相关分析。

    topics：
        /driver/encoder：这个话题发布了 4758 条消息，消息类型是 nav_msgs/Odometry。用于提供与机器人运动里程计相关的某些特定数据，来自编码器的里程计信息。
        /driver/eul：发布了 28635 条消息，消息类型为 sensor_msgs/Imu。传递与惯性测量单元相关的数据，但可能是侧重于某种特定角度：欧拉角。
        /driver/imu：同样发布了 28469 条消息，sensor_msgs/Imu 类型。传递 IMU 相关的数据。
        /driver/mag：发布了 28469 条消息，消息类型为 sensor_msgs/MagneticField。用于传递磁场相关的数据，可能是来自磁场传感器。
        /driver/scan：发布了 1017 条消息，消息类型是 sensor_msgs/LaserScan。用于传递激光雷达等测距设备扫描得到的环境数据。

