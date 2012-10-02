# Codecs

codecs - coder/decoder

* the basic task is to take an analog waveform, convert it to digital data, and then back to analog at the receiver
	* without using too much bandwidth
	* without losing too much of the original signal

# First problem: sampling

* the waveform has to be sampled periodically - so, the amplitude of the waveform is recorded
* aliasing - decoded frequency is a different waveform than encoded frequency
* too much - too much bandwidth
* Right amount:
	* Nyquist
	* 2x highest frequency
	* 8000 samples/sec
	* 1 sample/125 µsec
	* 8 bits/sample
	* 64 kbps circuit
* sampling - pulse amplitude modulation

## Quantizing

* need polarity
* Quantization assigns a binary value to the samples in prep for transmit

### Linear Quantizing

* assign a value to each sample as you go
* quantization error - the difference between actual and assigned values
* in order to reduce the quantizing error we can provide a greater set of values
	* closer to the actual value
* QE causes distortion because the decoded signal is not the same as the original
* QE is a greater problem for low volume or low amplitude signals

### Logarithmic Quantizing 

* cue can sample at greater frequency when dealing with low amplitude signals
	* bandwidth is constant
* Another way of looking at the problem is to provide more sample values for the low amplitude signals
* low volume samples are less affected by QE but we provide fewer values for high amplitude signals
* amplitudes are divided into segments with each segment having a different # of values
* for voice + the PSTN, most are covered by G.711 µ-Law and A-Law

## Compression

* are there repeating characters
* dead air
* repeated patterns

## Transmission

* parity bit
* segment
* value

# Codecs

* G.711 (PCM) and G.722 (ABPCM) are waveforms that follow this process
* G.723 is an example of a source codec which compresses speech by sending metadata
	* less bandwidth
* methods
	* Linear Predictive Coding (LPC)
	* Code Executed Linear Prediction (CELP)
	* Multipulse Muiltilevel quantization (MPMLQ)

## Transcoding

* encoding with one codec and decoding with another
	* occurs even if the same codec is used on both sides
* causes distortion similar to that seen in quantizing error
* some pairings can be disastrous

## Voice transmission enemies

* latency
	* every codec has latency
		* as compression and features increase, so does latency
* jitter
* packet loss
	* results in a significant reduction in quality
	* some codecs survive better than others
	* packet loss concealment (PLC) techniques reduce the impact of packet loss
		* reduce to 0
		* trail off to 0
		* repeat packet
	* PLC algorithms attempt to determine what was going to be there or smooth things out