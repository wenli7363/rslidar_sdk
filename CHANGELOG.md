# CHANGELOG

## v1.5.18 2025-07-15

### Added

- Add a solution for abnormally reduced frame rate under ROS2 humble.
- Support add install mode param for RSAIRY.
- Support user RPY transform for RSAIRY.

### Fixed

- Fix PCAP playback speed issue.

## v1.5.17 2025-02-14

### Added

- Support RSAIRY.
- Support parsing IMU data for RSAIRY and RSE1.
- Support parsing IMU extrinsics parameters frome difop for RSAIRY.

### Changed

- Add feature attribute to point type.
- Updated config file.
- Update help document.
- Update block_time_offset as us for RSE1

### Fixed

- Fix the issue of packets subscription failure under ros2.

## v1.5.16 2024-08-27

### Added

- Load config path frome ros2 param.

### Changed

- Remove the original compilation method.

### Fixed

- Use single package.xml file for both ROS1 and ROS2 @Timple.
- Update msop protocol of RSMX.

## v1.5.15 2024-08-07

### Added

- Support RSM3.

## v1.5.14 2024-07-15

### Added

- Support multiple lidars with different multicast addresses and the same port.

### Fixed

- Fixed the bug that only one lidar was parsed correctly when multiple bp4.0 were used.
- Fix version number in the package.xml by @Timple.

## v1.5.13 2024-05-10

### Added

- Support RSMX.

### Fixed

- Update timestamp parsing unit and the number of packets per frame in decoder_RSE1.
- Update firing_tss of Helios/Helios16P/RubyPlus.
- Fix compilation bug of unit test.
- Remove duplicate text "/rslidar_packets" by @luhuadong.

## v1.5.12 2023-12-28

### Fixed

- Fix bug in getting device info and status.
- Fix bug in getting device temperature.

## v1.5.11 2023-12-18

### Changed

- Enable modify socket buffer size.

## v1.5.10 - 2023-02-17

### Changed

- Merge RSBPV4 into RSBP

## v1.5.9 - 2023-02-17

### Changed

- Increase sending DDS buffer queue to avoid packet loss

## v1.5.8 - 2022-12-09

### Added

- Support ROS2/Humble Hawksbill
- rename RSEOS as RSE1

### Fixed

- Fix wrong widthxheight while ros_send_by_rows=true

## v1.5.7 - 2022-10-09

### Added

- Seperate RSBPV4 from RSBP
- Support to receive MSOP/DIFOP packet from rosbag v1.3.x
- Support option ros_send_by_rows

## v1.5.6 - 2022-09-01

### Added

+ Add a few build options according to rs_driver
+ Update help documents

## v1.5.5 - 2022-08-01

### Changed

- Output intensity in point cloud as float32

### Fixed

- Fix compiling and runtime error on ROS2 Elequent
- Fix frame_id in help docs

## v1.5.4 - 2022-07-01

### Added

- Support the option to stamp the point cloud with the first point

### Changed

- Remove the dependency on the protobuf library

## v1.5.3 - 2022-06-01

### Added

- Support Jumbo Mode

### Fixed

- Fix compiling error when protobuf is unavailable

## v1.5.0

### Changed

- refactory the project

### Added

- support user_layer_bytes and tail_layer_bytes
- support M2
- replace point with point cloud, as rs_driver's template parameter
- handle point cloud in rs_driver's thread

## v1.3.0 - 2020-11-10

### Added

- Add multi-cast support
- Add saved_by_rows argument
- Add different point types( XYZI & XYZIRT)

### Changed

- Update driver core, please refer to CHANGELOG in rs_driver for details
- Update some documents
- Change angle_path argument to hiding parameter

### Removed

- Remove RSAUTO for lidar type
- Remove device_ip argument

## v1.2.1 - 2020-09-04

### Fixed

- Fix bug in driver core, please refer to changelog in rs_driver for details.

## v1.2.0 - 2020-09-01

### Added

- Add camera software trigger (base on target angle)

### Changed

- Update driver core, please refer to changelog in rs_driver for details
- Update the compiler version from C++11 to C++14

## v1.1.0 - 2020-07-01

### Added

- Add ROS2 support

### Changed

- Replace while loop with cv.wait
- Update the vector copy part
- Update the program structure

### Removed

- Remove some unused variables in message struct

## v1.0.0 - 2020-06-01

### Added

- New program structure
- Support ROS & Protobuf-UDP functions
