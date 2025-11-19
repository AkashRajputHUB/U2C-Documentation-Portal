#### <mark>Feature 2467843 : Enhancement in existing JioBharat & JioPhone Plan delay visibility by 48 hrs.</mark>

###### v0.1 Nov'2025

##### Akash Rajput

---

|S NO|Date |Version History|Version|
|---|---|---|---|
|1.|13 Nov 2025|Initial Draft|v0.1|

## Draft Solution Design

##### Impact EBDM, EDIF

---

- Put incoming IMEI into **_```48HOURS list```(new)_**,
  - **_```48HOURS_FLAG = N``` (new)_**
  - Sent to EDIF
  - counter starts for 48 Hrs. to update ```48HOURS_FLAG```
- **Case1 :**
  - No letch event received within 48 Hrs. for the same IMEI
  - After 48 Hrs.
    - Update the ```48HOURS_FLAG = Y```
    - Send it to EDIF
    - Remove entry from ```48HOURS list```

- **Case2 :**
  - Letch event received within 48 Hrs. for the same IMEI
    - IMEI received exists in ```48HOURS list```
    - Remove the entry from the ```48HOURS list```
    - Insert the new entry in ```48HOURS list```
      - After 48 Hrs. (for the new entry, if no further letch event received)
      - Update the ```48HOURS_FLAG = Y```
      - Send it to EDIF
      - Remove from ```48HOURS list```

- _**In CCI to EDIF :**_

> If ```48HOURS_FLAG=Y``` or ```48HOURS_FLAG=NULL```

```sh
Channel to show the JioBharat/JioPhone plan
```

> otherwise

```sh
Channel not to show the JioBharat/JioPhone plan
```

## Flowcharts

```mermaid
graph LR
  A[Start] --> B{Failure?};
  B -->|Yes| C[Investigate...];
  C --> D[Debug];
  D --> B;
  B ---->|No| E[Success!];
