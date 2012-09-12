# PCM

## G.711

* codec that goes along with PCM
* most popular method to encode audio
* waveform is sampled continuously at regular intervals (8000 sec)
	* (4000 x 2) - from bandwidth of a voice channel
* samples are used to recreate the the analog signal at the receiver
* the number of bits allocated to each sample provides the detail level
	* 8 bits - 256 possible values
* the rate of sampling affects the accuracy
	* higher number of bits and higher number of samples = much greater accuracy

# Frequencies

* We can hear about ~20Hz - 20kHz
* We can generate sounds up to about 3-4kHz
* local loop bandwidth - 300-3400Hz
* recall the DTMF dialpad
	* previously: rotary dial used pulses
* DSL works by transmitting with frequencies that aren't used for the voice circuit

## Analog Transmission

* Difficult to transmit end-to-end
* Noise
	* Additive
	* Subtractive
	* Amplification just amplifies the noise
* Modulate voice into carrier wave
	* Difficult to multiplex
* Attenuation

## Digital Transmission

* encode the data and send this to the other end
* then recreate the analog signal
* better signal cleanup
	* Error checking
	* Deal with some attenuation and noise problems

# General Codecs

* Coder/decoder
* Convert analog to digital samples and vice versa
* Codec selection can be very important for compatibility, performance, quality and cost
	* selecting the wrong codec can mean that endpoints can't understand each other
	* many times switches do conversion between codecs
		* ex. G.711 <-> G.729
		* a bit of data lost in conversion
	* all devices need to support all codecs used
* not all codecs are supported everywhere by all products
* most of the commonly used codecs are ITU-T standards
	* G series
	* H series
* for analog lines, the codec exists in the SLC or switch
* for digital phones, the codec is local
	* signal traveling to/from the 
* many codecs offer some form of compression!

## Audio

* Use a variety of techniques to represent the original signal
* PCM and adaptive differential PCM (ADPCM) are waveform techniques that directly sample the audio stream
	* compression is accomplished by exploiting redundant characteristics of the wave
* source codecs compress speech by sending only parametric information about the voice
	* uses less bandwitdth
	* methods
		* linear predictive coding (LPC)
		* code selected linear prediction (CELP)
		* multipulse multilevel quantization (MP-MLQ)