# Ninebot Scooter integration for Home Assistant

**NOTE: This is integration has some known bugs in it and is in an alpha state. It is also a bit stale in development due to lack of mainatiner time. Feel free to fork or help pushing PRs improving this integration.** 


this fork changes line 69 from
`PassiveBluetoothProcessorEntity[PassiveBluetoothDataProcessor[str | int | None]],` to
`PassiveBluetoothProcessorEntity[PassiveBluetoothDataProcessor[str | int | None,1]],` 

This fixes issue and scooter pulls data  but fails to continuously pull info from scooter with `error Failure while polling. TimeoutError: Did not get a response on Packet[PC -> ES_BLE, cmd=INIT, idx=00]`

It connects and poll data from a Ninebot Scooter using BLE.

## Manual installation

1. Copy the directory `custom_components/ninebot_scooter` into you installation under
   `<config_dir>/custom_components`.

2. Restart home assistant.
