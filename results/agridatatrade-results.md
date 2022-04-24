# Robonomics Grant Results

- **Project Name:** AgriDataTrade
- **Proposal**: https://github.com/airalab/robonomics-grant-program/blob/main/proposals/agridatatrade.md
- **Grant Diary**: https://github.com/Darkflame72/robonomics-grant-results/blob/main/diaries/agridatatrade-grant-diary.md

## Deliverables

| No. |       Deliverable        |                        Link                        | Notes |
| :-: | :----------------------: | :------------------------------------------------: | :---: |
|  1  |    Arduino Datalogger    |     https://github.com/AgriData-Trade/hardware     |  ...  |
|  2  | MQTT to Robonomics relay | https://github.com/AgriData-Trade/Robonomics-Relay |  ...  |
|  3  |     Data visualiser      |     https://github.com/AgriData-Trade/frontend     |  ...  |

---

## Findings

### Sensor

#### Sensor hardware

Initially a [HL4](https://www.ott.com/products/water-quality-2/hydrolab-hl4-multiparameter-sonde-54/) sensor was used to collect water quality data from the water. It collected a mix of NO3, conductivity, pH and temperature. It used chemical sensors to measure the values which after a month of operation become unreliable in such conditions. As the sensor was deployed to a remote location, it was difficult to maintain making remote sensor deployments difficult.

Communication with the sensor wwas conducted over SDI-12 as it provided an easy protocol which was compatible with exisitng systems and made integrating it into the monitoring system simple. While a protocol such as Modbus was also available it had the downside of requiring custom code for each different sensor making long term changes to the sensor difficult. This would make the monitoring system reliant on a single vendor which would reduce trust in the system due to the lack of options.

A TriOS Nico sensor is currently being tested which uses a laser to measure the NO3 values making it reliable for a long period of time. The new system is still under development and testing and does not yet have any findings. As SDI-12 was used for the sensor base it has been easy to integrate the TriOS sensor into the monitoring system.

#### Remote operation

New Zealands farms and specifically the river systems around them are often located in rural areas with poor access to the internet. This makes it difficult to deploy the sensor as it would require a large amount of data to be collected and sent to the internet. Cellular networks are the only option for remote operation as they are the only connection possible for the monitoring sites. The same issue applies to power so the sensor relies on a solar panel and battery for power.

Due to both power and network constraints each monitoring sensor cannot directly connect to the Robonomics network requiring the use of gateways servers to provide a connection. The monitoring system uses MQTT to relay the data to the gateway server. This enables the minimal possible amount of data to be transmitted over the cellular network enabling data to be kept under 10mb a month with 3 hour measurements.

#### Gateway server

Gateway servers are required to relay the data from the sensors to the Robonomics Network for transparency and trust of the data. The gateway server operates a mosquitto mqtt server with a connected [relay program](https://github.com/AgriData-Trade/Robonomics-Relay) which based on each sensor will save the data to the Robonomics Network. These gateway servers are required for any remote monitoring systems as each sensor is not able to run a node directly.

#### Long term deployment of sensors

Long term deployment of monitoring sensors presented a number of unforseen challenges around the location and access to the sensors. The weather systems in New Zealand often have large periods with minimal rainfall with occasional heavy rainfall. This makes the water level raise drastically for short periods requiring extra thought into placement. The first deployed sensor encounted this issue when during a large rainfall a broken tree branch floated down and collided with the monitoring setup causing damage to the monitoring device and sensor cable.

For reliable deployment of the sensor a location shielded from potential debri is required along with a suitable location above the maximum possible water line for the monitoring system and solar panel to be located.

### Verification and Validation

With a digital twin system having the physical and digital twins corrospond to the correct ones with verification is a challenging concept. Inside of the blockchain data is immutable and can not be changed. The data is stored in the blockchain and can be verified by the blockchain along with the address that posted it. This allows the data once on the blockchain to be trusted and used for trading and forcasting.

With the physical half of the twin system, the data is collected from a physical sensor which is then sent to the blockchain. As there is no way to validate that the sensor measurements are correct and the sensor has not been tampered with the data is never trusted as being correct and is instead only verified as from that sensor. This has implications to the token trading and forecasting model around identifying bad actors and invalid data.

For verification of the correct source of the data each sensor node has a unique certificate which it uses to communicate with the mqtt server. This allows the relay to know that only the autherised sensor is sending data to it so it can be updated inside of the blockchain. Each of the sensor nodes has a unique blockchain address which publishes the received data from the physical node. This means that the digital twin is always up to date with the data.

### Data Storage

#### Datalog

Each data point (taken every 3 hours) is stored as a Datalog transation in the Robonomics Parachain under the digital twin account. The data is stored in minified json to allow all the sensor values to be recored in a single block without getting split up or requiring more then one transaction. The data is stored in the following format:

```json
{
  "temperature_kelvin": 0,
  "nitrate_mg_P_L": 0,
  "nitrate_mV": 0,
  "specificConductivity_mS_P_cm": 0,
  "salinity_psu": 0,
  "totalDissolvedSolids_g_P_L": 0,
  "rawCoductivity_uS_P_cm": 0,
  "pH_units": 0,
  "pH_mV": 0,
  "referece_mV": 0
}
```

As the each data point is stored under the digital twin account the data can be queried by searchign for transactions within a certain time period and then the corresponding transactions are the data points. This provides a seamless verifiable data storage system.

#### Transaction cost

Due to transaction fees there is a cost to each transaction (data point) stored on the network. This is taken at the initial storing time in the form of a fee and covers the work done to create the block of data sotred on the network. The transaction fee can be covered by a collator on the network for around 30 nodes but for a larger deployment this is not possible. For a full monitoring system the fees will have to be paid for by the marketplace which trades the data and is the topic of the current research ongoing.
