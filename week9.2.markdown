# SIP

Session Initiation Protocol

* Invite messages
	* can be multiple in a session
	* a method that tells the requester what to do
	* has header fields
	* what the fuck am I doing with my life?
* Headers include 

Larry Hill doesn't know what he's talking about; read the fucking wikipedia article about SIP.

## Components

* UA - user agent - logical portion that initiates or responds to SIP transactions (client/server) (stateful)
* UAC - user agent client - requests and accepts responses
* UAS - user agent server - accepts requests and responds
* proxy - forwards requests from a UAC to UAS or another proxy, primarily for routing, can participate in auth
* redirect server - sends UAC to alternate sets of URIs
* registrar server - handles register messages

## Addressing

* sip:user@domain:port
* sip:user@host:port

SIP - port 5060
SIPS - port 5061

## Messaging

* INVITE
* ACK
* OPTIONS
* BYE
* CANCEL
* REGISTER