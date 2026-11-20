<p align="center">
  <img src="pulzr-mark.png" width="96" alt="Pulzr">
</p>

<h1 align="center">Pulzr</h1>

<p align="center">
  <b>One platform for every wireless and wired IoT network.</b><br>
  LoRaWAN, Bluetooth, Zigbee, Z-Wave, Thread, Matter, Modbus and IP devices,<br>
  on gateways you plug a radio into and a console that manages them all.
</p>

<p align="center">
  <a href="https://pulzr.net">pulzr.net</a> ·
  <a href="https://app.pulzr.net">Console</a> ·
  <a href="https://app.pulzr.net/docs">Docs</a> ·
  <a href="https://pulzar-net.github.io/PulzrOS/">PulzrOS</a>
</p>

---

We build the gateway OS, the radio stacks and the tools that sit under Pulzr in
the open. Everything here is maintained by Pulzar and usable on its own,
with or without the Pulzr platform.

### Gateway

| | |
|---|---|
| [**PulzrOS**](https://github.com/pulzar-net/PulzrOS) | The gateway OS: OpenWrt with LoRaWAN, radio detection, add-ons and over-the-air updates. [Docs](https://pulzar-net.github.io/PulzrOS/) |
| [**pulzr-edge**](https://github.com/pulzar-net/pulzr-edge) | The edge daemon: one process per radio or bus, store-and-forward, one protocol to the platform. |

### Radio stacks

Host stacks in Rust, each with a standalone bridge to MQTT and Home Assistant.

| | |
|---|---|
| [**zigbee-bridge**](https://github.com/pulzar-net/zigbee-bridge) | Zigbee coordinator stack: Silicon Labs EZSP, TI ZNP and ConBee; backups, OTA, mesh mapping. [Docs](https://pulzar-net.github.io/zigbee-bridge/) |
| [**zwave-bridge**](https://github.com/pulzar-net/zwave-bridge) | Z-Wave controller stack: Serial API, S0 and S2, SmartStart, Long Range, NVM backup. [Docs](https://pulzar-net.github.io/zwave-bridge/) |
| [**bluetooth-bridge**](https://github.com/pulzar-net/bluetooth-bridge) | Bluetooth host stack over raw HCI: scanning, advertising, GATT, pairing, Mesh. [Docs](https://pulzar-net.github.io/bluetooth-bridge/) |
| [**matter-bridge**](https://github.com/pulzar-net/matter-bridge) | Matter controller on rs-matter: commissioning over IP, Bluetooth and Thread. [Docs](https://pulzar-net.github.io/matter-bridge/) |

### Device libraries

| | |
|---|---|
| [**zigbee-codec-catalog**](https://github.com/pulzar-net/zigbee-codec-catalog) | Every zigbee-herdsman-converters definition as a standalone codec, one release per upstream version. |
| [**zwave-config-catalog**](https://github.com/pulzar-net/zwave-config-catalog) | Z-Wave JS's device configuration lookup as one script for any JavaScript engine. |
| [**codec-test**](https://github.com/pulzar-net/codec-test) | Run LoRaWAN payload codecs the way ChirpStack and The Things Stack do, against their test vectors. |
| [**oui**](https://github.com/pulzar-net/oui) | MAC address vendor lookup as small static files, rebuilt weekly from the IEEE registries. |

### Build on Pulzr

| | |
|---|---|
| [**pulzr-sdk**](https://github.com/pulzar-net/pulzr-sdk) | The Python and TypeScript SDKs for the Pulzr API. |
| [**pulzr-package-sdk**](https://github.com/pulzar-net/pulzr-package-sdk) | Build gateway packages and carrier drivers as sandboxed WebAssembly: the ABI, a Rust SDK and the `pulzr-pkg` CLI. |
| [**perses-pulzr-datasource**](https://github.com/pulzar-net/perses-pulzr-datasource) | Pulzr data in Perses dashboards, with a family of panel plugins beside it. |
| [**docs-theme**](https://github.com/pulzar-net/docs-theme) | The Starlight theme and starter every project here uses for its docs. |

### LoRaWAN

| | |
|---|---|
| [**basicstation-gate**](https://github.com/pulzar-net/basicstation-gate) | A LoRa Basics Station front door and CUPS server for ChirpStack and other network servers. |
| [**lorawan-locate**](https://github.com/pulzar-net/lorawan-locate) | Locate LoRaWAN devices from the gateways that heard them: TDOA, RSSI multilateration, centroid. |
| [**sx1302_hal**](https://github.com/pulzar-net/sx1302_hal) | The SX1302 concentrator HAL and packet forwarder PulzrOS builds on. |

---

**Security:** report vulnerabilities privately through each repository's
*Security → Report a vulnerability*, never in a public issue.
**Contributing:** each repository's `CONTRIBUTING.md` explains how to build,
test and send a change.
