# Ferrite loop/rod antennas

Model with an RLC circuit 
Change what frequency we're tuning for based on C

Perhaps nab ferrite loop antenna from existing panasonic RC-6065 radio 
> Was capable of 520 - 1610 kHz so should be fine 

$$
f_{res} = \frac{1}{2\pi \sqrt{LC}}
$$

> [!info]
> Purpose of $C_{tune}$ is to resonate the frontend such that the resonant frequency is the same as the frequency of the AM radio station one wants to listen to

`L7` on the RC-6065 is a ferrite antenna. Need to measure L and R. Or buy from jaycar (https://www.jaycar.com.au/aerial-ferrite-rod-with-coil/p/LF1020?srsltid=AU7gw4XzW9NVKASd9DTNhwep7kWFuDEbQ25aGhvvEfzBc2rO9BNJ7k33). Need to pair with a trimming capacitor for $C_{tune}$.

## Jaycar ferrite loop

$L = 200\ uH \pm 10\%$

