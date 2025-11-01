joy_teleop
==========

A configurable node to map joystick controls to robot teleoperation commands
within Modified `JoyTeleopTopicCommand` class to support toggle functionality

# ⚠️ WARNING / 경고

**이 브랜치의 joy_teleop 패키지는 [The 4th F1Tenth Korea Championship](http://dsplay.kr:5050/)의 규정을 준수하기 위해 개인적으로 수정한 패키지입니다.**

**USE AT YOUR OWN RISK. 본인 책임 하에 사용하십시오.**


This is a MODIFIED version of the original joy_teleop package with toggle functionality for F1Tenth racing.

This modified code has NOT been extensively tested in all scenarios.

May cause unexpected vehicle behavior.

The original authors and modifier assume NO responsibility for any damages, injuries, or losses

**NO WARRANTY PROVIDED. Use this software entirely at your own risk.**


## How to install 
1. Remove original `teleop_tools/` in `~/your_ws/src/f1tenth_system`
2. Clone this repo: 
    ```bash 
    git clone https://github.com/zygn/teleop_tools.git -b iccas-toggle
    ```
3. Add `toggle: True` to your `~/your_ws/src/f1tenth_system/f1tenth_stack/config/joy_teleop.yaml` config file:
   ```yaml
    # for example
    autonomous_control:
      type: topic
      interface_type: std_msgs/msg/Int8
      topic_name: /dev/null
      deadman_buttons: [5]
      toggle: True  # Add this line
      message_value:
        data:
          value: 0
    ```
4. save and build your workspace 

