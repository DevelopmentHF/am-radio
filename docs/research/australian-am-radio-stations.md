# Australian AM radio station specifications

The baseband audio frequency bandwidth itself is typically restricted to about $9\ kHz$ on either side of carrier frequency


Mimicked stations + broadband noise in ltspice using 

`V= 100u*sin(2*pi*693k*time)*(1+0.5*sin(2*pi*1k*time))+200u*sin(2*pi*774k*time)*(1+0.4*sin(2*pi*700*time))+50u*sin(2*pi*855k*time)*(1+0.6*sin(2*pi*1.3k*time))+10u*white(time*1e6)`
