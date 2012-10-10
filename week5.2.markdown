# Skinny

## Basic Header Format

* all Skinny messages start the same but are then modified based on messages
* ID
* Fields
	* data length (4 bytes) - amount of information carried beyond the header version
	* header version (4 bytes) - default is 00...meaning skinny basic
	* message ID (6 bytes) - provides the hexadecimal value for the SCCP type
	* packets vary quite a bit in size and purpose
	* beyond this, type specific

## Stages

1. DHCP (options 66, 150, 176) (next-server)
2. TFTP
3. Register
4. (start call) Phones contact call manager with number dialed
5. Call server contacts destination phone
6. Call server informs both ends about parameters for the call
7. Phones communicate with RTP
8. One of phones terminates
9. Call manager performs cleanup

# T-1

* 24 channels
* can carry voice or data
* 1.544 Mbps
	* 64 kbps each channel (G.711)
	* 8x24 = 192 bits
	* 192 + 1 framing bit = 193 bits
	* 193 x 8000 = 1,544,000 bps
* full duplex
* 2 pairs of wire
	* pins 1+2 Rx from the network
	* pins 4+5 Tx to the network

## Frames

* in NA use either superframe (D4)
	* AT&T pub 62411
	* group of 12 T1 frames used to align and sync equipment
* or extended superframe (ESF)
	* AT&T pub 54016
	* a group of T1 frames
	* has a 4k maintenance channel
	* 2k reserved for CRC-6 check
	* 2k for synchornization

## Physical layer

* either AMI or B8ZS
* alternate mark encoding