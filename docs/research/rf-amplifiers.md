# RF amplifiers

Typically use bjts/semiconductor devices not op amps due to higher frequencies

![[typical-rf-amplifier.png]]
>[!Warning]
>This might be for transmitting, not receiving 

Use a single transistor to obtain wide bandwidth, well-controlled gain and well-controlled, stable input and output resistances. Several of these amplifiers can be cascaded to form a high gain circuit that is both stable and predictable

## Common emitter amplifier
https://www.youtube.com/watch?v=zXh5gMc6kyU
https://www.youtube.com/watch?v=IrAUC4ZoNYY&list=PL4ZSD4omd_AzYwgiAXCOsR1eyy3lHsTig

### Configuration
![[common-emitter-amp.png]]

### Input
`R1` and `R2` set and their source set the bjt into amplification mode. 
> `C1` blocks DC current, so as far as biasing is concerned it doesnt exist. Lets the AC signal in without messing with the DC bias.

$V_{BE}$ typically $0.6-0.7\ V$.

Ignoring the base current which brings the $V_b$ down a little bit, we have (at operating point)
$$
\begin{align}
V_b &\approx V_{cc} \frac{R_2}{R_1 + R_2} \\
&= 5 \frac{3.9k}{13.9k} = 1.4\ V
\end{align}
$$
>[!Info]
>Note this $V_b$ is the DC operating point but the actual voltage at that point is $V_b = V_{DC} + V_{sig}$ so we'd actually have $1.4 + 0.01\sin(1000t)$

So the AC signal wiggles about $1.4\ V$

$V_E \approx V_B - V_{BE} = 1.4 - 0.7$ 

### Output

Note that $I_c \approx I_e$

$I_E=I_C+I_B$

And since

$I_C=\beta I_B$

if, say, $\beta=100$:

$I_C=100I_B$

then
$I_E=100I_B+I_B=101I_B$

So $I_C$ and $I_E$ are extremely close:

$\boxed{I_E\approx I_C}$

`R3` sets/stabilises the emitter current:

$I_E=\frac{V_E}{R_3}\approx I_C$

`R4` converts changes in collector current into changes in output voltage:

$V_C=V_{CC}-I_CR_4$

So when the input rises:

$V_B\uparrow\Rightarrow I_C\uparrow\Rightarrow V_{R4}\uparrow\Rightarrow V_C\downarrow$

Hence the collector output is **amplified and inverted (180° phase shift)** relative to the input.

### Small signal model
Rule of thumb for CE gain is $A_v \approx \frac{-R_c}{R_e}$
but use small signal model for actual analysis

Useful for gain, input/output resistance and for coupling capacitor cutoffs

### Design considerations

Choose C so that the frequencies we care about arent attenuated. Essentially an RC filter.
> Tricky bit is what is R here?

$$
\boxed{f_c=\frac{1}{2\pi R_{\text{seen}}C}}
$$
The capacitor sees several paths to ground. Need small signal model for this.


