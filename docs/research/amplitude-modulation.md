# Amplitude modulation (AM)

Info impressed onto a carrier wave $c(t) = C\sin(2\pi f_ct)$
> Single frequency carrier, i.e 693 kHz

Information is encoded on $m(t) = M\cos(2\pi f_m t)$

>[!info]
>`M` is dimensionless. I.e choose M = 0.5 for 50% modulation. 50% modulation means the **carrier amplitude is being varied by ±50%** around its normal value

Perform modulation by multiplying these two together. 
For a single tone modulating signal, $am(t) = c(t) * (1 + m(t))$
> the 1 represents a DC component to allow the envelope to both increase and decrease (see 11.2.1 ARRL)

In fft of this modulated waveform, we expect frequency component at $f_c$ and upper and lower sidebars (although with less amplitude because our information has lower amp) at $f_c \pm f_m$

multiplying (in other words, modulating) a carrier with a single tone results in the tone being translated to frequencies of the sum and difference of the two. 
Thus, if a transmitter were to multiply a 600 Hz tone and a 600 kHz carrier signal, we would generate additional new frequencies at 599.4 and 600.6 kHz. If instead we were to modulate the 600 kHz carrier signal with a band of frequencies corresponding to human speech of 300 to 3300 Hz (the usual range of communication quality voice signals), we would have a pair of information-carrying sidebands extending from 596.7 to 603.3 kHz.