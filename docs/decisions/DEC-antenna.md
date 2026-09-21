# Decision - Antenna 

ARRL and the other [[refs|resources]] state that a *ferrite-loop* antenna is a suitable arrangement for receiving AM radio to meet the [[requirements]].

There are three primary options for this.

- Buy an antenna
- Build an antenna
- Salvage an antenna

There are difficulties in measuring the inductance of the *RC-6065* ferrite core, so the decision has been made to *buy one* directly from Jaycar, as it has a known inductance. 

>[!Warning]
>The series resistance $R_{coil}$ still needs to be measured with a multimeter


## Modelling 

In order to begin modelling the circuit in `LTSpice`, approximate values of $R_{coil} = 10\ \Omega$ and hence $C_{tune}$ were used. 
