# broadlink-magic

Python library for the local LAN protocol of BroadLink Magic Home families,
maintained by BroadLink. It powers the Broadlink Magic Home integration in
Home Assistant.

A Magic Home family is set up in the BroadLink app. The family's gateways
(for example the RM MAX) connect to a UDP server on the local network
(port 12346 by default). The server answers discovery and heartbeat messages,
receives status uploads, and sends control packets for the family's devices.

## Install

```bash
pip install broadlink-magic
```

Requires Python 3.13 or newer.

## What it covers

- Parsing the family export the BroadLink app uploads (`import_data`).
- The gateway session: message framing, discovery, heartbeat, status upload
  and query, and control (`inbound`, `gateway`).
- Payload encoding for lights, switches, curtains, air conditioners and
  three-in-one climate devices.
- Remote-controlled devices learned on an RM MAX (`remote`).

## Development

```bash
python -m venv .venv
.venv/bin/pip install -e ".[dev]"
.venv/bin/ruff check .
.venv/bin/ruff format --check .
.venv/bin/pytest
```

## Releases

Pushing a `v*` tag that matches the version in `pyproject.toml` publishes the
package to PyPI through trusted publishing. See `CHANGELOG.md`.

## License

MIT. See `LICENSE`.
