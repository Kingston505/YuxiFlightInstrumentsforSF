# Yuxi-Flight-Instruments-for-SF

## Introduction

A set of flight instruments designed for VRChat flight maps based on [SaccFlight](https://github.com/Sacchan-VRC/SaccFlightAndVehicles).
Currently, the main completed instruments include the airspeed indicator, attitude indicator, altimeter, turn coordinator, heading indicator, and vertical speed indicator (the "Big Six").

![A sample diagram](https://github.com/Heriyadi235/YuxiFlightInstrumentsforSF/blob/main/documents/pic1.png)

The image above is just a sample instrument model, and it’s a bit rough (I’m not very good at modeling, lol). But I kept reusability in mind when writing the scripts, so it should be easy to replace the models—just set up the animations, no additional code needed.

## Detailed Description

So one day, I suddenly felt like making an aircraft model for SF. I looked through the SaccFlight code and then realized that UdonSharp isn’t that hard. After spending two or three days brushing up on development knowledge, I managed to put this thing together.
Overall, making the instruments work requires two scripts and one animator controller. The process looks roughly like this:

* Script
  [YFI\_FlightDataInterface.cs](https://github.com/Heriyadi235/YuxiFlightInstrumentsforSF/blob/main/Scripts/YFI_FlightDataInterface.cs)
  Used to read or calculate most of the flight data from the SAVController.

* Script
  [YFI\_AnimatorController.cs](https://github.com/Heriyadi235/YuxiFlightInstrumentsforSF/blob/main/Scripts/YFI_AnimatorController.cs)
  Used to convert flight data into 0\~1 parameters to drive the animator controller associated with the instruments. Instrument ranges and other parameters can be set here.


