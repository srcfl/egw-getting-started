# Enhanced Energy Gateway API Documentation

Welcome to the Energy Gateway (eGW) API documentation. The eGW offers a RESTful API for configuration and management. This document outlines the necessary details to interact with the API, configure your eGW, and effectively utilize its features. 

## API Endpoint
The eGW API is accessible at: `http://EGW-LOCAL-IP-ADDR/api/`. Ensure the eGW is connected to the internet via ethernet for initial setup and obtain the local IP address for access.

## Response Status Codes
- `200`: Request successful.
- `400`: Malformed request.
- `500`: Internal server error; valid request but eGW could not process.

## Quick Navigation
- [WiFi Configuration](#wifi)
- [Device Naming](#name)
- [Initialization](#initialize)
- [Inverter Configuration](#inverter)
  - [Modbus TCP/IP](#invertertcp)
  - [Modbus RTU](#inverterrtu)

## WiFi Configuration
Configure the WiFi settings by sending a POST request with your network details to `/api/wifi`.

**Endpoint:** POST `http://EGW-LOCAL-IP-ADDR/api/wifi`

**Payload:**
```json
{
  "ssid": "YourNetworkSSID",
  "psk": "YourNetworkPassword"
}
```

## Device Naming
Each eGW has a unique name identifiable in the backend and explorer. Fetch this name via a GET request to enhance device management.

**Endpoint:** GET `http://EGW-LOCAL-IP-ADDR/api/name`

## Initialization
Connect your eGW to a wallet for reward management. Set the wallet address with a POST request.

**Endpoint:** POST `http://EGW-LOCAL-IP-ADDR/api/initialize`

**Payload:**
```json
{
  "wallet": "YourUniqueWalletAddress"
}
```

## Inverter Configuration
Configure your gateway to interact with inverters using Modbus TCP/IP or RTU (future hardware support).

### Modbus TCP/IP
Set up the eGW to communicate with an inverter over Modbus TCP/IP.

**Endpoint:** POST `http://EGW-LOCAL-IP-ADDR/api/invertertcp`

**Payload:**
```json
{
  "ip": "InverterIP",
  "port": 502,
  "type": "InverterType",
  "address": 1
}
```

### Modbus RTU
Future support for Modbus RTU configuration. Details will be similar to Modbus TCP/IP with specific serial connection parameters.

**Endpoint:** POST `http://EGW-LOCAL-IP-ADDR/api/inverterrtu`

**Payload:**
```json
{
  "port": "SerialPort",
  "baudrate": 9600,
  "bytesize": 8,
  "parity": "N",
  "stopbits": 1,
  "type": "InverterType",
  "address": 1
}
```