# Robonomics Grant Diary

> Only the GitHub account, which is responsible for the pull request of the accepted proposal is allowed to submit diary.

*NB!* Please note that we are switched to user "potanin" as grant reporter from user "anissiy" for convenience. Sorry about that!

* **Project Name:** AgriDataTrade
* **Proposal**: https://github.com/airalab/robonomics-grant-program/blob/main/proposals/agridatatrade.md

---
## Grant Diary no. 4

* **Date**: 10.12.2021

* Good news! We have two $8,000 Hach N sensors assembled and ready to go. We have two little boxes with Arduino communicating via local mobile network. The sensors will be connected via modbus to the Arduino box and the Arduino box will then use MQTT to talk to a server at VUW. The server at VUW will then create a Node for each sensor on the Robonomics.Network!

* We plan to deploy them on the actual farm over the next few weeks and tidy up the front end and signing the data to be able to trust each deployed sensor (which can still be manipulated if say someone were to move it physically - so we need to audit the deployed sensors to ensure they are not tampered with).

* There is an identified issue with storing "time series" data on the blockchain as the entire history gets duplicated when the new "link" is created - which means our data may be too large really quickly to store on the blockchain. We are working through these issues.

* We are exploring 3 other manufacturers in addition to Hach and also planning to use SDI-12 rather than modbus. The others are:

1. [http://www.hydrometrics.co.nz/](http://www.hydrometrics.co.nz/)
2. [https://www.trios.de/en/nico-plus.html](https://www.trios.de/en/nico-plus.html)
3. [https://ecodetection.com/technology/](https://ecodetection.com/technology/)

* We have planned meetings with the above three companies over the next couple of weeks before Christmas. While Hach uses "pH sensor" in combindation with conductivity to detect Nitrates, the other three use UV sensors to detect N concentration in the water and may be more reliable to deploy long term with less maintenance than Hach.

## Grant Diary no. 3

* **Date**: 17.11.2021

* While we are ready to deploy the sensors, we have yet another problem with Hach delivering the sensors - we received half of the order for the two sensors with batteries missing in both and delayed until mid January. I will amend this with Hach email when they will list all the ETA's as soon as I get them. We would be interested in exploring alternative N sensors but Hach seem to be the "state of the art" ones as far as we can tell so far. So we will look at alternatives now while waiting for Hach HL4 to arrive in mid January.

* Plan B is to develop the site and connect to Robonomics with "dummy data" until the real sensors arrive so we can get the infrastructure working and explore token creation as originally proposed. [https://frontend-agridata.vercel.app/map](https://frontend-agridata.vercel.app/map).

* We are now looking at alternative sensor to Hach HL4: [http://www.hydrometrics.co.nz/Specifications/](http://www.hydrometrics.co.nz/Specifications/) - we will keep you posted.

## Grant Diary no. 3

* **Date**: 17.11.2021

* While we are ready to deploy the sensors, we have yet another problem with Hach delivering the sensors - we received half of the order for the two sensors with batteries missing in both and delayed until mid January. I will amend this with Hach email when they will list all the ETA's as soon as I get them. We would be interested in exploring alternative N sensors but Hach seem to be the "state of the art" ones as far as we can tell so far. So we will look at alternatives now while waiting for Hach HL4 to arrive in mid January.

* Plan B is to develop the site and connect to Robonomics with "dummy data" until the real sensors arrive so we can get the infrastructure working and explore token creation as originally proposed. [https://frontend-agridata.vercel.app/map](https://frontend-agridata.vercel.app/map).

* We are now looking at alternative sensor to Hach HL4: [http://www.hydrometrics.co.nz/Specifications/](http://www.hydrometrics.co.nz/Specifications/) - we will keep you posted.

## Grant Diary no. 2

* **Date**: 18.10.2021

* The latest updated ETA for the two Hach sensors is 2nd of November 2021 (with a possible up to 10 days delay).
* Leon has designed a simpler box with Arduino low power board inside that can basically survive on batteries for 90 days (the maxmimum interval we can leave sensor alone before we need to replace pH tablets and recharge the sensor battery), so solar power will be bonus but not absolutely required to deploy for 3 month periods at a time.
* The board will communicate over MQTT to the VUW based server with a signed data that will be unique to each sensor. This way we can avoid having to have a node running on each sensor or require more powerful boards. Even if we did that the sensor can be tampered with and the trust of data can only come from regular audits that the sensor is in the exact state we left it when we installed it.
* Trust of the data remains an issue.
* Using IPFS for time series data is also an issue that appears that IPFS is not suitable for frequent updates like we plan (the transaction cost may become prohibitive). We will explore this further before the sensors arrive in a few weeks.
* Some of the ongoing work on MQTT connector is here: [https://github.com/AgriData-Trade/robonomics_mqtt](https://github.com/AgriData-Trade/robonomics_mqtt)

## Grant Diary no. 1

* **Date**: 01.10.2021

We have decided to order the following Hach sensor components as the initial set of 2. All amounts are in New Zealand Dollars (NZD):

TWO SENSORS:

* (Line 2 PN 2001H) Top casing: $4544 (HL4) - x2 (qty)
* (Line 5 PN 2001H) pH attachment with refill ($688) - x2 (qty)
* (Line 10 PN 2001H) Nitrate attachment ($827) - x2 (qty)
* (Line 14 PN 2001H) Conductivity attachment ($592) - x2 (qty)
* (Line 20 PN 2001H) 25M Deployment Cable ($799) - x2 (qty)
* (Line 21 PN 2001H) RS485 ($321) - x2 (qty)

CONSUMABLES:

* (Line 11 PN 2001H) 3-month supplies of pH pellets at $259 - x4 (qty)
* (Line 6 PN 2001H) pH ref solution ($15.70) - x1 (qty)
* (Line 7 PH 2001H) salt tablets ($15.70) - x1 (qty)
* (Line 9 PN 2947600) pH Solution Kit ($41.90) - x1 (qty)
* (Line12 PN 2001H) Low Range Nitrate Solution ($43) - x1 (qty)
* (Line13 PN 2001H) High Range Nitrate Solution ($43) - x1 (qty)

FREIGHT: $50

TOTAL: $16787.30 + GST

We have ordered these and are now waiting for the first two sensors to be delivered over the next month or two.

In the meantime, we have managed to get ESP32 board to connect to the Robonomics network as a node and we are designing a separate box that will house ESP32 with some 12v batteries to process the data coming from each Hach sensor and send it over CAT-M1 ([https://www.spark.co.nz/shop/mobile/network/](https://www.spark.co.nz/shop/mobile/network/)) network while being deployed in the field for several years. The sensor requires every 3 months "ph pellets" replacements as maintentance and every 9 months battery charging. Thus our box will be able to operate on its own for at least 3 months or more, using solar power and 12v batteries inside.
