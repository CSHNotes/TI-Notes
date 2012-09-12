# Telephony Integration 1

**WARNING**: My notes are totally all over the place today

# ACRONYMS WOO
- POTS - Plain Old Telephone Service
- PSTN - Public Switched Telephone Network
- DTMF - Dual Tone Multi-frequency signaling
	- send two frequencies with each tone
- SLC - Subscriber Line Card
- codec - COder/DECoder
- PBX - Like a switch but for phones

# Analog POTS
- PSTN uses SS7
- Defined by ITU-T recommendations (kind of like RFCs)
- Circuit switched vs packet switched
- Phone -> via analog wave -> local loop -> Telco switch (SLC (codec)) -> PSTN
- 0-4000Hz (really 300-3400Hz)

## Local loop
- two wires:
	- tip
	- ring

# Digital POTS?
- Phone -> PBX (like telco switch (both analog and digital cards))
- Digital phone handles analog to digital conversion
- Digital gives us features!

# VoIP
- AKA IP Telephony or Computer Telephony Integration (CTI)
- transport of voice, video or games over an IP network
	- really, anything that occurs in real time
- The same functions occur but in a fundamentally different way
- transport type is traditionally 802.3 or 802.11
- standards have been developed that govern transport (TCP) but we also need standards for signaling as well as call control
- transport is typically UDP but signaling is often TCP
- both ends still need codecs (PCM)
	- G.711
- **NOTE**: all the same processes must occur

- Phone -> ethernet switch -> VoIP PBX
- Traditional phone messages wrapped in delicious, delicious IP
## Protocols
###Signaling
- H.323
- SIP
- Skinny
### Transport
- RTP
- RTCP

# Reasons to migrate from POTS to VoIP
- Lower operational cost
- One set of net admins
- Unified infrastructure
# Reasons not to migrate
- Separation of concerns
- Don't want to hire VoIP people
- Possibly better uptime with digital phone networks