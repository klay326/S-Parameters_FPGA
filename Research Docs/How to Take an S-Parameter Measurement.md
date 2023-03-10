
- The Main Parts of an VNA Measurement:
  - Test Signal Generation: needs to create a test signal to be sent through the network under test usually a sinusoidal sweep acress a frequency range
  - Signal Sampling: Taking multiple samples of the the signal that passes throught the DUT. Theses are taken at different frequencies and power levels
  - Signal Processing: Takes the signal samples to create a frequency response of the network
  - Parameter Calculation: Uses the frequency response to calculate other parameters such as return loss, insertion loss, phase delay, etc.
- Measurement Process
  - To measure S11 or S21, the switch would route the signal toward Port 1. The signal first enters a directional device, shown as Directional Device R1 in Figure. This directional device could be a directional coupler or bridge. A power divider could also be used here. The purpose of this device is to direct a portion of the input signal to a reference receiver, shown as Reference Receiver 1. Once the signal enters this reference receiver, it’s downconverted and ultimately processed.
  - The signal that passes through Directional Device R1 then passes through another directional device, shown as Directional Device M1 in Figure, before arriving at the DUT. When the signal does arrive at the DUT, a portion is reflected back to Port 1 of the VNA and reenters Directional Device M1. This device now directs a portion of the reflected signal to a measurement receiver, shown as Measurement Receiver 1. Next, this signal is downconverted and processed. The VNA can then compare the data obtained from Measurement Receiver 1 with the data obtained from Reference Receiver 1. This process summarizes how S11 is measured.
  - The signal applied to the DUT also results in a transmitted signal, which exits the DUT and enters Port 2 of the VNA. This transmitted signal enters another directional device, shown as Directional Device M2 in Figure. This device directs a portion of the signal to another measurement receiver, shown as Measurement Receiver 2. This signal is subsequently downconverted and processed. Now, the VNA can compare the data obtained from Measurement Receiver 2 with the data obtained from Reference Receiver 1. This process summarizes how S21 is measured.
  - To measure S22 or S12, the switch would route the signal to Port 2. The same process occurs in the opposite direction: The signal first enters Directional Device R2 in Figure, which directs a portion of the signal to Reference Receiver 2. After entering this reference receiver, the signal is downconverted and processed.

![Aspose Words e15d70e9-a19f-41a6-b9db-4fcfb09769ad 003](https://user-images.githubusercontent.com/29070021/213368360-d90dd215-2da8-4940-bab2-541e947505cd.png)

- Electrical Components Needed:
  - Clock Source:
    - Source clock for required reference clocks of ics and things
  - Signal Generator: 
    - A signal generator is used to create a test signal that is sent through the network. The signal generator typically generates signals at different frequencies and power levels.
    - PLL most likely
  - Power Supply:
    - Integrated or USB, could possibly need many independent regulators to prevent
  - Power Amplifier:
    - A power amplifier is used to amplify the test signal before it is sent through the network. This is necessary because the signal may be too weak to be effectively measured by the network analyzer's receiver.
  - Mixer:
    - A mixer is used to convert the test signal to a different frequency range for processing.
  - Filter:
    - A filter is used to remove unwanted signals from the test signal. This is necessary to ensure that the measurement is accurate.
  - Attenuator:
    - Can digitally adjust the signal power
  - Directional Device
    - See Below 
  - Detector:
    - A detector is used to measure the amplitude of the signal and to extract the information needed to create a frequency response.
  - ADC:
    - An ADC is used to digitize the analog signal for further processing by a computer.
  - FPGA and Microcontroller:
    - State control and computer interfacing
- Directional Coupler vs Return-Loss Bridges
  - A directional coupler and a resistive return-loss-bridge are both types of devices that can be used to measure the performance of a network in a specific direction. However, they operate differently and are used for different purposes. A directional coupler is a passive device that is used to sample a portion of the signal that is passing through a network. It is a four-port device that allows the measurement of the forward and reflected power of a signal. It can be used to measure the return loss of a device, which is a measure of how much power is reflected back to the source. It also can be used to measure the insertion loss of a device, which is a measure of how much power is lost as it passes through the device. A resistive return-loss-bridge is a device that is used to measure the return loss of a device. It is a two-port device that is used to measure the amount of power that is reflected back to the source. It is typically used to measure the return loss of a device that is not directional, such as a resistor. In summary, a directional coupler is a four-port device that allows the measurement of the forward and reflected power of a signal, and it can be used to measure the return loss and insertion loss of a device. A resistive return-loss-bridge is a two-port device that is used to measure the return loss of a device, typically for a non-directional device like resistors.

