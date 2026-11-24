# Changelog

## 0.1.1

- Keep device, family and virtual subdevice keys out of the data class
  `repr`, so logging them does not write the keys to the log.
- Log a warning when a gateway session moves to a new address, and document
  that the session trusts the local network.
- Raise `ProtocolError` instead of a `cryptography` error when an encrypted
  LAN response is not a multiple of 16 bytes.
- Document the `local_mac` sent in discovery and heartbeat responses.

Thanks to @DAB-LABS for the review (#1).

## 0.1.0

First release. The protocol code moves here from the `broadlink_async.magic`
package proposed for broadlink-async.
