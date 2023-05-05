# FAQ

This section sorts out the solutions to various chassis common problems. If you can’t solve it according to this document, please contact the relevant technical personnel.。

- Q: The chassis cannot be driven, and the remote control has no alarm

> A: Step 1: Check if the power battery is sufficient. Step 2: Check if all emergency stop switches pop up.Step 3: Check if the handbrake is off. Step 4: Check if it is in remote control mode.Step 5: Check if the brakes are on The return position is normal, check whether the vehicle can be pushed.Step 6: Check whether the high-voltage power supply of the motor controller is normal. Step 7: Check whether the wake-up power relay of the motor controller in the fuse box is normal.

- Q: Chassis cannot be powered on

> A: Step 1: Check if all emergency stop switches pop out. Step 2: Check whether the 12V battery is out of power. Step 3: Check whether the fuses of each fuse box are normal. Step 4: Check whether the low-voltage fuse box is powered. Step 5: Check whether the VCU power supply is normal. Step 6: Check whether there is a short circuit or open circuit on the CAN bus.

- Q: The remote control shows SOC=0%**

> A: 
Step 1: Check if the remote controller has other alarms. If so, refer to Appendix 1 "Remote Controller Fault Code Analysis and Suggestions for Handling". Step 2: Check the power of the chassis power battery and charge the chassis. Step 3: Check whether the 12V battery is short of electricity, which will cause the power battery to fail to output, and it is recommended to recharge the battery. Step 4: Check whether the fuses of each fuse box are normal, whether there is a short circuit or an open circuit in the line. Step 5: Read the chassis CAN message, check whether the 782 message can be read, and contact technical assistance.

- Q: The chassis cannot be charged

> A: 
Step 1: Confirm the charging sequence, plug in the charging cable first, and then plug in the AC plug(The voltage standard in China is 220V) . Step 2: Check whether the main switch (knob switch, if any) is turned on, and it cannot be charged when the main switch is turned off. Step 3: Check the status of the indicator light of the charger to confirm the charging status (The red light flashes slowly to indicate charging, and the green light is always on to indicate that the charging is complete). Step 4: Check the charging circuit, whether there is a short circuit or open circuit; Step 5: Read the chassis message, check whether the 782 message can be read, and contact technical assistance to deal with it.

- Q: Chassis steering fails

> A: Step 1: Check whether the remote controller has an alarm, and deal with it according to the corresponding fault code. Step 2: Check whether the handbrake and brake are normal, and confirm that the low-voltage power supply is normal. Step 3: Check whether the 12V battery is out of power. Step 4: Check In the fuse box, confirm whether the fuse is blown. Step 5: Check the steering motor relay to confirm whether it is burnt out, which can be cross-validated.

- Q: Chassis brake failure

> A: Step 1: Check whether the remote controller has an alarm, and deal with it according to the corresponding fault code. Step 2: Check whether the handbrake and steering are normal, and confirm that the low-voltage power supply is normal. Step 3: Check whether the 12V battery is under charge. Step 4: Check the fuse box to see if any fuse is blown. Step 5: Check the brake relay to confirm whether it is burnt out, which can be cross-validated.

- Q: Chassis handbrake failure

> A: 
Step 1: Check whether the remote control has an alarm, and deal with it according to the corresponding fault code. Step 2: Check whether the braking and steering are normal, and confirm that the low-voltage power supply is normal. Step 3: Check whether the 12V battery is under charge. Step 4: Check the fuse box to see if any fuse is blown. Step 5: Check the handbrake relay to confirm whether it is burnt out, which can be cross-validated.

- Q: CAN port communication is abnormal

> A: Step 1: Check whether the remote control has an alarm, confirm that other functions of the chassis are normal, and the VCU is working normally. Step 2: Use a multimeter to measure the CAN port 2 and 7 respectively, and connect the negative pole to the chassis shell. Under normal circumstances, The voltage of port 2 is low, about 2.25V, and the voltage of port 7 is high, about 2.75V. If the voltage is normal, please check the CAN port connector at the other end connected by yourself. Step 3: If the voltage is abnormal, check the line along the CAN line to confirm whether there is a short circuit or an open circuit.

- Q: Remote control startup exception handling

> A: 
After the vehicle is powered on successfully, the lower part of the display screen of the remote control car will display “Ready”. Otherwise, the power on fails. After the chassis enters “Ready”, observe whether there is a triangle exclamation mark above “Ready”. If not, the driver can perform a driving operation. If it shows that there is a fault in the vehicle, you need to press the Display Switch button to switch the display as the second interface to check the specific system fault. Further investigation of detailed faults requires reading detailed fault codes from the CAN network connected to the phase system through the OBD interface, and the vehicle can be driven as a whole after troubleshooting.

## Remote Controller Fault Code Analysis and Suggestions for Handling is below

| No. | Error code          | Fault code in English  | Meaning of error code  | Handling suggestion  |
| ---- | --- | -------- | ----- | ----- |
| 1    | Chassis normal | System is normal  | Normal status | Normal status |
| 2    | Unable to run  | Can not operate  | Can not operate | 1.Check the remaining power of the power battery, if it is less than 20%, please charge it before use. 2.Check the high-voltage and low-voltage fuse boxes to confirm whether any fuse is blown. 3.Check that the handbrake or brakes are in place. 4.Collect and analyze the messages. |
| 3    | F-steer failure        | Front steering system fault | Steering system motor or controller fault | 1.Check the fuse box to see if there is a blown fuse. 2.Check steering motor relay. 3. Collect and analyze the messages |
| 4    | B-steer failure  | Back steering system fault |   |  |
| 5    | FL-Motor failure       | Front Left wheel failure  | The motor driver has no high-voltage input, or the communication of the signal line fails. | 1. Check the remaining power of the power battery, if it is less than 20%, please charge it before use. 2.Check the high-voltage and low-voltage fuses, and the motor wake-up relay. 3.Check the corresponding wheel motor controller, whether the high voltage input is normal, and whether the signal input is normal. 4.Collect and analyze the messages |
| 6    | RL-Motor failure | Rear Left wheel failure |   |   |
| 7    | FR-Motor failure | Front Right wheel failure |  |   |
| 8    | RR-Motor failure | Rear Right wheel failure |   |   |
| 9    | Brake failure  | Brake system failure  | Brake system brake pump or controller failure | 1.Operate the brakes by remote control, check whether there is a brake sound. 2.Check whether the brake oil pot is sufficient. 3.Check whether the oil pipes at each caliper position of the brake are leaking oil. 4.Release the handbrake, put in neutral, and use a trolley to confirm whether the chassis can move. 5.Collect and analyze the messages |
| 10   | ModeSwitch failure | Mode switch failure | Switching steering modes or shifting gears while the chassis is moving | 1.Switching steering modes or shifting gears while the chassis is moving. 2.Collect and analyze the messages |
| 11   | GearSwitch failure | Gear switch failure |  |  |
| 12   | Lost connection | Abnormal wireless communication | The communication between the remote control and the receiver is abnormal. | 1.The chassis is not powered on, or the receiver is not receiving power. Turn on the chassis, or check whether the power supply of the receiver is normal. 2.The distance between the remote control and the receiver is too long and greater than 100mm. Check whether the antenna of the receiver is normal, or operate it at close range. 3.There is signal shielding or interference between the remote control and the receiver, change the location to test. |
| 13   | Low battery | The battery of Remote control is low | The battery of Remote control is low | Replacing the dry battery of the remote control |
| 14   | Loss of VCU siagnal | Receiver CAN signal lost | Receiver CAN signal lost | Check the CAN network of receiver |
| 15   | Pus rod back to center | Push rod failureReturn the push rod to the neutral position and restart | Damaged push rod. The push rod is not in the neutral position, and the self-test fails | Make sure the push rod is back to the neutral position(center), restart the remote control, and the push rod is prohibited during the self-test process of the remote control. If the failure is still displayed after repeated attempts, please contact Pix Moving for support |
| 16   | ESTOP! | Emergency stop button activated | Emergency stop button is pressed | The emergency stop button is activated. To control the chassis, please exit the emergency stop state |
| 17   | E1 | Abnormal wireless communication  | The communication between the remote control and the receiver is abnormal. | 1.The chassis is not powered on, or the receiver is not receiving power. Turn on the chassis, or check whether the power supply of the receiver is normal. 2.The distance between the remote control and the receiver is too long and greater than 100mm. Check whether the antenna of the receiver is normal, or operate it at close range. 3.There is signal shielding or interference between the remote control and the receiver, change the location to test. |
| 18   | E2 | The battery of Remote control is low | The battery of Remote control is low | Replacing the dry battery of the remote control |
| 19   | E3 | Receiver CAN disconnected | The communication between the receiver and VCU is abnormal. | 1.The 12V battery of the chassis is out of power and the VCU is not activated. Measure the voltage of the 12V battery of the chassis. 2.The chassis power battery is  out of power , the VCU is not working.Please charge the chassis power battery. 3.The CAN line of the receiver is not in good contact or the line is abnormal. Check the receiver cable, re-plug and test, and check the line from the receiver to the VCU. |
| 20   | E4 | Remote control push rod failure | Remote control push rod failure. The self-test fails | 1.During the power-on self-test of the remote control, the push rod is pushed, resulting in the failure of the self-test. Restart the remote control. 2.The push rod of the remote control itself is faulty, please contact the PIX Moving for technical solution. |
| 21   | E5 | Abnormal wireless communication |  |  |
| 22   | E6 | Backup |  |  |