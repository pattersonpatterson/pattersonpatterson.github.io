# Field Support Log Book

_Started on 8/5/2022_

- [Field Support Log Book](#field-support-log-book)
  - [Currently Tracking:](#currently-tracking)
    - [SSM-WAAS-063 Maintainer Laptops](#ssm-waas-063-maintainer-laptops)
    - [CDB Ring 2 Down Hard since 8/6](#cdb-ring-2-down-hard-since-86)
    - [OTZ WRS Temperature Spikes - **OFFLINE**](#otz-wrs-temperature-spikes---offline)
    - [YYR WRE-A - Monitor in Normal](#yyr-wre-a---monitor-in-normal)
    - [MMX WRE-B - **OFFLINE**](#mmx-wre-b---offline)
  - [Upcoming Activities:](#upcoming-activities)
    - [8/15 CM1 Replace Failed KPA](#815-cm1-replace-failed-kpa)
    - [9/12-9/30 LOA for GUS EIRP Update](#912-930-loa-for-gus-eirp-update)
    - [9/13-9/23 POCC Relocation](#913-923-pocc-relocation)
    - [3/24/2023 CY23 Cutover](#3242023-cy23-cutover)
    - [MX Comm Upgrade](#mx-comm-upgrade)
  - [Bad Freq Stds Needing to be Returned](#bad-freq-stds-needing-to-be-returned)
  - [Daily Notes:](#daily-notes)
    - [20220812 Notes](#20220812-notes)
    - [20220811 Notes](#20220811-notes)
    - [20220810 Notes](#20220810-notes)
    - [20220809 Notes](#20220809-notes)
      - [BET WRE-C - Monitor in Normal](#bet-wre-c---monitor-in-normal)
    - [20220808 Notes](#20220808-notes)
    - [20220805 Notes](#20220805-notes)

## Currently Tracking:

### SSM-WAAS-063 Maintainer Laptops
* BRW and OTZ still haven't received laptops; stuck at Anchorage FedEx
  * 7773 0108 9113
  * 7773 0181 7300
* Still to return: 
  * 1x NOC O&M Laptop
  * 1x POC O&M Laptop
  * 6x WRS sites 
* Still to ship international
  1. Coordinate with Fernando and Dave McPhee to return all Legacy Maintainer Laptops to in-country store (Adam)
  2. Organize LCSS requests for all laptops for a one-to-one swap with the Depot




### CDB Ring 2 Down Hard since 8/6



### OTZ WRS Temperature Spikes - **OFFLINE**
* OTZ WRS Control Power OFF since 8/11 14:21
* 8/11 - OTZ WRS Powered down until a site technician can address the HVAC issues (ref [LIR 488764124](https://technetrmlsb.faa.gov/LIR/Details/488764124))

OTZ started seeing temperature spikes on 8/5, and the problem has recurred almost daily. Additionally OTZ WRE-C receiver appears to be more sensitive to temperature shifts and is more susceptible to failure during high temps.

Recommending a site technician **reseat cables on the WRE-C receiver** when they're onsite addressing the HVAC issue




### YYR WRE-A - Monitor in Normal
Spiky Allan Voltage Deviation / Phase Noise; looks like freq std failure

* 8/10 - YYR WRE-A allan voltage deviation seems to be degrading - **reiterate replacement of Freq Std needs to be performed** / EC recommends dropping YYR WRE-A to Maintenance due to WRE Bias Trips
* 8/9 - YYR WRE-A is still showing lots of phase noise, some spikes in allan voltage deviation (up to 1000), AGC is hairy on all bands, but not synchronous; mainly stable and tracking / **EC recommends replacement due to phase noise degradation**
* 8/8 - YYR WRE-A remained in Normal Mode through 8/6-8/8; receiver tracked OK with some phase noise; allan voltage deviation looked clean too 🤔 -- SE 728 subframe reasonability on 8/7 21:33 and some PID Alerts / Modes


[LIR 486122524](https://technetrmlsb.faa.gov/LIR/Details/486122524) - YYR WRE-A Rcvr reception intermittent faults. Requested WRS00010 (freq std 10 mhz) & WRS0005 (freq std AC power) be performed.

* Frequency Standard has been replaced 3 times in the last year
* 8/3 - 10 MHz Cable replaced; no change in behavior
* Requested WRS0010 (10 MHz scope meter check) and AC cable check; likely to replace freq std again
* Long-term recurring SE59 Rcvr reception faults




### MMX WRE-B - **OFFLINE**
Processor down; Freq Std also probably bad. Impossible to track down site technician to accomplish work; unclear if site tech has necessary experience if the old guy has retired...

Configured box waiting at Depot for further action... **Last attempt was 8/31/2021**.





## Upcoming Activities:

### 8/15 CM1 Replace Failed KPA
* See [LIR 489368624](https://technetrmlsb.faa.gov/LIR/Details/489368624) replacing bad KPA from 7/31 fault

### 9/12-9/30 LOA for GUS EIRP Update
* CM1, BR1, SZ1, and DX1
  * Travel to sites and adjust attenuation for AT2, AT3, AT4, and AT5
  * Perform Loopback Verification
* Need to coordinate with GUS sites, GEO contacts, and Operators
* **Submit LOA**

### 9/13-9/23 POCC Relocation
* Outside baseline equipment will be moved to equipment room


### 3/24/2023 CY23 Cutover


### MX Comm Upgrade 
* No ETA; Planning ongoing


## Bad Freq Stds Needing to be Returned
* BET


## Daily Notes:

### 20220812 Notes
* OTZ WRS Control Power OFF since 8/11 14:21
* YYR still showing elevated L1 Phase Noise - waiting for technician to replace Freq Std (double check with operators)




### 20220811 Notes
* YYR WRS went to No Data Reported briefly around 8/11 20:29; this is may be related to the geomagnetic storm activity (see [LIR 488390024](https://technetrmlsb.faa.gov/LIR/Details/488390024))
* OTZ WRS temperatures spiking just before morning brief - **protective shutdown until technician can get out to address the HVAC**
  * 8/11 - OTZ WRS Powered down until a site technician can address the HVAC issues (ref [LIR 488764124](https://technetrmlsb.faa.gov/LIR/Details/488764124))

* OTZ WRE-C seems to be more sensitive to the temperature changes than the other two; recommend reseating receiver cables -- if it is still overly sensitive during temperature spikes after that, the receiver should be replaced or run [WRS0014 Fault Iso](https://waas-engr.faa.gov/tib/current/Default.htm#Fault_Isolation_Procedures/WRS/WRS0014/1_intro.htm)



### 20220810 Notes
* Quiet night
* BRW WRS temperature spike at 8/10 06:45; no system impacts
* OTZ WRS still running a little hot
* YYR WRE-A allan voltage deviation seems to be degrading - **reiterate replacement of Freq Std needs to be performed** / EC recommends dropping YYR WRE-A to Maintenance due to WRE Bias Trips






### 20220809 Notes
* OTZ WRS protective shutdown overnight (8/9 02:35) due to temperature spike in the shelter - recommended restoring after 6-8 hours down, but did not happen...
* YYR WRE-A is still showing lots of phase noise, some spikes in allan voltage deviation (up to 1000), AGC is hairy on all bands, but not synchronous; mainly stable and tracking / **EC recommends replacement due to phase noise degradation**
* BET WRE-C is looking clean - no replacement needed apparently; BET will still need to hold on to the bad spare freq std until we release the STR for shipping hazmat

#### BET WRE-C - Monitor in Normal

* 8/9 - BET WRE-C is looking clean - no replacement needed apparently; BET will still need to hold on to the bad spare freq std until we release the STR for shipping hazmat
* 8/8 - BET WRE-C ran in Normal through the 8/6-8/8 weekend without any issues; some L5 phase noise on all threads on 8/8; allan voltage deviation seems to have leveled out

Allan voltage deviation ramps starting at 7/29 (seems to correspond to temperature fluxuations); Phase noise has been spiky for a while.

[LIR 296631732](https://technetrmlsb.faa.gov/LIR/Details/296631732) - BET WRE-C Freq Std exhibiting Alarm Code #1 Out-of-Tol Voltages. Spare Freq Std didn't work & ATSS to order new Freq Std.

* 8/4 - Replaced Freq Std, but spare was bad; ordered replacement freq std







### 20220808 Notes
* YYR WRE-A remained in Normal Mode through weekend; receiver tracked OK with some phase noise; allan voltage deviation looked clean too 🤔 -- SE 728 subframe reasonability on 8/7 21:33 and some PID Alerts / Modes
* OTZ WRS had **temperature spikes** over the weekend -- 8/7 6:33 - OTZ WRE-C had a SE 729 WRE Bias Error
  * 8/7 11:10 OTZ WRE-C Taken down to Maintenance
  * Per ticket [298739032](https://technetrmlsb.faa.gov/LIR/Details/298739032) "PERFORMED SE0729 (SOFT RESET), MAINTENANCE MODE UFN"
* Looks like BRW also had a temperature spike over the weekend around 8/6 22:30
* BET WRE-C ran in Normal through the 8/6-8/8 weekend without any issues; some L5 phase noise on all threads on 8/8; allan voltage deviation seems to have leveled out
* Mexico returning scope meter to Depot for calibration
* CDB Ring 2 has been down since 8/6; FTI has tested OK to ZAN





### 20220805 Notes
* AP1 Ring 1 PRI and Ring 2 ALT Lines cleared the loops; comm issues cleared for the site
* BET waiting for Freq Std (can they ship back the old freq std?)
* YYR waiting for further instructions... want to see the scope meter test results on the 10 MHz line before they remove freq std again
* YYR technician performed WRS0005 and WRS0010 tests on the Freq Std and said both "passed"... could be a problem with the receiver in port. **Pictures to be sent Monday.**
* **NOC Ring 1 losing RG1 packets every hour**
  * Due to serial port down on multilink for OEI router



