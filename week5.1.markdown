# Codecs

## G.711

* PCM, 64kbps, 8 bits/sample, 8000 sample/sec
* µ-Law, A-Law
* Waveform

## G.726

* ADPCM, 40/32/16/24 kbps

## Source codecs

* compress speech by sending metadata instead of quantized sample values

* Linear Predictive Code (LPC)
* Code executed linear prediction (CLEP)
* Multipulse multilevel quantization (MP-MLQ)

## G.729

* CELP into 8kbps streams
* similar to 32 kbps ADPCM

## G.723

* very low bitrate
* compression
* 5.3 kbps CELP
* 6.3 kbps MPMLQ 

## G.722

* ADPCM at lower data rates but higher sample rates

# Skinny Client Control Protocol (SCCP)

* Skinny
* less overheard than H.323 and the messages are easier to 
* Skinny is proprietary. Many Cisco phones are deployed with Skinny and CM/CME
	* Cisco is converting to SIP
* the original SIP RFC is limited in its feature set
	* Skinny supported more stuff
* TCP port 2000
* enables the connection of two clients via a call manager
* clients establish a pervasive connection with the CM
	* remains until phones are powered off (keepalive)
* after connection the phones communicate directly via RTP

* H.323 and Skinny (SCCP) are binary protocols
* SIP is ASCII

## Call Manager Express

* entry level solution integrated into IOS
* SOHO
* reasonable set of features
* components
	1. ephone (voice register pool)
		* typically represents a phone but can be a port to a mail system, etc.
		* provides phone config
		* phones can have multiple extensions and extensions can go to multiple phones
	2. directory number (dial number)
		* connects voice channel to the phone
		* virtual port