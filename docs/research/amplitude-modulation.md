# Amplitude modulation (AM)

Info impressed onto a carrier wave $c(t) = C\sin(2\pi f_ct)$
> Single frequency carrier, i.e 693 kHz

Information is encoded on $m(t) = M\cos(2\pi f_m t)$

Perform modulation by multiplying these two together. 
For a single tone modulating signal, $am(t) = c(t) * (1 + m(t))$
> the 1 represents a DC component to allow the envelope to both increase and decrease (see 11.2.1 ARRL)

In fft of this modulated waveform, we expect frequency component at $f_c$ and upper and lower sidebars (although with less amplitude because our information has lower amp) at $f_c \pm f_m$
