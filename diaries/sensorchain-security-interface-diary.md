# Robonomics Grant Diary

* **Project Name:** Location based identities in industry 4.0 production
* **Proposal**: https://github.com/airalab/robonomics-grant-program/blob/main/proposals/sensorchain_security_%20interface.md

---

## Grant Diary no. 1

* **Date**: 01.02.2022 - 11.02.2022

### Requirements and Development of Testing Scenarios
* Set up and tested the fischertechnik [factory](https://www.fischertechnik.de/en/service/elearning/simulating/fabrik-simulation-9v) and cloud
* Developed requirements regarding the fischertechnik factory, especially for the project use-cases
* Defined scenarios for the testing of the requirement fulfilment:
    1. High-bay warehouse behaves correctly
    2. To simulate ageing of one of the high-bay warehouse delivery cranes, a slight parameter drift is implemented
    3. At first, the high-bay crane behaves correctly, but it becomes more and more destructive the higher its trust score is
    4. The high-bay crane delivers wrong parts on purpose

### Adjustments to the Model Factory
* Determined necessary adjustments of the factory for the testing scenarios
    * Second high-bay warehouse crane
    * Changes to part delivery process to accommodate the second high-bay crane
    * Incorporation of additional RFID sensors and tags into the factory
* Checked if the additional parts fit into the training factory
* Got offers for the additional parts

### Software
* Did research on existing software to be used as basis for the development
* forked the [repository](https://github.com/fischertechnik/txt_training_factory) of the factory software as a basis for further development 

---

## Grant Diary no. 2

* **Date**: 14.02.2022 - 25.02.2022

### Adjustments to the Model Factory
* Ordered additional parts for the Factory
* Added additional parts to the Factory
* Evaluated the ideal Positioning of the Localization Sensors and Tags

### Software
* Started to work with the existing software for the Training Factory
* Set up the Toolchain for programming the Training Factory
* Started to implement the software for the new Factory Setup with the additional parts

### Literature Research
* Did additional Research for the Localization interface