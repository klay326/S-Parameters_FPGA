RF Signal Generator for Use in S-Parameter Collection Device

The design centers around the MAX2871 which is a 23.5MHz to 6GHz Fractional/Integer-N Synthesizer with VCO and PLL. This goes into a Mini Circuits DC to 1.5GHz Low Pass filter IC to reduce harmonics and improve performance across the designed S-Parameter sampling requirements of 100kHz to 1.5 GHz. The filtered output goes into a PE43711 Variable Attenuator to adjust signal attenuation with minimal distortion. It then goes into a TRF37A75 gain block to selectively add signal gain. Finally, an AD8319 power detector is used to formulate a feedback loop to adjust the desired signal output power. The combination of these devices forms the basis for an SPI controlled signal generator that can be used to provide a signal stimulus for taking S-Parameter measurements.

- PCB Assembly
- Voltage Probing and Component Testing
- Continuity Check

- Failed to Establish SPI Communication with ICs
- Issue with uC 3.3V Source

- Able to see default signal on spectrum analyzer.
- Tested RF passthrough even with attenuator, and gain block turned off to output signal.