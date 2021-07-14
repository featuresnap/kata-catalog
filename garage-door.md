# Garage Door Opener

You are to simulate the control system for a residential garage door opener.

## System Concepts
### Garage Door: 
The Garage Door can be represented by its position and movement. 
- Position can be OPEN, CLOSED, or PARTIAL (somewhere between OPEN and CLOSED). 
- Movement can be UPWARD (toward the OPEN position), DOWNWARD (toward the CLOSED position), or STATIONARY (not moving).
### Limit Switches:
Limit Switches protect the door and control system by preventing the door from traveling past safe position limits.
- Upper Limit Switch stops the door at the OPEN position when moving UPWARD.
- Lower Limit Switch stops the door at the CLOSED position when moving DOWNWARD.
### Safety Beam:
Safety Beam is a photo-sensor that prevents the door from closing on objects or people that are in the door's path. 
- During DOWNWARD motion, a blockage of the Safety Beam will immediately reverse the door's motion to UPWARD.
- Safety Beam must be unblocked in order to initiate any DOWNWARD motion. 
### Remote Control:
Remote Control is a single-button device that controls all door motion. 
- When door is fully CLOSED, pushing button will initiate opening.
- When door is fully OPEN, pushing button will initiate closing. 
- During opening or closing, pushing button will stop the operation in progress (STATIONARY movement), and the door will remain at its current PARTIAL position.
- If an opening or closing operation is interrupted by a button push, the next button push will resume operation in the _opposite_ direction:
    - UPWARD --> button --> STATIONARY --> button --> DOWNWARD
    - DOWNWARD --> button --> STATIONARY --> button --> UPWARD
