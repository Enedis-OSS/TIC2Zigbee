# Detailed Zigbee attributes and mapping for ERL Interface (Device ID 0x0509)

- [Detailed Zigbee attributes and mapping for ERL Interface (Device ID 0x0509)](#detailed-zigbee-attributes-and-mapping-for-erl-interface-device-id-0x0509)
  - [Introduction](#introduction)
  - [Basic 0x0000](#basic-0x0000)
    - [Attributes](#attributes)
      - [ZCLVersion 0x0000](#zclversion-0x0000)
      - [ApplicationVersion 0x0001](#applicationversion-0x0001)
      - [StackVersion 0x0002](#stackversion-0x0002)
      - [HWVersion 0x0003](#hwversion-0x0003)
      - [ManufacturerName 0x0004](#manufacturername-0x0004)
      - [ModelIdentifier 0x0005](#modelidentifier-0x0005)
      - [DateCode 0x0006](#datecode-0x0006)
      - [PowerSource 0x0007](#powersource-0x0007)
  - [Identify 0x0003](#identify-0x0003)
    - [Attributes](#attributes-1)
      - [IdentifyTime 0x0000](#identifytime-0x0000)
    - [Commands](#commands)
      - [IdentifyQueryResponse 0x00](#identifyqueryresponse-0x00)
      - [IdentifyQueryResponse 0x00](#identifyqueryresponse-0x00-1)
      - [Identify 0x00](#identify-0x00)
      - [Identify 0x00](#identify-0x00-1)
      - [IdentifyQuery 0x01](#identifyquery-0x01)
      - [IdentifyQuery 0x01](#identifyquery-0x01-1)
      - [TriggerEffect 0x40](#triggereffect-0x40)
      - [TriggerEffect 0x40](#triggereffect-0x40-1)
  - [Time 0x000A](#time-0x000a)
    - [Attributes](#attributes-2)
      - [Time 0x0000](#time-0x0000)
      - [TimeStatus 0x0001](#timestatus-0x0001)
      - [TimeZone 0x0002](#timezone-0x0002)
      - [DstStart 0x0003](#dststart-0x0003)
      - [DstEnd 0x0004](#dstend-0x0004)
      - [DstShift 0x0005](#dstshift-0x0005)
      - [StandardTime 0x0006](#standardtime-0x0006)
      - [LocalTime 0x0007](#localtime-0x0007)
      - [LastSetTime 0x0008](#lastsettime-0x0008)
      - [ValidUntilTime 0x0009](#validuntiltime-0x0009)
  - [OTA Upgrade 0x0019](#ota-upgrade-0x0019)
  - [Metering 0x0702](#metering-0x0702)
    - [Attributes](#attributes-3)
      - [CurrentSummationDelivered 0x0000](#currentsummationdelivered-0x0000)
      - [CurrentSummationReceived 0x0001](#currentsummationreceived-0x0001)
      - [ActiveRegisterTierDelivered 0x0020](#activeregistertierdelivered-0x0020)
      - [NumberofTiersInUse 0x0023](#numberoftiersinuse-0x0023)
      - [CurrentTier1SummationDelivered 0x0100](#currenttier1summationdelivered-0x0100)
      - [CurrentTier1SummationReceived 0x0101](#currenttier1summationreceived-0x0101)
      - [CurrentTier2SummationDelivered 0x0102](#currenttier2summationdelivered-0x0102)
      - [CurrentTier3SummationDelivered 0x0104](#currenttier3summationdelivered-0x0104)
      - [CurrentTier4SummationDelivered 0x0106](#currenttier4summationdelivered-0x0106)
      - [CurrentTier5SummationDelivered 0x0108](#currenttier5summationdelivered-0x0108)
      - [CurrentTier6SummationDelivered 0x010A](#currenttier6summationdelivered-0x010a)
      - [CurrentTier7SummationDelivered 0x010C](#currenttier7summationdelivered-0x010c)
      - [CurrentTier8SummationDelivered 0x010E](#currenttier8summationdelivered-0x010e)
      - [CurrentTier9SummationDelivered 0x0110](#currenttier9summationdelivered-0x0110)
      - [CurrentTier10SummationDelivered 0x0112](#currenttier10summationdelivered-0x0112)
      - [Status 0x0200](#status-0x0200)
      - [ExtendedStatus 0x0204](#extendedstatus-0x0204)
      - [CurrentMeterID 0x0206](#currentmeterid-0x0206)
      - [ServiceDisconnectReason 0x0208](#servicedisconnectreason-0x0208)
      - [LinkyModeOfOperation 0x0209](#linkymodeofoperation-0x0209)
      - [UnitofMeasure 0x0300](#unitofmeasure-0x0300)
      - [Multiplier 0x0301](#multiplier-0x0301)
      - [Divisor 0x0302](#divisor-0x0302)
      - [SummationFormatting 0x0303](#summationformatting-0x0303)
      - [DemandFormatting 0x0304](#demandformatting-0x0304)
      - [HistoricalConsumptionFormatting 0x0305](#historicalconsumptionformatting-0x0305)
      - [MeteringDeviceType 0x0306](#meteringdevicetype-0x0306)
      - [SiteID 0x0307](#siteid-0x0307)
      - [MeterSerialNumber 0x0308](#meterserialnumber-0x0308)
      - [ModuleSerialNumber 0x030E](#moduleserialnumber-0x030e)
      - [InstantaneousDemand  0x0400](#instantaneousdemand--0x0400)
      - [CurrentDayMaxDemandDelivered 0x045D](#currentdaymaxdemanddelivered-0x045d)
      - [CurrentDayMaxDemandDeliveredTime 0x045E](#currentdaymaxdemanddeliveredtime-0x045e)
      - [CurrentDayMaxDemandReceived 0x045F](#currentdaymaxdemandreceived-0x045f)
      - [CurrentDayMaxDemandReceivedTime 0x0460](#currentdaymaxdemandreceivedtime-0x0460)
      - [PreviousDayMaxDemandDelivered 0x0461](#previousdaymaxdemanddelivered-0x0461)
      - [PreviousDayMaxDemandDeliveredTime 0x0462](#previousdaymaxdemanddeliveredtime-0x0462)
      - [PreviousDayMaxDemandReceived 0x0463](#previousdaymaxdemandreceived-0x0463)
      - [PreviousDayMaxDemandReceivedTime 0x0464](#previousdaymaxdemandreceivedtime-0x0464)
      - [MaxNumberOfPeriodsDelivered 0x0500](#maxnumberofperiodsdelivered-0x0500)
      - [CurrentReactiveSummationQ1 0x0D05](#currentreactivesummationq1-0x0d05)
      - [CurrentReactiveSummationQ2 0x0D06](#currentreactivesummationq2-0x0d06)
      - [CurrentReactiveSummationQ3 0x0D07](#currentreactivesummationq3-0x0d07)
      - [CurrentReactiveSummationQ4 0x0D08](#currentreactivesummationq4-0x0d08)
    - [Commands](#commands-1)
      - [GetProfile 0x00](#getprofile-0x00)
        - [Parameters](#parameters)
          - [IntervalChannel](#intervalchannel)
          - [EndTime](#endtime)
          - [NumberOfPeriods](#numberofperiods)
      - [GetProfileResponse 0x00](#getprofileresponse-0x00)
        - [Parameters](#parameters-1)
          - [EndTime](#endtime-1)
          - [Status](#status)
          - [ProfileIntervalPeriod](#profileintervalperiod)
          - [NumberOfPeriodsDelivered](#numberofperiodsdelivered)
          - [Intervals](#intervals)
      - [PublishSnapshot 0x06](#publishsnapshot-0x06)
        - [Parameters](#parameters-2)
          - [SnapshotID](#snapshotid)
          - [SnapshotTime](#snapshottime)
          - [TotalSnapshotsFound](#totalsnapshotsfound)
          - [CommandIndex](#commandindex)
          - [TotalNumberOfCommands](#totalnumberofcommands)
          - [SnapshotCause](#snapshotcause)
          - [SnapshotPayloadType](#snapshotpayloadtype)
          - [SnapshotSub-Payload](#snapshotsub-payload)
      - [GetSnapshot 0x06](#getsnapshot-0x06)
        - [Parameters](#parameters-3)
          - [EarliestStartTime](#earlieststarttime)
          - [LatestEndTime](#latestendtime)
          - [SnapshotOffset](#snapshotoffset)
          - [SnapshotCause](#snapshotcause-1)
      - [GetSampledDataResponse 0x07](#getsampleddataresponse-0x07)
        - [Parameters](#parameters-4)
          - [SampleID](#sampleid)
          - [SampleStartTime](#samplestarttime)
          - [SampleType](#sampletype)
          - [SampleRequestInterval](#samplerequestinterval)
          - [NumberOfSamples](#numberofsamples)
          - [Samples](#samples)
      - [GetSampledData 0x08](#getsampleddata-0x08)
        - [Parameters](#parameters-5)
          - [SampleID](#sampleid-1)
          - [EarliestSampleTime](#earliestsampletime)
          - [SampleType](#sampletype-1)
          - [NumberOfSamples](#numberofsamples-1)
  - [Messaging 0x0703](#messaging-0x0703)
    - [Commands](#commands-2)
      - [DisplayMessage 0x00](#displaymessage-0x00)
        - [Parameters](#parameters-6)
          - [MessageID](#messageid)
          - [MessageControl](#messagecontrol)
          - [StartTime](#starttime)
          - [DurationInMinutes](#durationinminutes)
          - [Message](#message)
      - [GetLastMessage 0x00](#getlastmessage-0x00)
      - [CancelMessage 0x01](#cancelmessage-0x01)
        - [Parameters](#parameters-7)
          - [MessageID](#messageid-1)
      - [MessageConfirmation 0x01](#messageconfirmation-0x01)
        - [Parameters](#parameters-8)
          - [MessageID](#messageid-2)
          - [ConfirmationTime](#confirmationtime)
          - [MessageConfirmationControl](#messageconfirmationcontrol)
          - [MessageConfirmationResponse](#messageconfirmationresponse)
  - [Daily Schedule 0x070D](#daily-schedule-0x070d)
    - [Attributes](#attributes-4)
      - [AuxSwitch1Label 0x0000](#auxswitch1label-0x0000)
      - [AuxSwitch2Label 0x0001](#auxswitch2label-0x0001)
      - [AuxSwitch3Label 0x0002](#auxswitch3label-0x0002)
      - [AuxSwitch4Label 0x0003](#auxswitch4label-0x0003)
      - [AuxSwitch5Label 0x0004](#auxswitch5label-0x0004)
      - [AuxSwitch6Label 0x0005](#auxswitch6label-0x0005)
      - [AuxSwitch7Label 0x0006](#auxswitch7label-0x0006)
      - [AuxSwitch8Label 0x0007](#auxswitch8label-0x0007)
      - [CurrentAuxiliaryLoadSwitchState 0x0100](#currentauxiliaryloadswitchstate-0x0100)
      - [CurrentDeliveredTier 0x0101](#currentdeliveredtier-0x0101)
      - [CurrentTierLabel 0x0102](#currenttierlabel-0x0102)
      - [LinkyPeakPeriodStatus 0x0103](#linkypeakperiodstatus-0x0103)
      - [PeakStartTime  0x0104](#peakstarttime--0x0104)
      - [PeakEndTime  0x0105](#peakendtime--0x0105)
      - [CurrentTariffLabel 0x0106](#currenttarifflabel-0x0106)
    - [Commands](#commands-3)
      - [PublishSchedule 0x00](#publishschedule-0x00)
        - [Parameters](#parameters-9)
          - [ProviderID](#providerid)
          - [IssuerEventID](#issuereventid)
          - [ScheduleID](#scheduleid)
          - [DayID](#dayid)
          - [StartTime](#starttime-1)
          - [ScheduleType](#scheduletype)
          - [ScheduleTimeReference](#scheduletimereference)
          - [ScheduleName](#schedulename)
      - [GetSchedule 0x00](#getschedule-0x00)
        - [Parameters](#parameters-10)
          - [ProviderID](#providerid-1)
          - [EarliestStartTime](#earlieststarttime-1)
          - [MinIssuerEventID](#minissuereventid)
          - [NumberOfSchedules](#numberofschedules)
          - [ScheduleType](#scheduletype-1)
      - [PublishDayProfile 0x01](#publishdayprofile-0x01)
        - [Parameters](#parameters-11)
          - [ProviderID](#providerid-2)
          - [IssuerEventID](#issuereventid-1)
          - [DayID](#dayid-1)
          - [TotalNumberOfScheduleEntries](#totalnumberofscheduleentries)
          - [CommandIndex](#commandindex-1)
          - [TotalNumberOfCommands](#totalnumberofcommands-1)
          - [ScheduleType](#scheduletype-2)
          - [DayScheduleEntries](#dayscheduleentries)
      - [GetDayProfile 0x01](#getdayprofile-0x01)
        - [Parameters](#parameters-12)
          - [ProviderID](#providerid-3)
          - [DayID](#dayid-2)
      - [GetScheduleCancellation 0x05](#getschedulecancellation-0x05)
      - [CancelAllSchedules 0x06](#cancelallschedules-0x06)
  - [Meter Identification 0x0b01](#meter-identification-0x0b01)
    - [Attributes](#attributes-5)
      - [CompanyName 0x0000](#companyname-0x0000)
      - [MeterTypeID 0x0001](#metertypeid-0x0001)
      - [DataQualityID 0x0004](#dataqualityid-0x0004)
      - [Model  0x0006](#model--0x0006)
      - [POD 0x000C](#pod-0x000c)
      - [AvailablePower 0x000D](#availablepower-0x000d)
      - [PowerThreshold 0x000E](#powerthreshold-0x000e)
  - [Electrical Measurement 0x0b04](#electrical-measurement-0x0b04)
    - [Attributes](#attributes-6)
      - [MeasurementType 0x0000](#measurementtype-0x0000)
      - [TotalActivePower 0x0304](#totalactivepower-0x0304)
      - [TotalApparentPower 0x0306](#totalapparentpower-0x0306)
      - [PowerMultiplier 0x0402](#powermultiplier-0x0402)
      - [PowerDivisor 0x0403](#powerdivisor-0x0403)
      - [RMSVoltage 0x0505](#rmsvoltage-0x0505)
      - [RMSCurrent 0x0508](#rmscurrent-0x0508)
      - [ActivePower 0x050B](#activepower-0x050b)
      - [ApparentPower 0x050F](#apparentpower-0x050f)
      - [AverageRMSVoltageMeasurementPeriod 0x0511](#averagermsvoltagemeasurementperiod-0x0511)
      - [ACVoltageMultiplier 0x0600](#acvoltagemultiplier-0x0600)
      - [ACVoltageDivisor 0x0601](#acvoltagedivisor-0x0601)
      - [ACCurrentMultiplier 0x0602](#accurrentmultiplier-0x0602)
      - [ACCurrentDivisor 0x0603](#accurrentdivisor-0x0603)
      - [ACPowerMultiplier 0x0604](#acpowermultiplier-0x0604)
      - [ACPowerDivisor 0x0605](#acpowerdivisor-0x0605)
      - [RMSVoltagePhB 0x0905](#rmsvoltagephb-0x0905)
      - [RMSCurrentPhB 0x0908](#rmscurrentphb-0x0908)
      - [ActivePowerPhB 0x090B](#activepowerphb-0x090b)
      - [ApparentPowerPhB 0x090F](#apparentpowerphb-0x090f)
      - [AverageRMSVoltageMeasurementPeriodPhB 0x0911](#averagermsvoltagemeasurementperiodphb-0x0911)
      - [RMSVoltagePhC 0x0A05](#rmsvoltagephc-0x0a05)
      - [RMSCurrentPhC 0x0A08](#rmscurrentphc-0x0a08)
      - [ActivePowerPhC 0x0A0B](#activepowerphc-0x0a0b)
      - [ApparentPowerPhC 0x0A0F](#apparentpowerphc-0x0a0f)
      - [AverageRMSVoltageMeasurementPeriodPhC 0x0A11](#averagermsvoltagemeasurementperiodphc-0x0a11)
  - [Diagnostic 0x0b05](#diagnostic-0x0b05)
    - [Attributes](#attributes-7)
      - [NumberOfResets 0x0000](#numberofresets-0x0000)
      - [LastMessageLQI 0x011C](#lastmessagelqi-0x011c)
      - [LastMessageRSSI 0x011D](#lastmessagerssi-0x011d)
  - [Global attributes](#global-attributes)
    - [Attributes](#attributes-8)
      - [ClusterRevision 0xFFFD](#clusterrevision-0xfffd)


## Introduction

This note lists the Zigbee clusters and their attributes and commands used to implement an ERL interface.

It also explains the mapping between TIC Fields and Zigbee attributes and commands of the ERL interface (Device ID 0x0509).

This data mapping is not mandatory but a recommendation from Enedis.

First, here are the clusters to be supported by any ERL interface:

| **Server Side**                     | **Client Side**                |
|-------------------------------------|--------------------------------|
| **Mandatory**                       |                                |
| Basic (0x0000)                      |                                |
| Identify (0x0003)                   | Identify (0x0003)              |
| Time (0x000A)                       | Time (0x000A)                  |
| Metering (0x0702)                   |                                |
| Messaging (0x0703)                  |                                |
| Meter Identification (0x0B01)       |                                |
| Electrical Measurement (0x0B04)     |                                |
| Diagnostics (0x0B05)                |                                |
| Daily Schedule (0x070D)             |                                |
| **Recommended optional**            |                                |
|                                     | OTA Upgrade (0x0019)           |

<div style="page-break-after: always;"></div>












##  Basic 0x0000
This cluster provides attributes for determining basic general information.

* Mandatory / Optional: M

* Client / Server: ( S )



| **Identifier** | **Name**           | **Type**               | **Range**    | **Access** | **Reportable** |
|----------------|--------------------|------------------------|--------------|------------|----------------|
| 0x0000         | ZCLVersion         | Unsigned 8-bit integer | [0x00, 0xFF] | Read Only  | No             |
| 0x0001         | ApplicationVersion | Unsigned 8-bit integer | [0x00, 0xFF] | Read Only  | No             |
| 0x0002         | StackVersion       | Unsigned 8-bit integer | [0x00, 0xFF] | Read Only  | No             |
| 0x0003         | HWVersion          | Unsigned 8-bit integer | [0x00, 0xFF] | Read Only  | No             |
| 0x0004         | ManufacturerName   | String                 | {0, 32}      | Read Only  | No             |
| 0x0005         | ModelIdentifier    | String                 | {0, 32}      | Read Only  | No             |
| 0x0006         | DateCode           | String                 | {0, 16}      | Read Only  | No             |
| 0x0007         | PowerSource        | 8-bit Enumeration      | [0x00, 0xFF] | Read Only  | No             |


### Attributes

#### ZCLVersion 0x0000
Attribute of cluster 0x0000 Basic:

* Type: Unsigned 8-bit integer
* Range: [0x00, 0xFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: ZCL version

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | ZCL version     | ZCL version    |
| **STD Prod**  | ZCL version     | ZCL version    |
| **HST**       | ZCL version     | ZCL version    |


----------------------





#### ApplicationVersion 0x0001
Attribute of cluster 0x0000 Basic:

* Type: Unsigned 8-bit integer
* Range: [0x00, 0xFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x00

**Values:**

| **TIC mode**  | **Singlephase**       | **Threephase**        |
|---------------|-----------------------|-----------------------|
| **STD Conso** | Manufacturer Specific | Manufacturer Specific |
| **STD Prod**  | Manufacturer Specific | Manufacturer Specific |
| **HST**       | Manufacturer Specific | Manufacturer Specific |


**Comment:**
Manufacturer Specific.

----------------------





#### StackVersion 0x0002
Attribute of cluster 0x0000 Basic:

* Type: Unsigned 8-bit integer
* Range: [0x00, 0xFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x00

**Values:**

| **TIC mode**  | **Singlephase**                    | **Threephase**                     |
|---------------|------------------------------------|------------------------------------|
| **STD Conso** | Zigbee stack manufacturer specific | Zigbee stack manufacturer specific |
| **STD Prod**  | Zigbee stack manufacturer specific | Zigbee stack manufacturer specific |
| **HST**       | Zigbee stack manufacturer specific | Zigbee stack manufacturer specific |


**Comment:**
Zigbee stack manufacturer specific.

----------------------





#### HWVersion 0x0003
Attribute of cluster 0x0000 Basic:

* Type: Unsigned 8-bit integer
* Range: [0x00, 0xFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x00

**Values:**

| **TIC mode**  | **Singlephase**       | **Threephase**        |
|---------------|-----------------------|-----------------------|
| **STD Conso** | Manufacturer specific | Manufacturer specific |
| **STD Prod**  | Manufacturer specific | Manufacturer specific |
| **HST**       | Manufacturer specific | Manufacturer specific |


**Comment:**
Manufacturer specific.

----------------------





#### ManufacturerName 0x0004
Attribute of cluster 0x0000 Basic:

* Type: String
* Range: {0, 32}
* Access: Read Only
* Reportable: No
* Default value / Reset value: Empty string

**Values:**

| **TIC mode**  | **Singlephase**       | **Threephase**        |
|---------------|-----------------------|-----------------------|
| **STD Conso** | Manufacturer specific | Manufacturer specific |
| **STD Prod**  | Manufacturer specific | Manufacturer specific |
| **HST**       | Manufacturer specific | Manufacturer specific |


**Comment:**
Manufacturer specific.

----------------------





#### ModelIdentifier 0x0005
Attribute of cluster 0x0000 Basic:

* Type: String
* Range: {0, 32}
* Access: Read Only
* Reportable: No
* Default value / Reset value: Empty string

**Values:**

| **TIC mode**  | **Singlephase**       | **Threephase**        |
|---------------|-----------------------|-----------------------|
| **STD Conso** | Manufacturer specific | Manufacturer specific |
| **STD Prod**  | Manufacturer specific | Manufacturer specific |
| **HST**       | Manufacturer specific | Manufacturer specific |


**Comment:**
Manufacturer specific.

----------------------





#### DateCode 0x0006
Attribute of cluster 0x0000 Basic:

* Type: String
* Range: {0, 16}
* Access: Read Only
* Reportable: No
* Default value / Reset value: Empty string

**Values:**

| **TIC mode**  | **Singlephase**                                          | **Threephase**                                           |
|---------------|----------------------------------------------------------|----------------------------------------------------------|
| **STD Conso** | 8 first bytes ISO8601 / last bytes Manufacturer specific | 8 first bytes ISO8601 / last bytes Manufacturer specific |
| **STD Prod**  | 8 first bytes ISO8601 / last bytes Manufacturer specific | 8 first bytes ISO8601 / last bytes Manufacturer specific |
| **HST**       | 8 first bytes ISO8601 / last bytes Manufacturer specific | 8 first bytes ISO8601 / last bytes Manufacturer specific |


**Comment:**
8 first bytes ISO8601 / last bytes Manufacturer specific.

----------------------





#### PowerSource 0x0007
Attribute of cluster 0x0000 Basic:

* Type: 8-bit Enumeration
* Range: [0x00, 0xFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x00

**Values:**

| **TIC mode**  | **Singlephase**                                              | **Threephase** |
|---------------|--------------------------------------------------------------|----------------|
| **STD Conso** | 0x00 (means "Unknown" see for specification table Table 3-8. Values of the PowerSource Attribute in ZCL specification) | 0x00 (Unknown) |
| **STD Prod**  | 0x00 (Unknown)                                               | 0x00 (Unknown) |
| **HST**       | 0x00 (Unknown)                                               | 0x00 (Unknown) |


**Comment:**
Specify the power source of the equipment.

----------------------




<div style="page-break-after: always;"></div>












##  Identify 0x0003
Attributes and commands to put a device into an Identification mode (e.g., flashing a light), that indicates to an observer which of several devices it is, also to request any device that is identifying itself to respond to the initiator. Note that this cluster cannot be disabled.


Notice:

As the ERL shall support EZ-Mode, according to the Dotdot Architecture 14-0240 specification, the Identify cluster must be both Client and Server.

* Mandatory / Optional: M

* Client / Server: ( C&S )



| **Identifier** | **Name**     | **Type**                | **Range**        | **Access** | **Reportable** |
|----------------|--------------|-------------------------|------------------|------------|----------------|
| 0x0000         | IdentifyTime | Unsigned 16-bit integer | [0x0000, 0xFFFF] | Read Write | No             |


### Attributes

#### IdentifyTime 0x0000
Attribute of cluster 0x0003 Identify:

* Type: Unsigned 16-bit integer
* Range: [0x0000, 0xFFFF]
* Access: Read Write
* Reportable: No
* Default value / Reset value: 0x0000

**Values:**

| **TIC mode**  | **Singlephase**       | **Threephase**        |
|---------------|-----------------------|-----------------------|
| **STD Conso** | Manufacturer Specific | Manufacturer Specific |
| **STD Prod**  | Manufacturer Specific | Manufacturer Specific |
| **HST**       | Manufacturer Specific | Manufacturer Specific |


**Comment:**
Time leaving for equipment to identify.

----------------------




### Commands

#### IdentifyQueryResponse 0x00
Command:

* Client / Server: Server - Generated

**Comment:**
Command send by ERL interface in response of a "Identify Query" command received in the case that the ERL Interface  is currently identifying itself.



#### IdentifyQueryResponse 0x00
Command:

* Client / Server: Client - Received

**Comment:**
Command received by ERL interface in response of a "Identify Query" command send.


#### Identify 0x00
Command:

* Client / Server: Client - Generated

**Comment:**
Command send by the ERL Interface to ask other equipments to identify themselves.


#### Identify 0x00
Command:

* Client / Server: Server - Received

**Comment:**
Command received asking for ERL interface to identify.


#### IdentifyQuery 0x01
Command:

* Client / Server: Client - Generated

**Comment:**
Command send by the ERL Interface to ask other equipments (target or targets) to respond if they are currently identifying themselves.



#### IdentifyQuery 0x01
Command:

* Client / Server: Server - Received

**Comment:**
Command received asking for ERL interface if it is currently identifying itself.



#### TriggerEffect 0x40
Command:

* Client / Server: Server - Received

**Comment:**
On receipt of this command, the ERL Interface SHALL execute the trigger effect indicated in the Effect Identifier and Effect Variant fields.


#### TriggerEffect 0x40
Command:

* Client / Server: Client - Generated


<div style="page-break-after: always;"></div>












##  Time 0x000A
This cluster provides a basic interface to a real-time clock. The clock time MAY be read and also written, in order to synchronize the clock (as close as practical) to a time standard. This time standard is the number of seconds since 0 hrs 0 mins 0 sec on 1st January 2000 UTC (Universal Coordinated Time).


The cluster also includes basic functionality for local time zone and daylight saving time (DST).


Nota: the TIC time is local time, whereas Zigbee time is UTC. Local time should be converted to UTC with the formulae given for France (mainland).

* Mandatory / Optional: M

* Client / Server: ( C&S )



| **Identifier** | **Name**       | **Type**                | **Range**                | **Access** | **Reportable** |
|----------------|----------------|-------------------------|--------------------------|------------|----------------|
| 0x0000         | Time           | UTCTime                 | [0x00000000, 0xFFFFFFFF] | Read Write | No             |
| 0x0001         | TimeStatus     | 8-bit BitMap            | 0b0000xxxx               | Read Write | Yes            |
| 0x0002         | TimeZone       | Signed 32-bit integer   | [-86400, 86400]          | Read Write | No             |
| 0x0003         | DstStart       | Unsigned 32-bit integer | [0x00000000, 0xFFFFFFFF] | Read Write | No             |
| 0x0004         | DstEnd         | Unsigned 32-bit integer | [0x00000000, 0xFFFFFFFF] | Read Write | No             |
| 0x0005         | DstShift       | Signed 32-bit integer   | [-86400, 86400]          | Read Write | No             |
| 0x0006         | StandardTime   | Unsigned 32-bit integer | [0x00000000, 0xFFFFFFFF] | Read Only  | No             |
| 0x0007         | LocalTime      | Unsigned 32-bit integer | [0x00000000, 0xFFFFFFFF] | Read Only  | No             |
| 0x0008         | LastSetTime    | UTCTime                 | [0x00000000, 0xFFFFFFFF] | Read Only  | No             |
| 0x0009         | ValidUntilTime | UTCTime                 | [0x00000000, 0xFFFFFFFF] | Read Write | No             |


### Attributes

#### Time 0x0000
Attribute of cluster 0x000A Time:

* Type: UTCTime
* Range: [0x00000000, 0xFFFFFFFF]
* Access: Read Write
* Reportable: No
* Default value / Reset value: 0xffffffff

**Values:**

| **TIC mode**  | **Singlephase**          | **Threephase**           |
|---------------|--------------------------|--------------------------|
| **STD Conso** | StandardTime - TimeZone  | StandardTime - TimeZone  |
| **STD Prod**  | StandardTime - TimeZone  | StandardTime - TimeZone  |
| **HST**       | 0xffffffff (see comment) | 0xffffffff (see comment) |


**Comment:**
Number of seconds since 0 hrs 0 mins 0 sec on 1st January 2000 UTC (Universal Coordinated Time).



In STD Mode, calculated like described in corresponding column. Time Server cluster is used.


In HST TIC Mode, Time is not present. In HST TIC Mode:  

- If a Time Server is available in the Zigbee network, ERL Interface Internal Clock (RTC) can be configured by this Time Server. In this case, the Time Client cluster is used. The Time Client cluster may be replaced by the Timer Server cluster if an out of band device with a Time Server using a higher level of trust is added.

-  If an out of band device (when an other interface in an ERL Device is available, ie: BLE) sets and synchronizes the internal ERL clock (Internal clock is set and synchronized out of band), the ERL interface can provide timestamp. Time Server is used.

-  If no Time Server is present in the Zigbee network or/and out of band, ERL interface can’t provide timestamps and can not use commands which need time (ie : daily schedule cluster). 

----------------------





#### TimeStatus 0x0001
Attribute of cluster 0x000A Time:

* Type: 8-bit BitMap
* Range: 0b0000xxxx
* Access: Read Write
* Reportable: Yes
* Default value / Reset value: 0b00000000

**Values:**

| **TIC mode**  | **Singlephase**                                              | **Threephase**                                               |
|---------------|--------------------------------------------------------------|--------------------------------------------------------------|
| **STD Conso** | * 0b00000101 if STGE bit 16 == 0<br />* 0b00000010 if STGE bit 16 == 1 and time is able to be synchronized by the Zigbee network or out of band (for instance BLE)<br />* 0b00000000 in other cases | * 0b00000101 if STGE bit 16 == 0<br />* 0b00000010 if STGE bit 16 == 1 and time is able to be synchronized by the Zigbee network or out of band (for instance BLE)<br />* 0b00000000 in other cases |
| **STD Prod**  | * 0b00000101 if STGE bit 16 == 0<br />* 0b00000010 if STGE bit 16 == 1 and time is able to be synchronized by the Zigbee network or out of band (for instance BLE)<br />* 0b00000000 in other cases | * 0b00000101 if STGE bit 16 == 0<br />* 0b00000010 if STGE bit 16 == 1 and time is able to be synchronized by the Zigbee network or out of band (for instance BLE)<br />* 0b00000000 in other cases |
| **HST**       | * 0b00000010 if time is able to be synchronized by the Zigbee network or out of band (for instance BLE)<br />* 0b00000000 in other cases | * 0b00000010 if time is able to be synchronized by the Zigbee network or out of band (for instance BLE)<br />* 0b00000000 in other cases |


**Comment:**
Only bits 0 to 3 used, true or false flags:
* bit 0 : Master
* bit 1 : Synchronized
* bit 2 : MasterZoneDst
* bit 3 : Superseding

----------------------





#### TimeZone 0x0002
Attribute of cluster 0x000A Time:

* Type: Signed 32-bit integer
* Range: [-86400, 86400]
* Access: Read Write
* Reportable: No
* Default value / Reset value: 0x00000000

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | 3600            | 3600           |
| **STD Prod**  | 3600            | 3600           |
| **HST**       | Default value   | Default value  |


**Comment:**
Local meridian shift (in seconds) compared to Greenwich meridian.

1h = 3600s for Paris meridian, shall be modified for other UTC zones.

----------------------





#### DstStart 0x0003
Attribute of cluster 0x000A Time:

* Type: Unsigned 32-bit integer
* Range: [0x00000000, 0xFFFFFFFF]
* Access: Read Write
* Reportable: No
* Default value / Reset value: 0xFFFFFFFF

**Values:**

| **TIC mode**  | **Singlephase**                            | **Threephase**                             |
|---------------|--------------------------------------------|--------------------------------------------|
| **STD Conso** | Last Sunday of March in UTC (see comments) | Last Sunday of March in UTC (see comments) |
| **STD Prod**  | Last Sunday of March in UTC (see comments) | Last Sunday of March in UTC (see comments) |
| **HST**       | Default value                              | Default value                              |


**Comment:**
DstStart and DstEnd calculation:

The Linky meter does not provide DstStart and DstEnd before the d-day. 

But it is possible to calculate it from the current time. In central Europe these dates are:
* The last Sunday of March at 2 AM,
* the last Sunday of October at 3 AM.


The following function can be used: 

Last Sunday=31-(int((2,6*(m-2))-0,19)+31+aa+int(aa/4)+int(Century/4)-(2*Century))%7


With:  
* AAAA = current year	
* Century = int(AAAA/100)	
* aa = AAAA-(Century*100)
* m = 3 for DstStart and m=10 for DstEnd


The result must be converted in UTC before being written in the DstStart and DstEnd attributes. 

This calculation must be done when the ERL starts right after reading a Standard Tic frame, or right after an external time server gives date/time information, or when the year changes.

----------------------





#### DstEnd 0x0004
Attribute of cluster 0x000A Time:

* Type: Unsigned 32-bit integer
* Range: [0x00000000, 0xFFFFFFFF]
* Access: Read Write
* Reportable: No
* Default value / Reset value: 0xFFFFFFFF

**Values:**

| **TIC mode**  | **Singlephase**                              | **Threephase**                               |
|---------------|----------------------------------------------|----------------------------------------------|
| **STD Conso** | Last Sunday of October in UTC (see comments) | Last Sunday of October in UTC (see comments) |
| **STD Prod**  | Last Sunday of October in UTC (see comments) | Last Sunday of October in UTC (see comments) |
| **HST**       | Default value                                | Default value                                |


**Comment:**
DstStart and DstEnd calculation:

The Linky meter does not provide DstStart and DstEnd before the d-day. 

But it is possible to calculate it from the current time. In central Europe these dates are:
* The last Sunday of March at 2 AM,
* the last Sunday of October at 3 AM.


The following function can be used: 

Last Sunday=31-(int((2,6*(m-2))-0,19)+31+aa+int(aa/4)+int(Century/4)-(2*Century))%7


With:  
* AAAA = current year	
* Century = int(AAAA/100)	
* aa = AAAA-(Century*100)
* m = 3 for DstStart and m=10 for DstEnd


The result must be converted in UTC before being written in the DstStart and DstEnd attributes. 

This calculation must be done when the ERL starts right after reading a Standard Tic frame, or right after an external time server gives date/time information, or when the year changes.

----------------------





#### DstShift 0x0005
Attribute of cluster 0x000A Time:

* Type: Signed 32-bit integer
* Range: [-86400, 86400]
* Access: Read Write
* Reportable: No
* Default value / Reset value: 0x00000000

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | 3600            | 3600           |
| **STD Prod**  | 3600            | 3600           |
| **HST**       | Default value   | Default value  |


**Comment:**
Corresponds to DST shift (in seconds) for France to add between DstStart and DstEnd. Can be 0 if no more UE DST shift in the future.


In case the DST shift is not applicable anymore in the UE, ERL interface should detect that the letter "e" doesn’t switch to "h". In this case ERL should apply 0 to DstShift. For DstStart and DstEnd they should be set to 0xFFFFFFFF.

----------------------





#### StandardTime 0x0006
Attribute of cluster 0x000A Time:

* Type: Unsigned 32-bit integer
* Range: [0x00000000, 0xFFFFFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0xFFFFFFFF

**Values:**

| **TIC mode**  | **Singlephase**                                              | **Threephase**                                               |
|---------------|--------------------------------------------------------------|--------------------------------------------------------------|
| **STD Conso** | * LocalTime - DstShift if DATE[0] == ‘E’ or  DATE[0] == ‘e’<br />* LocalTime if DATE[0] == ‘H’ or  DATE[0] == ‘h’ | * LocalTime - DstShift if DATE[0] == ‘E’ or  DATE[0] == ‘e’<br />* LocalTime if DATE[0] == ‘H’ or  DATE[0] == ‘h’ |
| **STD Prod**  | * LocalTime - DstShift if DATE[0] == ‘E’ or  DATE[0] == ‘e’<br />* LocalTime if DATE[0] == ‘H’ or  DATE[0] == ‘h’ | * LocalTime - DstShift if DATE[0] == ‘E’ or  DATE[0] == ‘e’<br />* LocalTime if DATE[0] == ‘H’ or  DATE[0] == ‘h’ |
| **HST**       | 0xFFFFFFFF                                                   | 0xFFFFFFFF                                                   |


**Comment:**
Timestamp of Standard Time in seconds since 01/01/2000.


In STD Mode, calculated like described in corresponding column. Time Server cluster is used.


In HST TIC Mode, Time is not present. In HST TIC Mode:  
- If a Time Server is available in the Zigbee network, ERL Interface Internal Clock (RTC) can be configured by this Time Server. In this case, the Time Client cluster is used. The Time Client cluster may be replaced by the Timer Server cluster if an out of band device with a Time Server using a higher level of trust is added.

-  If an out of band device (when an other interface in an ERL Device is available, ie: BLE) sets and synchronizes the internal ERL clock (Internal clock is set and synchronized out of band), the ERL interface can provide timestamp. Time Server is used.

-  If no Time Server is present in the Zigbee or/and in out of band, ERL interface can’t provide timestamps and can not use commands which need time (ie : daily schedule cluster). 

----------------------





#### LocalTime 0x0007
Attribute of cluster 0x000A Time:

* Type: Unsigned 32-bit integer
* Range: [0x00000000, 0xFFFFFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0xFFFFFFFF

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | DATE            | DATE           |
| **STD Prod**  | DATE            | DATE           |
| **HST**       | 0xFFFFFFFF      | 0xFFFFFFFF     |


**Comment:**
Timestamp of Local Time in seconds since 01/01/2000 - Shall convert DATE string field without first byte to timestamp.


In STD Mode, calculated like described in corresponding column. Time Server cluster is used.


In HST TIC Mode, Time is not present. In HST TIC Mode:  
- If a Time Server is available in the Zigbee network, ERL Interface Internal Clock can be configured by this Time Server. In this case, the Time Client cluster is used. The Time Client cluster may be replaced by the Timer Server cluster if an out of band device with a Time Server using a higher level of trust is added.

-  If an out of band device (when an other interface in an ERL Device is available, ie: BLE) sets and synchronizes the internal ERL clock (Internal clock is set and synchronized out of band), the ERL interface can provide timestamp. Time Server is used.

-  If no Time Server is present in the Zigbee or/and in out of band, ERL interface can’t provide timestamps and can not use commands which need time synchronisation (ie : daily schedule cluster Commands).

----------------------





#### LastSetTime 0x0008
Attribute of cluster 0x000A Time:

* Type: UTCTime
* Range: [0x00000000, 0xFFFFFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0xFFFFFFFF

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | Time            | Time           |
| **STD Prod**  | Time            | Time           |
| **HST**       | Default value   | Default value  |


**Comment:**
Set to Time each time an uncorrupted TIC frame is received by ERL interface.

----------------------





#### ValidUntilTime 0x0009
Attribute of cluster 0x000A Time:

* Type: UTCTime
* Range: [0x00000000, 0xFFFFFFFF]
* Access: Read Write
* Reportable: No
* Default value / Reset value: 0xFFFFFFFF

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | Time + 86400    | Time + 86400   |
| **STD Prod**  | Time + 86400    | Time + 86400   |
| **HST**       | Default value   | Default value  |


**Comment:**
The validity time is extended by 24h each time an uncorrupted TIC frame is received by the ERL interface.

----------------------




<div style="page-break-after: always;"></div>












##  OTA Upgrade 0x0019
Parameters and commands for upgrading image on devices Over-The-Air.


See last version of Zigbee Cluster Library for details.

* Mandatory / Optional: O

* Client / Server: ( C )



<div style="page-break-after: always;"></div>












##  Metering 0x0702
The Metering Cluster provides a mechanism to retrieve usage information from Electric devices.

The Metering Cluster is designed to provide flexibility while limiting capabilities to a set number of metered information types.

Provides in particular differents tiers (cumulative energy) for consumption and production.

* Mandatory / Optional: M

* Client / Server: ( S )



| **Identifier** | **Name**                          | **Type**                | **Range**                                 | **Access** | **Reportable** |
|----------------|-----------------------------------|-------------------------|-------------------------------------------|------------|----------------|
| 0x0000         | CurrentSummationDelivered         | Unsigned 48-bit integer | [0x000000000000, 0xFFFFFFFFFFFF]          | Read Only  | No             |
| 0x0001         | CurrentSummationReceived          | Unsigned 48-bit integer | [0x000000000000, 0xFFFFFFFFFFFF]          | Read Only  | No             |
| 0x0020         | ActiveRegisterTierDelivered       | 8-bit Enumeration       | {0, 48}                                   | Read Only  | Yes            |
| 0x0023         | NumberofTiersInUse                | Unsigned 8-bit integer  | {0, 48}                                   | Read Only  | Yes            |
| 0x0100         | CurrentTier1SummationDelivered    | Unsigned 48-bit integer | [0x000000000000, 0xFFFFFFFFFFFF]          | Read Only  | No             |
| 0x0101         | CurrentTier1SummationReceived     | Unsigned 48-bit integer | [0x000000000000, 0xFFFFFFFFFFFF]          | Read Only  | No             |
| 0x0102         | CurrentTier2SummationDelivered    | Unsigned 48-bit integer | [0x000000000000, 0xFFFFFFFFFFFF]          | Read Only  | No             |
| 0x0104         | CurrentTier3SummationDelivered    | Unsigned 48-bit integer | [0x000000000000, 0xFFFFFFFFFFFF]          | Read Only  | No             |
| 0x0106         | CurrentTier4SummationDelivered    | Unsigned 48-bit integer | [0x000000000000, 0xFFFFFFFFFFFF]          | Read Only  | No             |
| 0x0108         | CurrentTier5SummationDelivered    | Unsigned 48-bit integer | [0x000000000000, 0xFFFFFFFFFFFF]          | Read Only  | No             |
| 0x010A         | CurrentTier6SummationDelivered    | Unsigned 48-bit integer | [0x000000000000, 0xFFFFFFFFFFFF]          | Read Only  | No             |
| 0x010C         | CurrentTier7SummationDelivered    | Unsigned 48-bit integer | [0x000000000000, 0xFFFFFFFFFFFF]          | Read Only  | No             |
| 0x010E         | CurrentTier8SummationDelivered    | Unsigned 48-bit integer | [0x000000000000, 0xFFFFFFFFFFFF]          | Read Only  | No             |
| 0x0110         | CurrentTier9SummationDelivered    | Unsigned 48-bit integer | [0x000000000000, 0xFFFFFFFFFFFF]          | Read Only  | No             |
| 0x0112         | CurrentTier10SummationDelivered   | Unsigned 48-bit integer | [0x000000000000, 0xFFFFFFFFFFFF]          | Read Only  | No             |
| 0x0200         | Status                            | 8-bit BitMap            | [0x00, 0xFF]                              | Read Only  | Yes            |
| 0x0204         | ExtendedStatus                    | 64-bit BitMap           | [0x0000000000000000,  0xFFFFFFFFFFFFFFFF] | Read Only  | Yes            |
| 0x0206         | CurrentMeterID                    | Octet String            | {0, 6}                                    | Read Only  | Yes            |
| 0x0208         | ServiceDisconnectReason           | 8-bit Enumeration       | [0x00, 0xFF]                              | Read Only  | No             |
| 0x0209         | LinkyModeOfOperation              | 8-bit BitMap            | [0x00, 0xFF]                              | Read Only  | Yes            |
| 0x0300         | UnitofMeasure                     | 8-bit Enumeration       | [0x00, 0xFF]                              | Read Only  | No             |
| 0x0301         | Multiplier                        | Unsigned 24-bit integer | [0x000000, 0xFFFFFF]                      | Read Only  | No             |
| 0x0302         | Divisor                           | Unsigned 24-bit integer | [0x000000, 0xFFFFFF]                      | Read Only  | No             |
| 0x0303         | SummationFormatting               | 8-bit BitMap            | [0x00, 0xFF]                              | Read Only  | No             |
| 0x0304         | DemandFormatting                  | 8-bit BitMap            | [0x00, 0xFF]                              | Read Only  | No             |
| 0x0305         | HistoricalConsumptionFormatting   | 8-bit BitMap            | [0x00, 0xFF]                              | Read Only  | No             |
| 0x0306         | MeteringDeviceType                | 8-bit BitMap            | [0x00, 0xFF]                              | Read Only  | No             |
| 0x0307         | SiteID                            | Octet String            | {0, 33}                                   | Read Only  | Yes            |
| 0x0308         | MeterSerialNumber                 | Octet String            | {0, 25}                                   | Read Only  | Yes            |
| 0x030E         | ModuleSerialNumber                | Octet String            | {0, 25}                                   | Read Only  | No             |
| 0x0400         | InstantaneousDemand               | Signed 24-bit integer   | [-8388607, 8388607]                       | Read Only  | No             |
| 0x045D         | CurrentDayMaxDemandDelivered      | Unsigned 48-bit integer | [0x000000000000, 0xFFFFFFFFFFFF]          | Read Only  | No             |
| 0x045E         | CurrentDayMaxDemandDeliveredTime  | UTCTime                 | [0x00000000, 0xFFFFFFFF]                  | Read Only  | No             |
| 0x045F         | CurrentDayMaxDemandReceived       | Unsigned 48-bit integer | [0x000000000000, 0xFFFFFFFFFFFF]          | Read Only  | No             |
| 0x0460         | CurrentDayMaxDemandReceivedTime   | UTCTime                 | [0x00000000, 0xFFFFFFFF]                  | Read Only  | No             |
| 0x0461         | PreviousDayMaxDemandDelivered     | Unsigned 48-bit integer | [0x000000000000, 0xFFFFFFFFFFFF]          | Read Only  | No             |
| 0x0462         | PreviousDayMaxDemandDeliveredTime | UTCTime                 | [0x00000000, 0xFFFFFFFF]                  | Read Only  | No             |
| 0x0463         | PreviousDayMaxDemandReceived      | Unsigned 48-bit integer | [0x000000000000, 0xFFFFFFFFFFFF]          | Read Only  | No             |
| 0x0464         | PreviousDayMaxDemandReceivedTime  | UTCTime                 | [0x00000000, 0xFFFFFFFF]                  | Read Only  | No             |
| 0x0500         | MaxNumberOfPeriodsDelivered       | Unsigned 8-bit integer  | [0x00, 0xFF]                              | Read Only  | No             |
| 0x0D05         | CurrentReactiveSummationQ1        | Unsigned 48-bit integer | [0x000000000000, 0xFFFFFFFFFFFF]          | Read Only  | No             |
| 0x0D06         | CurrentReactiveSummationQ2        | Unsigned 48-bit integer | [0x000000000000, 0xFFFFFFFFFFFF]          | Read Only  | No             |
| 0x0D07         | CurrentReactiveSummationQ3        | Unsigned 48-bit integer | [0x000000000000, 0xFFFFFFFFFFFF]          | Read Only  | No             |
| 0x0D08         | CurrentReactiveSummationQ4        | Unsigned 48-bit integer | [0x000000000000, 0xFFFFFFFFFFFF]          | Read Only  | No             |


### Attributes

#### CurrentSummationDelivered 0x0000
Attribute of cluster 0x0702 Metering:

* Type: Unsigned 48-bit integer
* Range: [0x000000000000, 0xFFFFFFFFFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x000000000000

**Values:**

| **TIC mode**  | **Singlephase**                                              | **Threephase**                                               |
|---------------|--------------------------------------------------------------|--------------------------------------------------------------|
| **STD Conso** | EAST                                                         | EAST                                                         |
| **STD Prod**  | EAST                                                         | EAST                                                         |
| **HST**       | * CurrentTier1SummationDelivered if OPTARIF == "BASE"<br />* CurrentTier1SummationDelivered + CurrentTier2SummationDelivered if OPTARIF == "HC.." or "EJP."<br />* CurrentTier1SummationDelivered + CurrentTier2SummationDelivered + CurrentTier3SummationDelivered  + CurrentTier4SummationDelivered  + CurrentTier5SummationDelivered  + CurrentTier6SummationDelivered if OPTARIF[0-2] == "BBR" | * CurrentTier1SummationDelivered if OPTARIF == "BASE"<br />* CurrentTier1SummationDelivered + CurrentTier2SummationDelivered if OPTARIF == "HC.." or "EJP."<br />* CurrentTier1SummationDelivered + CurrentTier2SummationDelivered + CurrentTier3SummationDelivered  + CurrentTier4SummationDelivered  + CurrentTier5SummationDelivered  + CurrentTier6SummationDelivered if OPTARIF[0-2] == "BBR" |


**Comment:**
Total consumed energy in Wh.

----------------------





#### CurrentSummationReceived 0x0001
Attribute of cluster 0x0702 Metering:

* Type: Unsigned 48-bit integer
* Range: [0x000000000000, 0xFFFFFFFFFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x000000000000

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | Default value   | Default value  |
| **STD Prod**  | EAIT            | EAIT           |
| **HST**       | Default value   | Default value  |


**Comment:**
Total produced energy in Wh.

----------------------





#### ActiveRegisterTierDelivered 0x0020
Attribute of cluster 0x0702 Metering:

* Type: 8-bit Enumeration
* Range: {0, 48}
* Access: Read Only
* Reportable: Yes
* Default value / Reset value: 0x01

**Values:**

| **TIC mode**  | **Singlephase**                                              | **Threephase**                                               |
|---------------|--------------------------------------------------------------|--------------------------------------------------------------|
| **STD Conso** | NTARF                                                        | NTARF                                                        |
| **STD Prod**  | NTARF                                                        | NTARF                                                        |
| **HST**       | * 0x01 if PTEC == "TH.." or "HC.." or "HN.." or "HCJB"<br />* 0x02 if PTEC == "HP.." or "PM.." or "HPJB"<br />* 0x03 if PTEC == "HCJW"<br />* 0x04 if PTEC == "HPJW"<br />* 0x05 if PTEC == "HCJR"<br />* 0x06 if PTEC == "HPJR" | * 0x01 if PTEC == "TH.." or "HC.." or "HN.." or "HCJB"<br />* 0x02 if PTEC == "HP.." or "PM.." or "HPJB"<br />* 0x03 if PTEC == "HCJW"<br />* 0x04 if PTEC == "HPJW"<br />* 0x05 if PTEC == "HCJR"<br />* 0x06 if PTEC == "HPJR" |


**Comment:**
Active tier number currently in use (for consumption).

Price tier and Register tier are stored along together.

Delivered means energy consumed.

----------------------





#### NumberofTiersInUse 0x0023
Attribute of cluster 0x0702 Metering:

* Type: Unsigned 8-bit integer
* Range: {0, 48}
* Access: Read Only
* Reportable: Yes
* Default value / Reset value: 0x01

**Values:**

| **TIC mode**  | **Singlephase**                                              | **Threephase**                                               |
|---------------|--------------------------------------------------------------|--------------------------------------------------------------|
| **STD Conso** | The number of tiers in use is calculated in real time by the ERL interface. The value is updated (incremented) according to the new tiers received in PJOURF+1 and PPOINTE TIC fields potentially each day.<br />This value is reset when :<br />- The tariff changes (NGTF value changes)<br />- The TIC Mode changes | The number of tiers in use is calculated in real time by the ERL interface. The value is updated (incremented) according to the new tiers received in PJOURF+1 and PPOINTE TIC fields potentially each day.<br />This value is reset when :<br />- The tariff changes (NGTF value changes)<br />- The TIC Mode changes |
| **STD Prod**  | The number of tiers in use is calculated in real time by the ERL interface. The value is updated (incremented) according to the new tiers received in PJOURF+1 and PPOINTE TIC fields potentially each day.<br />This value is reset when :<br />- The tariff changes (NGTF value changes)<br />- The TIC Mode changes | The number of tiers in use is calculated in real time by the ERL interface. The value is updated (incremented) according to the new tiers received in PJOURF+1 and PPOINTE TIC fields potentially each day.<br />This value is reset when :<br />- The tariff changes (NGTF value changes)<br />- The TIC Mode changes |
| **HST**       | * 0x01 if OPTARIF == "BASE"<br />* 0x02 if OPTARIF == "HC.." or "EJP."<br />* 0x06 if OPTARIF[0-2] == "BBR" | * 0x01 if OPTARIF == "BASE"<br />* 0x02 if OPTARIF == "HC.." or "EJP."<br />* 0x06 if OPTARIF[0-2] == "BBR" |


**Comment:**
Number of tiers used for the tariff (contract).

----------------------





#### CurrentTier1SummationDelivered 0x0100
Attribute of cluster 0x0702 Metering:

* Type: Unsigned 48-bit integer
* Range: [0x000000000000, 0xFFFFFFFFFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x000000000000

**Values:**

| **TIC mode**  | **Singlephase**                                              | **Threephase**                                               |
|---------------|--------------------------------------------------------------|--------------------------------------------------------------|
| **STD Conso** | EASF01                                                       | EASF01                                                       |
| **STD Prod**  | EASF01                                                       | EASF01                                                       |
| **HST**       | * BASE if present in TIC frame<br />* HCHC if present in TIC frame<br />* EJPHN if present in TIC frame<br />* BBRHCJB if present in TIC frame | * BASE if present in TIC frame<br />* HCHC if present in TIC frame<br />* EJPHN if present in TIC frame<br />* BBRHCJB if present in TIC frame |


**Comment:**
1st tier of cumulative energy consumed, in Wh. 

In HST Mode, only one field is present to fill attribute depending of tariff.

----------------------





#### CurrentTier1SummationReceived 0x0101
Attribute of cluster 0x0702 Metering:

* Type: Unsigned 48-bit integer
* Range: [0x000000000000, 0xFFFFFFFFFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x000000000000

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | Default value   | Default Value  |
| **STD Prod**  | EAIT            | EAIT           |
| **HST**       | Default value   | Default value  |


**Comment:**
1st tier of cumulative energy produced, in Wh. 

Not available in HST Mode.

Only one tier for STD production mode.

----------------------





#### CurrentTier2SummationDelivered 0x0102
Attribute of cluster 0x0702 Metering:

* Type: Unsigned 48-bit integer
* Range: [0x000000000000, 0xFFFFFFFFFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x000000000000

**Values:**

| **TIC mode**  | **Singlephase**                                              | **Threephase**                                               |
|---------------|--------------------------------------------------------------|--------------------------------------------------------------|
| **STD Conso** | EASF02                                                       | EASF02                                                       |
| **STD Prod**  | EASF02                                                       | EASF02                                                       |
| **HST**       | * HCHP if present in TIC frame<br />* EJPHPM if present in TIC frame<br />* BBRHPJB if present in TIC frame | * HCHP if present in TIC frame<br />* EJPHPM if present in TIC frame<br />* BBRHPJB if present in TIC frame |


**Comment:**
2nd tier of cumulative energy consumed, in Wh.

----------------------





#### CurrentTier3SummationDelivered 0x0104
Attribute of cluster 0x0702 Metering:

* Type: Unsigned 48-bit integer
* Range: [0x000000000000, 0xFFFFFFFFFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x000000000000

**Values:**

| **TIC mode**  | **Singlephase**                 | **Threephase**                  |
|---------------|---------------------------------|---------------------------------|
| **STD Conso** | EASF03                          | EASF03                          |
| **STD Prod**  | EASF03                          | EASF03                          |
| **HST**       | BBRHCJW if present in TIC frame | BBRHCJW if present in TIC frame |


**Comment:**
3rd tier of cumulative energy consumed, in Wh.

----------------------





#### CurrentTier4SummationDelivered 0x0106
Attribute of cluster 0x0702 Metering:

* Type: Unsigned 48-bit integer
* Range: [0x000000000000, 0xFFFFFFFFFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x000000000000

**Values:**

| **TIC mode**  | **Singlephase**                 | **Threephase**                  |
|---------------|---------------------------------|---------------------------------|
| **STD Conso** | EASF04                          | EASF04                          |
| **STD Prod**  | EASF04                          | EASF04                          |
| **HST**       | BBRHPJW if present in TIC frame | BBRHPJW if present in TIC frame |


**Comment:**
4th tier of cumulative energy consumed, in Wh.

----------------------





#### CurrentTier5SummationDelivered 0x0108
Attribute of cluster 0x0702 Metering:

* Type: Unsigned 48-bit integer
* Range: [0x000000000000, 0xFFFFFFFFFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x000000000000

**Values:**

| **TIC mode**  | **Singlephase**                 | **Threephase**                  |
|---------------|---------------------------------|---------------------------------|
| **STD Conso** | EASF05                          | EASF05                          |
| **STD Prod**  | EASF05                          | EASF05                          |
| **HST**       | BBRHCJR if present in TIC frame | BBRHCJR if present in TIC frame |


**Comment:**
5th tier of cumulative energy consumed, in Wh.

----------------------





#### CurrentTier6SummationDelivered 0x010A
Attribute of cluster 0x0702 Metering:

* Type: Unsigned 48-bit integer
* Range: [0x000000000000, 0xFFFFFFFFFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x000000000000

**Values:**

| **TIC mode**  | **Singlephase**                 | **Threephase**                  |
|---------------|---------------------------------|---------------------------------|
| **STD Conso** | EASF06                          | EASF06                          |
| **STD Prod**  | EASF06                          | EASF06                          |
| **HST**       | BBRHPJR if present in TIC frame | BBRHPJR if present in TIC frame |


**Comment:**
6th tier of cumulative energy consumed, in Wh.

----------------------





#### CurrentTier7SummationDelivered 0x010C
Attribute of cluster 0x0702 Metering:

* Type: Unsigned 48-bit integer
* Range: [0x000000000000, 0xFFFFFFFFFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x000000000000

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | EASF07          | EASF07         |
| **STD Prod**  | EASF07          | EASF07         |
| **HST**       | Default value   | Default value  |


**Comment:**
7th tier of cumulative energy consumed, in Wh.

----------------------





#### CurrentTier8SummationDelivered 0x010E
Attribute of cluster 0x0702 Metering:

* Type: Unsigned 48-bit integer
* Range: [0x000000000000, 0xFFFFFFFFFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x000000000000

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | EASF08          | EASF08         |
| **STD Prod**  | EASF08          | EASF08         |
| **HST**       | Default value   | Default value  |


**Comment:**
8th tier of cumulative energy consumed, in Wh.

----------------------





#### CurrentTier9SummationDelivered 0x0110
Attribute of cluster 0x0702 Metering:

* Type: Unsigned 48-bit integer
* Range: [0x000000000000, 0xFFFFFFFFFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x000000000000

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | EASF09          | EASF09         |
| **STD Prod**  | EASF09          | EASF09         |
| **HST**       | Default value   | Default value  |


**Comment:**
9th tier of cumulative energy consumed, in Wh.

----------------------





#### CurrentTier10SummationDelivered 0x0112
Attribute of cluster 0x0702 Metering:

* Type: Unsigned 48-bit integer
* Range: [0x000000000000, 0xFFFFFFFFFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x000000000000

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | EASF10          | EASF10         |
| **STD Prod**  | EASF10          | EASF10         |
| **HST**       | Default value   | Default value  |


**Comment:**
10th tier of cumulative energy consumed, in Wh.

----------------------





#### Status 0x0200
Attribute of cluster 0x0702 Metering:

* Type: 8-bit BitMap
* Range: [0x00, 0xFF]
* Access: Read Only
* Reportable: Yes
* Default value / Reset value: 0x00

**Values:**

| **TIC mode**  | **Singlephase**                                              | **Threephase**                                               |
|---------------|--------------------------------------------------------------|--------------------------------------------------------------|
| **STD Conso** | 0b0n000000 with :<br />* n = 1 if STGE bits 1 to 3 ≠ 000<br />* n = 0 in other case | 0b0n000000 with :<br />* n = 1 if STGE bits 1 to 3 ≠ 000<br />* n = 0 in other case |
| **STD Prod**  | 0b0n000000 with :<br />* n = 1 if STGE bits 1 to 3 ≠ 000<br />* n = 0 in other case | 0b0n000000 with :<br />* n = 1 if STGE bits 1 to 3 ≠ 000<br />* n = 0 in other case |
| **HST**       | 0x00                                                         | 0x00                                                         |


**Comment:**
Status register. 

In STD Mode, only one bit is used : bit 6 is 0 if meter breaker is closed, 1 in other cases.

In HST Mode, unused.

----------------------





#### ExtendedStatus 0x0204
Attribute of cluster 0x0702 Metering:

* Type: 64-bit BitMap
* Range: [0x0000000000000000,  0xFFFFFFFFFFFFFFFF]
* Access: Read Only
* Reportable: Yes
* Default value / Reset value: 0x0000000000000000

**Values:**

| **TIC mode**  | **Singlephase**                                              | **Threephase**                                               |
|---------------|--------------------------------------------------------------|--------------------------------------------------------------|
| **STD Conso** | * bit 11 (Clock Invalid) : 1 if STGE bit 16 == 1<br />* bit 24 (Terminal Cover Removed) : 1 if STGE bit 4 == 1<br />* bit 27 (Limit Threshold Exceeded) : 1 if STGE bit 7 == 1 or if SINSTS>PCOUP<br />* bit 29 (Over Voltage) : 1 if STGE bit 6 == 1<br />* bit 30 (Bi-directional Operation) : 1 if STGE bit 8 == 1<br />* bit 31 (Active Power Received) : 1 if STGE bit 9 == 1 | * bit 11 (Clock Invalid) : 1 if STGE bit 16 == 1<br />* bit 24 (Terminal Cover Removed) : 1 if STGE bit 4 == 1<br />* bit 27 (Limit Threshold Exceeded) : 1 if STGE bit 7 == 1 or if SINSTS>PCOUP or if SINSTS1 > PCOUP/3 or if SINSTS2 > PCOUP/3 or if SINSTS3 > PCOUP/3<br />* bit 29 (Over Voltage) : 1 if STGE bit 6 == 1<br />* bit 30 (Bi-directional Operation) : 1 if STGE bit 8 == 1<br />* bit 31 (Active Power Received) : 1 if STGE bit 9 == 1 |
| **STD Prod**  | * bit 11 (Clock Invalid) : 1 if STGE bit 16 == 1<br />* bit 24 (Terminal Cover Removed) : 1 if STGE bit 4 == 1<br />* bit 27 (Limit Threshold Exceeded) : 1 if STGE bit 7 == 1 or if SINSTS > PCOUP or if SINSTI > PREF<br />* bit 29 (Over Voltage) : 1 if STGE bit 6 == 1<br />* bit 30 (Bi-directional Operation) : 1 if STGE bit 8 == 1<br />* bit 31 (Active Power Received) : 1 if STGE bit 9 == 1 | * bit 11 (Clock Invalid) : 1 if STGE bit 16 == 1<br />* bit 24 (Terminal Cover Removed) : 1 if STGE bit 4 == 1<br />* bit 27 (Limit Threshold Exceeded) : 1 if STGE bit 7 == 1 or if SINSTS > PCOUP or if SINSTI > PREF or if SINSTS1 > PCOUP/3 or if SINSTS2 > PCOUP/3 or if SINSTS3 > PCOUP/3 <br />* bit 29 (Over Voltage) : 1 if STGE bit 6 == 1<br />* bit 30 (Bi-directional Operation) : 1 if STGE bit 8 == 1<br />* bit 31 (Active Power Received) : 1 if STGE bit 9 == 1 |
| **HST**       | * bit 11 (Clock Invalid) : 1 if Time Client is not set by Zigbee network or out of band (see Time cluster)<br />* bit 24 (Terminal Cover Removed) : 0<br />* bit 27 (Limit Threshold Exceeded) : 1 if ADPS == 1<br />* bit 29 (Over Voltage) : 0<br />* bit 30 (Bi-directional Operation) : 0<br />* bit 31 (Active Power Received) : 0 | * bit 11 (Clock Invalid) : 1 if Time Client is not set by Zigbee network or out of band (see Time cluster)<br />* bit 24 (Terminal Cover Removed) : 0<br />* bit 27 (Limit Threshold Exceeded) : 1 if ADIR1 >ISOUSC or if ADIR2 == ISOUSC or if ADIR3 == ISOUSC<br />* bit 29 (Over Voltage) : 0<br />* bit 30 (Bi-directional Operation) : 0<br />* bit 31 (Active Power Received) : 0 |


**Comment:**
Extended status register providing :
* Clock validity flag : bit 11 (1 = clock invalid)
* Terminal cover removed flag : bit 24 (1 = cover removed)
* Limit threshold exceeded flag : bit 27 (1 = limit exceeded)
* Over voltage flag : bit 29 (1 = over voltage)
* Bi-directional operation (production mode) flag : bit 30 (0 = consumer only mode, 1 = consumer/producer mode)
* Active power received flag : bit 31 (0 = consumption in progress, 1 = production in progress) 

----------------------





#### CurrentMeterID 0x0206
Attribute of cluster 0x0702 Metering:

* Type: Octet String
* Range: {0, 6}
* Access: Read Only
* Reportable: Yes
* Default value / Reset value: Empty string

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | VTIC            | VTIC           |
| **STD Prod**  | VTIC            | VTIC           |
| **HST**       | "AMMICC"        | "AMMICC"       |


**Comment:**
TIC version of Linky meter.

----------------------





#### ServiceDisconnectReason 0x0208
Attribute of cluster 0x0702 Metering:

* Type: 8-bit Enumeration
* Range: [0x00, 0xFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x00

**Values:**

| **TIC mode**  | **Singlephase**                                              | **Threephase**                                               |
|---------------|--------------------------------------------------------------|--------------------------------------------------------------|
| **STD Conso** | * 0x00 if STGE[1-3] == 000<br />* 0x01 if STGE[1-3] == 001<br />* 0x02 if STGE[1-3] == 010<br />* 0x03 if STGE[1-3] == 011<br />* 0x04 if STGE[1-3] == 100<br />* 0x05 if STGE[1-3] == 101<br />* 0x06 if STGE[1-3] == 110 | * 0x00 if STGE[1-3] == 000<br />* 0x01 if STGE[1-3] == 001<br />* 0x02 if STGE[1-3] == 010<br />* 0x03 if STGE[1-3] == 011<br />* 0x04 if STGE[1-3] == 100<br />* 0x05 if STGE[1-3] == 101<br />* 0x06 if STGE[1-3] == 110 |
| **STD Prod**  | * 0x00 if STGE[1-3] == 000<br />* 0x01 if STGE[1-3] == 001<br />* 0x02 if STGE[1-3] == 010<br />* 0x03 if STGE[1-3] == 011<br />* 0x04 if STGE[1-3] == 100<br />* 0x05 if STGE[1-3] == 101<br />* 0x06 if STGE[1-3] == 110 | * 0x00 if STGE[1-3] == 000<br />* 0x01 if STGE[1-3] == 001<br />* 0x02 if STGE[1-3] == 010<br />* 0x03 if STGE[1-3] == 011<br />* 0x04 if STGE[1-3] == 100<br />* 0x05 if STGE[1-3] == 101<br />* 0x06 if STGE[1-3] == 110 |
| **HST**       | 0x00                                                         | 0x00                                                         |


**Comment:**
Provides information on meter breaker state and reason of breaker opening:
* 0 : closed
* 1 : opened, power limit exceeded
* 2 : opened, over voltage
* 3 : opened, load shedding
* 4 : opened, by Euridis/PLC remote command
* 5 : opened, overheat and overcurrent
* 6 : opened, overheat without overcurrent

----------------------





#### LinkyModeOfOperation 0x0209
Attribute of cluster 0x0702 Metering:

* Type: 8-bit BitMap
* Range: [0x00, 0xFF]
* Access: Read Only
* Reportable: Yes
* Default value / Reset value: 0x00

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | 0x01            | 0x01           |
| **STD Prod**  | 0x01            | 0x01           |
| **HST**       | 0x00            | 0x00           |


**Comment:**
Linky TIC mode. Can be HST (historical) mode or STD (standard) mode.

----------------------





#### UnitofMeasure 0x0300
Attribute of cluster 0x0702 Metering:

* Type: 8-bit Enumeration
* Range: [0x00, 0xFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x00

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | 0x00            | 0x00           |
| **STD Prod**  | 0x00            | 0x00           |
| **HST**       | 0x00            | 0x00           |


**Comment:**
Unit of measure for display: kWh or kW.

----------------------





#### Multiplier 0x0301
Attribute of cluster 0x0702 Metering:

* Type: Unsigned 24-bit integer
* Range: [0x000000, 0xFFFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x000001

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | Default value   | Default value  |
| **STD Prod**  | Default value   | Default value  |
| **HST**       | Default value   | Default value  |


----------------------





#### Divisor 0x0302
Attribute of cluster 0x0702 Metering:

* Type: Unsigned 24-bit integer
* Range: [0x000000, 0xFFFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x000001

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | Default value   | Default value  |
| **STD Prod**  | Default value   | Default value  |
| **HST**       | Default value   | Default value  |


----------------------





#### SummationFormatting 0x0303
Attribute of cluster 0x0702 Metering:

* Type: 8-bit BitMap
* Range: [0x00, 0xFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0b10110011

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | 0b10110011      | 0b10110011     |
| **STD Prod**  | 0b10110011      | 0b10110011     |
| **HST**       | 0b10110011      | 0b10110011     |


**Comment:**
Formatting to convert energy values according to UnitOfMeasure (kWh). Formats Wh to kWh with 3 decimal digits.
* Bits 0 to 2 : number of digits to the right of the decimal point (3)
* Bits 3 to 6 : number of digits to the left of the decimal point (6)
* Bit 7 : if set, suppress leading zeros

----------------------





#### DemandFormatting 0x0304
Attribute of cluster 0x0702 Metering:

* Type: 8-bit BitMap
* Range: [0x00, 0xFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0b10010011

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | 0b10010011      | 0b10010011     |
| **STD Prod**  | 0b10010011      | 0b10010011     |
| **HST**       | 0b10010011      | 0b10010011     |


**Comment:**
Formatting to convert power values according to UnitOfMeasure (kW or VA). Formats W or VA to kW or VA with 3 decimal digits.
* Bits 0 to 2 : number of digits to the right of the decimal point (3)
* Bits 3 to 6 : number of digits to the left of the decimal point (2)
* Bit 7 : if set, suppress leading zeros

----------------------





#### HistoricalConsumptionFormatting 0x0305
Attribute of cluster 0x0702 Metering:

* Type: 8-bit BitMap
* Range: [0x00, 0xFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0b10110011

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | 0b10110011      | 0b10110011     |
| **STD Prod**  | 0b10110011      | 0b10110011     |
| **HST**       | 0b10110011      | 0b10110011     |


**Comment:**
Formatting to convert energy values according to UnitOfMeasure (kWh). Formats Wh to kWh with 3 decimal digits.
* Bits 0 to 2 : number of digits to the right of the decimal point (3)
* Bits 3 to 6 : number of digits to the left of the decimal point (6)
* Bit 7 : if set, suppress leading zeros

----------------------





#### MeteringDeviceType 0x0306
Attribute of cluster 0x0702 Metering:

* Type: 8-bit BitMap
* Range: [0x00, 0xFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 00x00

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | 0x00            | 0x00           |
| **STD Prod**  | 0x00            | 0x00           |
| **HST**       | 0x00            | 0x00           |


**Comment:**
Electrical Metering type.

----------------------





#### SiteID 0x0307
Attribute of cluster 0x0702 Metering:

* Type: Octet String
* Range: {0, 33}
* Access: Read Only
* Reportable: Yes
* Default value / Reset value: Empty string

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | PRM             | PRM            |
| **STD Prod**  | PRM             | PRM            |
| **HST**       | Default value   | Default value  |


**Comment:**
Electical Delivery Point reference.

----------------------





#### MeterSerialNumber 0x0308
Attribute of cluster 0x0702 Metering:

* Type: Octet String
* Range: {0, 25}
* Access: Read Only
* Reportable: Yes
* Default value / Reset value: Empty string

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | ADSC            | ADSC           |
| **STD Prod**  | ADSC            | ADSC           |
| **HST**       | ADCO            | ADCO           |


**Comment:**
Meter serial number.

----------------------





#### ModuleSerialNumber 0x030E
Attribute of cluster 0x0702 Metering:

* Type: Octet String
* Range: {0, 25}
* Access: Read Only
* Reportable: No
* Default value / Reset value: Empty string

**Values:**

| **TIC mode**  | **Singlephase**       | **Threephase**        |
|---------------|-----------------------|-----------------------|
| **STD Conso** | Manufacturer specific | Manufacturer specific |
| **STD Prod**  | Manufacturer specific | Manufacturer specific |
| **HST**       | Manufacturer specific | Manufacturer specific |


**Comment:**
Module serial number, manufacturer specific.

----------------------





#### InstantaneousDemand  0x0400
Attribute of cluster 0x0702 Metering:

* Type: Signed 24-bit integer
* Range: [-8388607, 8388607]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0

**Values:**

| **TIC mode**  | **Singlephase**                                      | **Threephase**                                       |
|---------------|------------------------------------------------------|------------------------------------------------------|
| **STD Conso** | SINSTS                                               | SINSTS                                               |
| **STD Prod**  | SINSTS if STGE bit9 == 0 or -SINSTI if STGE bit9 ==1 | SINSTS if STGE bit9 == 0 or -SINSTI if STGE bit9 ==1 |
| **HST**       | PAPP                                                 | PAPP                                                 |


**Comment:**
Instantaneous active power in kW with 3 number of digits to the right of the decimal Point.

Positive if consumption, negative if production.


Because Active Power is no available in the current  V2 TIC version, Instantaneous demand reflect Apparent Power. 

----------------------





#### CurrentDayMaxDemandDelivered 0x045D
Attribute of cluster 0x0702 Metering:

* Type: Unsigned 48-bit integer
* Range: [0x000000000000, 0xFFFFFFFFFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x000000000000

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | SMAXSN          | SMAXSN         |
| **STD Prod**  | SMAXSN          | SMAXSN         |
| **HST**       | Default value   | Default value  |


**Comment:**
Maximum apparent power (in VA) consumed during current day since 00:00. This maximum apparent power is calculated by filtering (low pass filter) instantaneous apparent power.

----------------------





#### CurrentDayMaxDemandDeliveredTime 0x045E
Attribute of cluster 0x0702 Metering:

* Type: UTCTime
* Range: [0x00000000, 0xFFFFFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x00000000

**Values:**

| **TIC mode**  | **Singlephase**     | **Threephase**      |
|---------------|---------------------|---------------------|
| **STD Conso** | Timestamp of SMAXSN | Timestamp of SMAXSN |
| **STD Prod**  | Timestamp of SMAXSN | Timestamp of SMAXSN |
| **HST**       | Default value       | Default value       |


**Comment:**
Timestamp of when CurrentDayMaxDemandDelivered has been reached during current day since 00:00.

----------------------





#### CurrentDayMaxDemandReceived 0x045F
Attribute of cluster 0x0702 Metering:

* Type: Unsigned 48-bit integer
* Range: [0x000000000000, 0xFFFFFFFFFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x000000000000

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | Default value   | Default Value  |
| **STD Prod**  | SMAXIN          | SMAXIN         |
| **HST**       | Default value   | Default value  |


**Comment:**
Maximum apparent power (in VA) produced during current day since 00:00. This maximum apparent power is calculated by filtering (low pass filter) instantaneous apparent power.

----------------------





#### CurrentDayMaxDemandReceivedTime 0x0460
Attribute of cluster 0x0702 Metering:

* Type: UTCTime
* Range: [0x00000000, 0xFFFFFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x00000000

**Values:**

| **TIC mode**  | **Singlephase**     | **Threephase**      |
|---------------|---------------------|---------------------|
| **STD Conso** | Default value       | Default Value       |
| **STD Prod**  | Timestamp of SMAXIN | Timestamp of SMAXIN |
| **HST**       | Default value       | Default value       |


**Comment:**
Timestamp of when CurrentDayMaxDemandReceived has been reached during current day since 00:00.

----------------------





#### PreviousDayMaxDemandDelivered 0x0461
Attribute of cluster 0x0702 Metering:

* Type: Unsigned 48-bit integer
* Range: [0x000000000000, 0xFFFFFFFFFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: [0x000000000000

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | SMAXSN-1        | SMAXSN-1       |
| **STD Prod**  | SMAXSN-1        | SMAXSN-1       |
| **HST**       | Default value   | PMAX           |


**Comment:**
Maximum apparent power (in VA) consumed during previous day. This maximum apparent power is calculated by filtering (low pass filter) instantaneous apparent power.

----------------------





#### PreviousDayMaxDemandDeliveredTime 0x0462
Attribute of cluster 0x0702 Metering:

* Type: UTCTime
* Range: [0x00000000, 0xFFFFFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x00000000

**Values:**

| **TIC mode**  | **Singlephase**       | **Threephase**        |
|---------------|-----------------------|-----------------------|
| **STD Conso** | Timestamp of SMAXSN-1 | Timestamp of SMAXSN-1 |
| **STD Prod**  | Timestamp of SMAXSN-1 | Timestamp of SMAXSN-1 |
| **HST**       | Default value         | Default value         |


**Comment:**
Timestamp of when PreviousDayMaxDemandDelivered has been reached during previous day.

----------------------





#### PreviousDayMaxDemandReceived 0x0463
Attribute of cluster 0x0702 Metering:

* Type: Unsigned 48-bit integer
* Range: [0x000000000000, 0xFFFFFFFFFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | Default value   | Default Value  |
| **STD Prod**  | SMAXIN-1        | SMAXIN-1       |
| **HST**       | Default value   | Default value  |


**Comment:**
Maximum apparent power (in VA) produced during previous day. This maximum apparent power is calculated by filtering (low pass filter) instantaneous apparent power.

----------------------





#### PreviousDayMaxDemandReceivedTime 0x0464
Attribute of cluster 0x0702 Metering:

* Type: UTCTime
* Range: [0x00000000, 0xFFFFFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x00000000

**Values:**

| **TIC mode**  | **Singlephase**       | **Threephase**        |
|---------------|-----------------------|-----------------------|
| **STD Conso** | Default value         | Default Value         |
| **STD Prod**  | Timestamp of SMAXIN-1 | Timestamp of SMAXIN-1 |
| **HST**       | Default value         | Default value         |


**Comment:**
Timestamp of when PreviousDayMaxDemandReceived has been reached during previous day.

----------------------





#### MaxNumberOfPeriodsDelivered 0x0500
Attribute of cluster 0x0702 Metering:

* Type: Unsigned 8-bit integer
* Range: [0x00, 0xFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x0A

**Values:**

| **TIC mode**  | **Singlephase**    | **Threephase**     |
|---------------|--------------------|--------------------|
| **STD Conso** | 0x0A (See comment) | 0x0A (See comment) |
| **STD Prod**  | 0x0A (See comment) | 0x0A (See comment) |
| **HST**       | 0x0A (See comment) | 0x0A (See comment) |


**Comment:**
MaxNumberOfPeriodsDelivered shall be set to 0x0A (10 periods) maximum. At least 6 commands must be issued to retrieve 60 minutes consumption.

----------------------





#### CurrentReactiveSummationQ1 0x0D05 
Attribute of cluster 0x0702 Metering:

* Type: Unsigned 48-bit integer
* Range: [0x000000000000, 0xFFFFFFFFFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x000000000000

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | Default value   | Default Value  |
| **STD Prod**  | ERQ1            | ERQ1           |
| **HST**       | Default value   | Default value  |


**Comment:**
Cumulative energy produced in 1st quadrant (in VARh).

Only in STD mode for a producer.

----------------------





#### CurrentReactiveSummationQ2 0x0D06
Attribute of cluster 0x0702 Metering:

* Type: Unsigned 48-bit integer
* Range: [0x000000000000, 0xFFFFFFFFFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x000000000000

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | Default value   | Default Value  |
| **STD Prod**  | ERQ2            | ERQ2           |
| **HST**       | Default value   | Default value  |


**Comment:**
Cumulative energy produced in 2nd quadrant (in VARh).

Only in STD mode for a producer.

----------------------





#### CurrentReactiveSummationQ3 0x0D07
Attribute of cluster 0x0702 Metering:

* Type: Unsigned 48-bit integer
* Range: [0x000000000000, 0xFFFFFFFFFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x000000000000

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | Default value   | Default Value  |
| **STD Prod**  | ERQ3            | ERQ3           |
| **HST**       | Default value   | Default value  |


**Comment:**
Cumulative energy produced in 3rd quadrant (in VARh).

Only in STD mode for a producer.

----------------------





#### CurrentReactiveSummationQ4 0x0D08
Attribute of cluster 0x0702 Metering:

* Type: Unsigned 48-bit integer
* Range: [0x000000000000, 0xFFFFFFFFFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x000000000000

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | Default value   | Default Value  |
| **STD Prod**  | ERQ4            | ERQ4           |
| **HST**       | Default value   | Default value  |


**Comment:**
Cumulative energy produced in 4th quadrant (in VARh).

Only in STD mode for a producer.

----------------------




### Commands

#### GetProfile 0x00
Command:

* Client / Server: Server - Received

**Comment:**
Command received by ERL interface. Asking for ERL interface to respond (Get Profile Response command) with total energy data at a specified interval period (1min interval specified by ProfileIntervalPeriod parameter of Get Profile Response command)

ERL interface can send such data only in STD mode or if time is externally set.

ERL interface uses consumption delivered only. Received energy (production) could be used in the future.

##### Parameters

###### IntervalChannel
Command parameter:

* Type: 8-bit Enumeration
* Range: [0x00, 0xFF]

**Values:**

| **TIC mode**  | **Singlephase**                                  | **Threephase**                                    |
|---------------|--------------------------------------------------|---------------------------------------------------|
| **STD Conso** | 0: Consumption Delivered                         | 0: Consumption Delivered                          |
| **STD Prod**  | 0: Consumption Delivered<br />1: Consumption Received | 0: Consumption Delivered<br />1:  Consumption Received |
| **HST**       | Not available                                    | Not available                                     |


**Comment:**
Enumerated value to select the quantity of interest returned by the GetProfileResponse command.


Linky meter interface uses consumption delivered only (enumeration value : 0). Production (enumeration value : 1) could be used in the future.


Not available in HST mode if no time server is available in the Zigbee network.

----------------------





###### EndTime
Command parameter:

* Type: UTCTime
* Range: [0x00000000, 0xFFFFFFFF]

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | Client defined  | Client defined |
| **STD Prod**  | Client defined  | Client defined |
| **HST**       | Client defined  | Client defined |


**Comment:**
Timestamp used to select an interval block from all the interval blocks available. The intervals block returned is the most recent one with its EndTime equal or older to the EndTime received here.


The most recent intervals block can be requested by the client using an EndTime set to 0x00000000, subsequent intervals blocks are requested using an EndTime set to EndTime of the previous block - (numberOfIntervalsOfThePreviousBlock x ProfileInervalPeriod).

----------------------





###### NumberOfPeriods
Command parameter:

* Type: Unsigned 8-bit integer
* Range: [0x01, 0xFF]

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | Client defined  | Client defined |
| **STD Prod**  | Client defined  | Client defined |
| **HST**       | Client defined  | Client defined |


**Comment:**
Represents the number of intervals being requested. This value cannot exceed the size stipulated in the MaxNumberOfPeriodsDelivered attribute. If more intervals are requested than can be delivered, the GetProfileResponse will return the number of intervals equal to MaxNumberOfPeriodsDelivered attribute. If fewer intervals are available for the time period, only those available are returned.

----------------------





#### GetProfileResponse 0x00
Command:

* Client / Server: Server - Generated

**Comment:**
Command send by ERL interface in response to a Get Profile command.

ERL interface will send total energy data (TotalComsumptionDelivered) at 1min interval (hh:mm:00). NumberOfPeriodsDelivered is min of MaxNumberOfPeriodsDelivered attribute and NumberOfPeriods parameter of the Get Profile command.

ERL interface can send such data only in STD mode or if time is externally set.

ERL interface uses consumption delivered only. Received energy (production) could be used in the future.

##### Parameters

###### EndTime
Command parameter:

* Type: UTCTime
* Range: [0x00000000, 0xFFFFFFFF]

**Values:**

| **TIC mode**  | **Singlephase**                | **Threephase**                 |
|---------------|--------------------------------|--------------------------------|
| **STD Conso** | End Time of last interval sent | End Time of last interval sent |
| **STD Prod**  | End Time of last interval sent | End Time of last interval sent |
| **HST**       | End Time of last interval sent | End Time of last interval sent |


**Comment:**
32-bit  value  (in  UTC)  representing  the  end  time  of  the  most chronologically recent interval send. Example: Data collected from 2:00 PM to 3:00 PM would be specified as a 3:00 PM interval (end time).

----------------------





###### Status
Command parameter:

* Type: 8-bit Enumeration
* Range: [0x00, 0xFF]

**Values:**

| **TIC mode**  | **Singlephase**                                              | **Threephase**                                               |
|---------------|--------------------------------------------------------------|--------------------------------------------------------------|
| **STD Conso** | * 0x00 if all is ok<br />* 0x02 if Interval Channel of Get Profile command ≠ 0<br />* 0x05 if no interval can be sent according to EndTime | * 0x00 if all is ok<br />* 0x02 if Interval Channel of Get Profile command ≠ 0<br />* 0x05 if no interval can be sent according to EndTime |
| **STD Prod**  | * 0x00 if all is ok<br />* 0x02 if Interval Channel of Get Profile command ≠ 0<br />* 0x05 if no interval can be sent according to EndTime | * 0x00 if all is ok<br />* 0x02 if Interval Channel of Get Profile command ≠ 0<br />* 0x05 if no interval can be sent according to EndTime |
| **HST**       | * 0x00 if all is ok<br />* 0x02 if Interval Channel of Get Profile command ≠ 0<br />* 0x03 if time is not externally set<br />* 0x05 if no interval can be sent according to EndTime | * 0x00 if all is ok<br />* 0x02 if Interval Channel of Get Profile command ≠ 0<br />* 0x03 if time is not externally set<br />* 0x05 if no interval can be sent according to EndTime |


**Comment:**
See last version of Zigbee specifications.

----------------------





###### ProfileIntervalPeriod
Command parameter:

* Type: 8-bit Enumeration
* Range: [0x00, 0xFF]

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | 8               | 8              |
| **STD Prod**  | 8               | 8              |
| **HST**       | 8               | 8              |


**Comment:**
Represents the interval or time frame used to capture metered Energy. ProfileIntervalPeriod is an   enumerated field representing the timeframes. 

The only interval period supported is 1 minute (enum 8). 

----------------------





###### NumberOfPeriodsDelivered
Command parameter:

* Type: Unsigned 8-bit integer
* Range: [0x00, 0xFF]

**Values:**

| **TIC mode**  | **Singlephase**                                         | **Threephase**                                          |
|---------------|---------------------------------------------------------|---------------------------------------------------------|
| **STD Conso** | Number of 1 minute periods available for given End Time | Number of 1 minute periods available for given End Time |
| **STD Prod**  | Number of 1 minute periods available for given End Time | Number of 1 minute periods available for given End Time |
| **HST**       | Number of 1 minute periods available for given End Time | Number of 1 minute periods available for given End Time |


**Comment:**
Represents the number of intervals ERL interface is returning. This value cannot exceed the size stipulated in the MaxNumberOfPeriodsDelivered attribute.

----------------------





###### Intervals
Command parameter:

* Type: Unsigned 24-bit integer
* Range: [0x000000, 0xFFFFFF]

**Values:**

| **TIC mode**  | **Singlephase**                                              | **Threephase**                                               |
|---------------|--------------------------------------------------------------|--------------------------------------------------------------|
| **STD Conso** | Serie of unsigned 24 bits values representing total consumed energy each minute, the most recent first | Serie of unsigned 24 bits values representing total consumed energy each minute, the most recent first |
| **STD Prod**  | Serie of unsigned 24 bits values representing total consumed energy each minute, the most recent first | Serie of unsigned 24 bits values representing total consumed energy each minute, the most recent first |
| **HST**       | Serie of unsigned 24 bits values representing total consumed energy each minute, the most recent first | Serie of unsigned 24 bits values representing total consumed energy each minute, the most recent first |


**Comment:**
Series of interval data captured using the period specified by the ProfileIntervalPeriod and EndTime fields. The content of the interval data depends on the type of information requested using the Channel field in the Get Profile Command, and will represent the change in that information since the previous interval. Data is   organized in a reverse chronological order, the most recent interval is transmitted first and the oldest interval is transmitted last. Invalid intervals should be marked as 0xFFFFFF.

----------------------





#### PublishSnapshot 0x06
Command:

* Client / Server: Server - Generated

**Comment:**
Command send by ERL interface to publish a snapshot of all the tiers, total and individual ones, in consumption and in production, calculated for a 10 min period. ERL interface responds to a Get Snapshot command. 

The ERL Interface shall calculate the individual snapshot at HH:M0:00 every 10 minutes. At least one snapshot shall be saved.

ERL interface can send such data only in STD mode or if time is externally set.

ERL interface will send consumed and produced data, in several messages depending on producer mode and used tiers number.

##### Parameters

###### SnapshotID
Command parameter:

* Type: Unsigned 32-bit integer
* Range: [0x00000000, 0xFFFFFFFF]

**Values:**

| **TIC mode**  | **Singlephase**                                              | **Threephase**                                               |
|---------------|--------------------------------------------------------------|--------------------------------------------------------------|
| **STD Conso** | Value of the current date at HH:M0:00 converted in UTC Time when a new snapshot is generated | Value of the current date at HH:M0:00 converted in UTC Time when a new snapshot is generated |
| **STD Prod**  | Value of the current date at HH:M0:00 converted in UTC Time when a new snapshot is generated | Value of the current date at HH:M0:00 converted in UTC Time when a new snapshot is generated |
| **HST**       | Value of the current date at HH:M0:00 converted in UTC Time when a new snapshot is generated | Value of the current date at HH:M0:00 converted in UTC Time when a new snapshot is generated |


**Comment:**
Unique identifier allocated by the ERL interface creating the snapshot. One ID for all commands of one snapshot.

----------------------





###### SnapshotTime
Command parameter:

* Type: UTCTime
* Range: [0x00000000, 0xFFFFFFFF]

**Values:**

| **TIC mode**  | **Singlephase**                                              | **Threephase**                                               |
|---------------|--------------------------------------------------------------|--------------------------------------------------------------|
| **STD Conso** | Value of the current date at HH:M0:00 converted in UTC Time when a new snapshot is generated | Value of the current date at HH:M0:00 converted in UTC Time when a new snapshot is generated |
| **STD Prod**  | Value of the current date at HH:M0:00 converted in UTC Time when a new snapshot is generated | Value of the current date at HH:M0:00 converted in UTC Time when a new snapshot is generated |
| **HST**       | Value of the current date at HH:M0:00 converted in UTC Time when a new snapshot is generated | Value of the current date at HH:M0:00 converted in UTC Time when a new snapshot is generated |


**Comment:**
This is a 32 bit value (in UTC Time) representing the end time at which the data snapshot (10 minutes values for all tiers) was taken. Must be HH:M0:00 calculated.

----------------------





###### TotalSnapshotsFound
Command parameter:

* Type: Unsigned 8-bit integer
* Range: [0x00, 0xFF]

**Values:**

| **TIC mode**  | **Singlephase**                                              | **Threephase**                                               |
|---------------|--------------------------------------------------------------|--------------------------------------------------------------|
| **STD Conso** | Calculated depending on the search criteria defined in the associated GetSnapshot command. | Calculated depending on the search criteria defined in the associated GetSnapshot command. |
| **STD Prod**  | Calculated depending on the search criteria defined in the associated GetSnapshot command. | Calculated depending on the search criteria defined in the associated GetSnapshot command. |
| **HST**       | Calculated depending on the search criteria defined in the associated GetSnapshot command. | Calculated depending on the search criteria defined in the associated GetSnapshot command. |


**Comment:**
An 8-bit Integer indicating the number of snapshots found, based on the search criteria defined in the associated GetSnapshot command. If the value is greater than 1, the client is able to request the next snapshot by incrementing the Snapshot Offset field in an otherwise repeated GetSnapshot command.

----------------------





###### CommandIndex
Command parameter:

* Type: Unsigned 8-bit integer
* Range: [0x00, 0xFF]

**Values:**

| **TIC mode**  | **Singlephase**                | **Threephase**                 |
|---------------|--------------------------------|--------------------------------|
| **STD Conso** | 0 to "TotalNumberOfCommands-1" | 0 to "TotalNumberOfCommands-1" |
| **STD Prod**  | 0 to "TotalNumberOfCommands-1" | 0 to "TotalNumberOfCommands-1" |
| **HST**       | 0 to "TotalNumberOfCommands-1" | 0 to "TotalNumberOfCommands-1" |


**Comment:**
The CommandIndex is used to count the payload fragments in the case where the entire payload (snapshot) does not fit into one message (TotalNumberOfCommands > 1). The CommandIndex starts at 0 and is incremented for each fragment belonging to the same command.

0 if entire payload fit in one message.

----------------------





###### TotalNumberOfCommands
Command parameter:

* Type: Unsigned 8-bit integer
* Range: [0x00, 0xFF]

**Values:**

| **TIC mode**  | **Singlephase**                                              | **Threephase**                                               |
|---------------|--------------------------------------------------------------|--------------------------------------------------------------|
| **STD Conso** | Depending on NumberOfTiersInUse attribute:<br />* 1 to 2 tiers : 1<br />* 3 to 6 tiers : 2<br />* 7 to 10 tiers: 3 | Depending on NumberOfTiersInUse attribute:<br />* 1 to 2 tiers : 1<br />* 3 to 6 tiers : 2<br />* 7 to 10 tiers: 3 |
| **STD Prod**  | For TOU Information Set DeliveredRegisters:<br /><br />Depending on NumberOfTiersInUse attribute: <br />* 1 to 2 tiers : 2<br />* 3 to 6 tiers : 3<br />* 7 to 10 tiers: 4<br /><br />For TOU Information Set ReceivedRegisters:<br />* 1 | For TOU Information Set DeliveredRegisters:<br /><br />Depending on NumberOfTiersInUse attribute: <br />* 1 to 2 tiers : 2<br />* 3 to 6 tiers : 3<br />* 7 to 10 tiers: 4<br /><br />For TOU Information Set ReceivedRegisters:<br />* 1 |
| **HST**       | Depending on OPTARIF field:<br />* 1 if OPTARIF == "BASE" or "HC.." or "EJP."<br />* 2 if OPTARIF[0-2] == "BBR" | Depending on OPTARIF field:<br />* 1 if OPTARIF == "BASE" or "HC.." or "EJP."<br />* 2 if OPTARIF[0-2] == "BBR" |


**Comment:**
In the case where the entire payload (snapshot) does not fit into one message, the Total Number of Commands field indicates the total number of sub-commands that will be returned.

One more command if producer mode.

----------------------





###### SnapshotCause
Command parameter:

* Type: 32-bit Bitmap
* Range: [0x00000000, 0xFFFFFFFF]

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | 0x00010000      | 0x00010000     |
| **STD Prod**  | 0x00010000      | 0x00010000     |
| **HST**       | 0x00010000      | 0x00010000     |


**Comment:**
A 32-bit BitMap indicating the cause of the snapshot. The Only one available snapshot cause value in the ERL Interface is the Scheduled Snapshot (bit 16 = 1, enumeration value equal 0x00010000).

----------------------





###### SnapshotPayloadType
Command parameter:

* Type: Unsigned 8-bit integer
* Range: [0x00, 0xFF]

**Values:**

| **TIC mode**  | **Singlephase**                                              | **Threephase**                                               |
|---------------|--------------------------------------------------------------|--------------------------------------------------------------|
| **STD Conso** | 4                                                            | 4                                                            |
| **STD Prod**  | 4 for consumption commands (1 to 3 commands), 5 for the production command | 4 for consumption commands (1 to 3 commands), 5 for the production command |
| **HST**       | 4                                                            | 4                                                            |


**Comment:**
The SnapshotPayloadType is an 8-bit enumerator defining the format of the SnapshotSub-Payload in this message. The different available snapshot types available in the ERL Interface are:
* 4 : TOU Information Set Delivered (no billing). Used for delivered tiers (consumption)
* 5 : TOU Information Set Received (no billing). Used for production tier

----------------------





###### SnapshotSub-Payload
Command parameter:

* Type: Structure
* Range: Variable length

**Values:**

| **TIC mode**  | **Singlephase**                                              | **Threephase**                                               |
|---------------|--------------------------------------------------------------|--------------------------------------------------------------|
| **STD Conso** | ** CurrentSummationDelivered at SnapshotTime<br />** NumberOfTiersInUse attribute<br />** Serie of CurrentTier1SummationDelivered to CurrentTierNSummationDelivered with N=NumberOfTiersInUse  | ** CurrentSummationDelivered at SnapshotTime<br />** NumberOfTiersInUse attribute<br />** Serie of CurrentTier1SummationDelivered to CurrentTierNSummationDelivered with N=NumberOfTiersInUse |
| **STD Prod**  | * if SnapshotPayloadType == 4 :<br />** CurrentSummationDelivered at SnapshotTime<br />** NumberOfTiersInUse attribute<br />** Serie of CurrentTier1SummationDelivered to CurrentTierNSummationDelivered with N=NumberOfTiersInUse at SnapshotTime<br /><br />* if SnapshotPayloadType == 5 :<br />** CurrentSummationReceived at SnapshotTime<br />** 1<br />** CurrentSummationReceived at SnapshotTime | if SnapshotPayloadType == 4 :<br />** CurrentSummationDelivered at SnapshotTime<br />** NumberOfTiersInUse attribute<br />** Serie of CurrentTier1SummationDelivered to CurrentTierNSummationDelivered with N=NumberOfTiersInUse at SnapshotTime<br /><br />* if SnapshotPayloadType == 5 :<br />** CurrentSummationReceived at SnapshotTime<br />** 1<br />** CurrentSummationReceived at SnapshotTime |
| **HST**       | * if OPTARIF == "BASE" : <br />** CurrentSummationDelivered at SnapshotTime<br />** 1<br />** Serie of tiers :<br />*** CurrentTier1SummationDelivered at SnapshotTime<br /><br />* if OPTARIF == "HC.." :<br />** CurrentSummationDelivered at SnapshotTime<br />** 2<br />** Serie of tiers :<br />*** CurrentTier1SummationDelivered at SnapshotTime<br />*** CurrentTier2SummationDelivered at SnapshotTime<br /><br />* if OPTARIF == "EJP." :<br />** CurrentSummationDelivered at SnapshotTime<br />** 2<br />** Serie of tiers :<br />*** CurrentTier1SummationDelivered at SnapshotTime<br />*** CurrentTier2SummationDelivered at SnapshotTime<br /><br />* if OPTARIF[0-2] == "BBR" :<br />** CurrentSummationDelivered at SnapshotTime<br />** 6<br />** Serie of tiers :<br />*** CurrentTier1SummationDelivered at SnapshotTime<br />*** CurrentTier2SummationDelivered at SnapshotTime<br />*** CurrentTier3SummationDelivered at SnapshotTime<br />*** CurrentTier4SummationDelivered at SnapshotTime<br />*** CurrentTier5SummationDelivered at SnapshotTime<br />*** CurrentTier6SummationDelivered at SnapshotTime<br /> | * if OPTARIF == "BASE" : <br />** CurrentSummationDelivered at SnapshotTime<br />** 1<br />** Serie of tiers :<br />*** CurrentTier1SummationDelivered at SnapshotTime<br /><br />* if OPTARIF == "HC.." :<br />** CurrentSummationDelivered at SnapshotTime<br />** 2<br />** Serie of tiers :<br />*** CurrentTier1SummationDelivered at SnapshotTime<br />*** CurrentTier2SummationDelivered at SnapshotTime<br /><br />* if OPTARIF == "EJP." :<br />** CurrentSummationDelivered at SnapshotTime<br />** 2<br />** Serie of tiers :<br />*** CurrentTier1SummationDelivered at SnapshotTime<br />*** CurrentTier2SummationDelivered at SnapshotTime<br /><br />* if OPTARIF[0-2] == "BBR" :<br />** CurrentSummationDelivered at SnapshotTime<br />** 6<br />** Serie of tiers :<br />*** CurrentTier1SummationDelivered at SnapshotTime<br />*** CurrentTier2SummationDelivered at SnapshotTime<br />*** CurrentTier3SummationDelivered at SnapshotTime<br />*** CurrentTier4SummationDelivered at SnapshotTime<br />*** CurrentTier5SummationDelivered at SnapshotTime<br />*** CurrentTier6SummationDelivered at SnapshotTime |


**Comment:**
The format of the SnapshotSub-Payload differs depending on the SnapshotPayloadType, as shown below. Note that, where the entire payload (snapshot) does not fit into one message, only the leading (non-Sub-Payload) fields of the Snapshot payload are repeated in each command; the SnapshotSub-Payload is divided over the required number of commands.


Structure:
* if SnapshotPayloadType == 4 (consumption) : 
** Unsigned 48 bits integer ⇒ CurrentSummationDelivered
** Unsigned 8 bits integers ⇒ NumberOfTiersInUse
** Serie of NumberOfTiersInUse unsigned 48 bits integers ⇒ CurrentTier1SummationDelivered to CurrentTier10SummationDelivered dependinf of NumberOfTiersInUse

* if SnapshotPayloadType == 5 (production) : 
** Unsigned 48 bits integer ⇒ CurrentSummationReceived
** Unsigned 8 bits integers ⇒ 1
** Serie of 1 unsigned 48 bits integers ⇒ CurrentTier1SummationReceived

----------------------





#### GetSnapshot 0x06
Command:

* Client / Server: Server - Received

**Comment:**
Command received by ERL interface. Asking for ERL interface to respond (Publish Snapshot command) with energy data (total tier and each individual one) at 10min interval period. The ERL Interface shall calculate the individual snapshot at HH:M0:00 every 10 minutes.
ERL interface can send such data only in STD mode or if time is externally set.

ERL interface will send delivered and received consumption data, in several messages depending on producer mode and used tiers number.

##### Parameters

###### EarliestStartTime
Command parameter:

* Type: UTCTime
* Range: [0x00000000, 0xFFFFFFFF]

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | Client defined  | Client defined |
| **STD Prod**  | Client defined  | Client defined |
| **HST**       | Client defined  | Client defined |


**Comment:**
A UTC Timestamp indicating the earliest time of a snapshot to be returned by a corresponding Publish Snapshot command. Snapshots with a timestamp equal to or greater than the specified Earliest Start Time shall be returned.

----------------------





###### LatestEndTime
Command parameter:

* Type: UTCTime
* Range: [0x00000000, 0xFFFFFFFF]

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | Client defined  | Client defined |
| **STD Prod**  | Client defined  | Client defined |
| **HST**       | Client defined  | Client defined |


**Comment:**
A UTC Timestamp indicating the latest time of a snapshot to be returned by a corresponding Publish Snapshot command. Snapshots with a timestamp less than the specified Latest End Time shall be returned.

----------------------





###### SnapshotOffset
Command parameter:

* Type: Unsigned 8-bit integer
* Range: [0x00, 0xFF]

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | Client defined  | Client defined |
| **STD Prod**  | Client defined  | Client defined |
| **HST**       | Client defined  | Client defined |


**Comment:**
Where multiple snapshots satisfy the selection criteria specified by the other fields in this command, this field identifies the individual snapshot to be returned. An offset of zero (0x00) indicates that the first snapshot satisfying the selection criteria should be returned, 0x01 the second, and so on.

----------------------





###### SnapshotCause
Command parameter:

* Type: 32-bit Bitmap
* Range: [0x00000000, 0xFFFFFFFF]

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | 0x00010000      | 0x00010000     |
| **STD Prod**  | 0x00010000      | 0x00010000     |
| **HST**       | 0x00010000      | 0x00010000     |


**Comment:**
This field is used to select only snapshots that were taken due to a specific cause. The only one available Snapshot cause is the Scheduled Snapshot (bit 16 = 1).

----------------------





#### GetSampledDataResponse 0x07
Command:

* Client / Server: Server - Generated

**Comment:**
This command is send by the ERL interface to provide real time sampled data to the client (instantaneous demand). The interval between samples returned is defined by ERL interface and given in the command parameters. It can be 2 to 5s. Note that it is the responsibility of the client to ensure that it does not request more samples than can be held in a single command payload.


##### Parameters

###### SampleID
Command parameter:

* Type: Unsigned 16-bit integer
* Range: [0x0000, 0xFFFF]

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | 0x0000          | 0x0000         |
| **STD Prod**  | 0x0000          | 0x0000         |
| **HST**       | 0x0000          | 0x0000         |


**Comment:**
Unique identifier allocated to this Sampling session. This field allows devices to match response data with the appropriate request.

----------------------





###### SampleStartTime
Command parameter:

* Type: UTCTime
* Range: [0x00000000, 0xFFFFFFFF]

**Values:**

| **TIC mode**  | **Singlephase**                    | **Threephase**                     |
|---------------|------------------------------------|------------------------------------|
| **STD Conso** | Timestamp of first sample returned | Timestamp of first sample returned |
| **STD Prod**  | Timestamp of first sample returned | Timestamp of first sample returned |
| **HST**       | Timestamp of first sample returned | Timestamp of first sample returned |


**Comment:**
A UTC Time field to denote the time of the first sample (the oldest) returned in this response.

----------------------





###### SampleType
Command parameter:

* Type: 8-bit Enumeration
* Range: [0x00, 0xFF]

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | 4               | 4              |
| **STD Prod**  | 4               | 4              |
| **HST**       | 4               | 4              |


**Comment:**
An 8 bit enumeration that identifies the type of data being sampled. For the ERL interface, the only possible value is: 4 (InstantaneousDemand).

----------------------





###### SampleRequestInterval
Command parameter:

* Type: Unsigned 16-bit integer
* Range: [0x0000, 0xFFFF]

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | 2               | 2              |
| **STD Prod**  | 2               | 2              |
| **HST**       | 2               | 2              |


**Comment:**
An unsigned 16-bit field representing the interval of time in seconds between samples. Should be 2 for the ERL interface.

----------------------





###### NumberOfSamples
Command parameter:

* Type: Unsigned 16-bit integer
* Range: [0x0000, 0xFFFF]

**Values:**

| **TIC mode**  | **Singlephase**                                              | **Threephase**                                               |
|---------------|--------------------------------------------------------------|--------------------------------------------------------------|
| **STD Conso** | Number of InstantaneousDemand samples available in the Samples list | Number of InstantaneousDemand samples available in the Samples list |
| **STD Prod**  | Number of InstantaneousDemand samples available in the Samples list | Number of InstantaneousDemand samples available in the Samples list |
| **HST**       | Number of InstantaneousDemand samples available in the Samples list | Number of InstantaneousDemand samples available in the Samples list |


**Comment:**
Represents the number of samples being returned (less or equal to requested number and max supported number).

----------------------





###### Samples
Command parameter:

* Type: List of signed 24-bit integers
* Range: Variable length

**Values:**

| **TIC mode**  | **Singlephase**                                              | **Threephase**                                               |
|---------------|--------------------------------------------------------------|--------------------------------------------------------------|
| **STD Conso** | List of NumberOfSamples Instantaneous Demand values, beginning at SampleStartTime | List of NumberOfSamples Instantaneous Demand values, beginning at SampleStartTime |
| **STD Prod**  | List of NumberOfSamples Instantaneous Demand values, beginning at SampleStartTime | List of NumberOfSamples Instantaneous Demand values, beginning at SampleStartTime |
| **HST**       | List of NumberOfSamples Instantaneous Demand values, beginning at SampleStartTime | List of NumberOfSamples Instantaneous Demand values, beginning at SampleStartTime |


**Comment:**
Series of data samples captured using the interval specified by the SampleRequestInterval parameter. Each sample contains the change in the relevant data since the previous sample. Data is organised in a chronological  order, the oldest sample is transmitted first and the most recent sample is transmitted last. Invalid samples should be marked as 0xFFFFFF.

----------------------





#### GetSampledData 0x08
Command:

* Client / Server: Server - Received

**Comment:**
This command is received to request from the ERL interface real time sampled data (instantaneous demand). The interval between samples (Sample Request Interval) returned is defined by ERL interface and given in the response command. The value of Sample Request Interval is 2 seconds. ERL Interface will interpolate the Instantaneous Demand with a 2 seconds period.  
Note that it is the responsibility of the client to ensure that it does not request more samples than can be held in a single command payload.


##### Parameters

###### SampleID
Command parameter:

* Type: Unsigned 16-bit integer
* Range: [0x0000, 0xFFFF]

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | 0X0000          | 0X0000         |
| **STD Prod**  | 0X0000          | 0X0000         |
| **HST**       | 0X0000          | 0X0000         |


**Comment:**
Unique identifier allocated to this Sampling session. This field allows devices to match response data with the appropriate request.

----------------------





###### EarliestSampleTime
Command parameter:

* Type: UTCTime
* Range: [0x00000000, 0xFFFFFFFF]

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | Client defined  | Client defined |
| **STD Prod**  | Client defined  | Client defined |
| **HST**       | Client defined  | Client defined |


**Comment:**
A UTC Timestamp indicating the earliest time of a sample to be returned. Samples with a timestamp equal to or greater than the specified EarliestSampleTime shall be returned.

----------------------





###### SampleType
Command parameter:

* Type: 8-bit Enumeration
* Range: [0x00, 0xFF]

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | 0b00000100      | 0b00000100     |
| **STD Prod**  | 0b00000100      | 0b00000100     |
| **HST**       | 0b00000100      | 0b00000100     |


**Comment:**
A 8 bit enumeration that identifies the required type of sampled data. Here, enumeration value is 4 (Instantaneous Demand).

----------------------





###### NumberOfSamples
Command parameter:

* Type: Unsigned 16-bit integer
* Range: [0x0001, 0xFFFF]

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | Client defined  | Client defined |
| **STD Prod**  | Client defined  | Client defined |
| **HST**       | Client defined  | Client defined |


**Comment:**
Represents the number of samples being requested. If fewer samples are available for the time period, only those available are returned.

----------------------




<div style="page-break-after: always;"></div>












##  Messaging 0x0703
This cluster provides an interface for passing text messages arriving from Linky meter (16 bytes and 32 bytes messages) between ZigBee devices.

* Mandatory / Optional: M

* Client / Server: ( S )



### Commands

#### DisplayMessage 0x00
Command:

* Client / Server: Server - Generated

**Comment:**
Command generated when a new MSG1 or MSG2 is received by Linky meter, or when a "Get Last Message" command is received.

Not used in HST MODE.

##### Parameters

###### MessageID
Command parameter:

* Type: Unsigned 32-bit integer
* Range: [0x00000000, 0xFFFFFFFF]

**Values:**

| **TIC mode**  | **Singlephase**                                              | **Threephase**                                               |
|---------------|--------------------------------------------------------------|--------------------------------------------------------------|
| **STD Conso** | Timestamp extracted from the DATE TIC field when a new MSG1 or MSG2 is received | Timestamp extracted from the DATE TIC field when a new MSG1 or MSG2 is received |
| **STD Prod**  | Timestamp extracted from the DATE TIC field when a new MSG1 or MSG2 is received | Timestamp extracted from the DATE TIC field when a new MSG1 or MSG2 is received |
| **HST**       | Not applicable                                               | Not applicable                                               |


----------------------





###### MessageControl
Command parameter:

* Type: 8-bit BitMap
* Range: [0x00, 0xFF]

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | 0b00000000      | 0b00000000     |
| **STD Prod**  | 0b00000000      | 0b00000000     |
| **HST**       | Not applicable  | Not applicable |


----------------------





###### StartTime
Command parameter:

* Type: UTCTime
* Range: [0x00000000, 0xFFFFFFFF]

**Values:**

| **TIC mode**  | **Singlephase**                         | **Threephase**                          |
|---------------|-----------------------------------------|-----------------------------------------|
| **STD Conso** | Timestamp extracted from DATE TIC field | Timestamp extracted from DATE TIC field |
| **STD Prod**  | Timestamp extracted from DATE TIC field | Timestamp extracted from DATE TIC field |
| **HST**       | Not applicable                          | Not applicable                          |


----------------------





###### DurationInMinutes
Command parameter:

* Type: Unsigned 16-bit integer
* Range: [0x0000, 0xFFFF]

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | 0xFFFF          | 0xFFFF         |
| **STD Prod**  | 0xFFFF          | 0xFFFF         |
| **HST**       | Not applicable  | Not applicable |


----------------------





###### Message
Command parameter:

* Type: String
* Range: {0, 32}

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | MSG1 or MSG2    | MSG1 or MSG2   |
| **STD Prod**  | MSG1 or MSG2    | MSG1 or MSG2   |
| **HST**       | Not applicable  | Not applicable |


----------------------





#### GetLastMessage 0x00
Command:

* Client / Server: Server - Received

**Comment:**
When this command is received, shall generates "Display Message" command with the last MSG1 or MSG2 received.

Not used in HST MODE.


#### CancelMessage 0x01
Command:

* Client / Server: Server - Generated

**Comment:**
When the next MSG1 appears, the ERL interface shall send a "Cancel Message" command for the previous MSG1 message (if exists).

When the next MSG2 appears, the ERL interface shall send a "Cancel Message" command for the previous MSG2 message (if exists).

Not used in HST MODE.

##### Parameters

###### MessageID
Command parameter:

* Type: Unsigned 32-bit integer
* Range: [0x00000000, 0xFFFFFFFF]

**Values:**

| **TIC mode**  | **Singlephase**                                            | **Threephase**                                             |
|---------------|------------------------------------------------------------|------------------------------------------------------------|
| **STD Conso** | Message ID generated when the last MSG1 or MSG2 was issued | Message ID generated when the last MSG1 or MSG2 was issued |
| **STD Prod**  | Message ID generated when the last MSG1 or MSG2 was issued | Message ID generated when the last MSG1 or MSG2 was issued |
| **HST**       | Not applicable                                             | Not applicable                                             |


----------------------





#### MessageConfirmation 0x01
Command:

* Client / Server: Server - Received

**Comment:**
Received when a client equipment confirms reception of a "Display Message" send by the ERL interface.

Not used in HST MODE.

##### Parameters

###### MessageID
Command parameter:

* Type: Unsigned 32-bit integer
* Range: [0x00000000, 0xFFFFFFFF]

**Values:**

| **TIC mode**  | **Singlephase**                                              | **Threephase**                                               |
|---------------|--------------------------------------------------------------|--------------------------------------------------------------|
| **STD Conso** | Message ID generated and send when the last MSG1 or MSG2 was issued | Message ID generated and send when the last MSG1 or MSG2 was issued |
| **STD Prod**  | Message ID generated and send when the last MSG1 or MSG2 was issued | Message ID generated and send when the last MSG1 or MSG2 was issued |
| **HST**       | Not applicable                                               | Not applicable                                               |


----------------------





###### ConfirmationTime
Command parameter:

* Type: UTCTime
* Range: [0x00000000, 0xFFFFFFFF]

**Values:**

| **TIC mode**  | **Singlephase**                                              | **Threephase**                                               |
|---------------|--------------------------------------------------------------|--------------------------------------------------------------|
| **STD Conso** | Confirmation time (Timestamp) generated by the client equipment when it received a "Display Message" to confirm the reception | Confirmation time (Timestamp) generated by the client equipment when it received a "Display Message" to confirm the reception |
| **STD Prod**  | Confirmation time (Timestamp) generated by the client equipment when it received a "Display Message" to confirm the reception | Confirmation time (Timestamp) generated by the client equipment when it received a "Display Message" to confirm the reception |
| **HST**       | Not applicable                                               | Not applicable                                               |


----------------------





###### MessageConfirmationControl
Command parameter:

* Type: 8-bit BitMap
* Range: [0x00, 0xFF]

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | 0b00000000      | 0b00000000     |
| **STD Prod**  | 0b00000000      | 0b00000000     |
| **HST**       | Not applicable  | Not applicable |


----------------------





###### MessageConfirmationResponse
Command parameter:

* Type: Octet String
* Range: {1, 21}

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | "OK"            | "OK"           |
| **STD Prod**  | "OK"            | "OK"           |
| **HST**       | Not applicable  | Not applicable |


----------------------




<div style="page-break-after: always;"></div>












##  Daily Schedule 0x070D
The Daily Schedule cluster implements commands to transfer daily calendar information. It provides tiers information and auxiliary switches state for each period of a day, and current information.

* Mandatory / Optional: M

* Client / Server: ( S )



| **Identifier** | **Name**                        | **Type**          | **Range**                | **Access** | **Reportable** |
|----------------|---------------------------------|-------------------|--------------------------|------------|----------------|
| 0x0000         | AuxSwitch1Label                 | Octet String      | {1, 23}                  | Read Write | No             |
| 0x0001         | AuxSwitch2Label                 | Octet String      | {1, 23}                  | Read Write | No             |
| 0x0002         | AuxSwitch3Label                 | Octet String      | {1, 23}                  | Read Write | No             |
| 0x0003         | AuxSwitch4Label                 | Octet String      | {1, 23}                  | Read Write | No             |
| 0x0004         | AuxSwitch5Label                 | Octet String      | {1, 23}                  | Read Write | No             |
| 0x0005         | AuxSwitch6Label                 | Octet String      | {1, 23}                  | Read Write | No             |
| 0x0006         | AuxSwitch7Label                 | Octet String      | {1, 23}                  | Read Write | No             |
| 0x0007         | AuxSwitch8Label                 | Octet String      | {1, 23}                  | Read Write | No             |
| 0x0100         | CurrentAuxiliaryLoadSwitchState | 8-bit BitMap      | [0x00, 0xFF]             | Read Only  | Yes            |
| 0x0101         | CurrentDeliveredTier            | 8-bit Enumeration | {0, 48}                  | Read Only  | Yes            |
| 0x0102         | CurrentTierLabel                | Octet String      | {1, 17}                  | Read Only  | No             |
| 0x0103         | LinkyPeakPeriodStatus           | 8-bit BitMap      | [0x00, 0xFF]             | Read Only  | Yes            |
| 0x0104         | PeakStartTime                   | UTCTime           | [0x00000000, 0xFFFFFFFF] | Read Only  | No             |
| 0x0105         | PeakEndTime                     | UTCTime           | [0x00000000, 0xFFFFFFFF] | Read Only  | No             |
| 0x0106         | CurrentTariffLabel              | Octet String      | {1, 25}                  | Read Only  | No             |


### Attributes

#### AuxSwitch1Label 0x0000
Attribute of cluster 0x070D Daily Schedule:

* Type: Octet String
* Range: {1, 23}
* Access: Read Write
* Reportable: No
* Default value / Reset value: Empty String

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | "CS1"           | "CS1"          |
| **STD Prod**  | "CS1"           | "CS1"          |
| **HST**       | "CS1"           | "CS1"          |


**Comment:**
Label for 1st auxiliary switch.

Corresponds to the physical dry contact of the Linky meter (mostly used for heat water tank).

----------------------





#### AuxSwitch2Label 0x0001
Attribute of cluster 0x070D Daily Schedule:

* Type: Octet String
* Range: {1, 23}
* Access: Read Write
* Reportable: No
* Default value / Reset value: Empty String

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | "CSV2"          | "CSV2"         |
| **STD Prod**  | "CSV2"          | "CSV2"         |
| **HST**       | Default value   | Default value  |


**Comment:**
Exists only in STD mode.

Label for 2nd auxiliary switch.

Can be configured depending on CRE recommandation, future standardisation or by the client.

----------------------





#### AuxSwitch3Label 0x0002
Attribute of cluster 0x070D Daily Schedule:

* Type: Octet String
* Range: {1, 23}
* Access: Read Write
* Reportable: No
* Default value / Reset value: Empty String

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | "CSV3"          | "CSV3"         |
| **STD Prod**  | "CSV3"          | "CSV3"         |
| **HST**       | Default value   | Default value  |


**Comment:**
Exists only in STD mode.

Label for 3rd auxiliary switch.

Can be configured depending on CRE recommandation, future standardisation or by the client.

----------------------





#### AuxSwitch4Label 0x0003
Attribute of cluster 0x070D Daily Schedule:

* Type: Octet String
* Range: {1, 23}
* Access: Read Write
* Reportable: No
* Default value / Reset value: Empty String

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | "CSV4"          | "CSV4"         |
| **STD Prod**  | "CSV4"          | "CSV4"         |
| **HST**       | Default value   | Default value  |


**Comment:**
Exists only in STD mode.

Label for 4th auxiliary switch.

Can be configured depending on CRE recommandation, future standardisation or by the client.

----------------------





#### AuxSwitch5Label 0x0004
Attribute of cluster 0x070D Daily Schedule:

* Type: Octet String
* Range: {1, 23}
* Access: Read Write
* Reportable: No
* Default value / Reset value: Empty String

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | "CSV5"          | "CSV5"         |
| **STD Prod**  | "CSV5"          | "CSV5"         |
| **HST**       | Default value   | Default value  |


**Comment:**
Exists only in STD mode.

Label for 5th auxiliary switch.

Can be configured depending on CRE recommandation, future standardisation or by the client.

----------------------





#### AuxSwitch6Label 0x0005
Attribute of cluster 0x070D Daily Schedule:

* Type: Octet String
* Range: {1, 23}
* Access: Read Write
* Reportable: No
* Default value / Reset value: Empty String

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | "CSV6"          | "CSV6"         |
| **STD Prod**  | "CSV6"          | "CSV6"         |
| **HST**       | Default value   | Default value  |


**Comment:**
Exists only in STD mode.

Label for 6th auxiliary switch.

Can be configured depending on CRE recommandation, future standardisation or by the client.

----------------------





#### AuxSwitch7Label 0x0006
Attribute of cluster 0x070D Daily Schedule:

* Type: Octet String
* Range: {1, 23}
* Access: Read Write
* Reportable: No
* Default value / Reset value: Empty String

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | "CSV7"          | "CSV7"         |
| **STD Prod**  | "CSV7"          | "CSV7"         |
| **HST**       | Default value   | Default value  |


**Comment:**
Exists only in STD mode.

Label for 7th auxiliary switch.

Can be configured depending on CRE recommandation, future standardisation or by the client.

----------------------





#### AuxSwitch8Label 0x0007
Attribute of cluster 0x070D Daily Schedule:

* Type: Octet String
* Range: {1, 23}
* Access: Read Write
* Reportable: No
* Default value / Reset value: Empty String

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | "CSV8"          | "CSV8"         |
| **STD Prod**  | "CSV8"          | "CSV8"         |
| **HST**       | Default value   | Default value  |


**Comment:**
Exists only in STD mode.

Label for 8th auxiliary switch.

Can be configured depending on CRE recommandation, future standardisation or by the client.

----------------------





#### CurrentAuxiliaryLoadSwitchState 0x0100
Attribute of cluster 0x070D Daily Schedule:

* Type: 8-bit BitMap
* Range: [0x00, 0xFF]
* Access: Read Only
* Reportable: Yes
* Default value / Reset value: 0b00000000

**Values:**

| **TIC mode**  | **Singlephase**                                              | **Threephase**                                               |
|---------------|--------------------------------------------------------------|--------------------------------------------------------------|
| **STD Conso** | RELAIS                                                       | RELAIS                                                       |
| **STD Prod**  | RELAIS                                                       | RELAIS                                                       |
| **HST**       | 0b0000000x with x (bit 0) defined below.<br /><br />* bit 0 = 1 if PTEC is present in TIC frame and PTEC == "HC.." (HPHC Mode)<br />* bit 0 = 1 if PTEC is present in TIC frame and PTEC == "HN.." (EJP Mode)<br />* bit 0 = 1 if (OPTARIF[0-2] == "BBR") and (bits 4 and 3 of OPTARIF[3] == 01) and (PTEC == "HCJB" or "HCJW" or "HCJR") (TEMPO Mode, circuit 1 program A)<br />* bit 0 = 1 if (OPTARIF[0-2] == "BBR") and (bits 4 and 3 of OPTARIF[3] == 10) and (PTEC == "HCJB" or "HPJB" or "HCJW" or "HCJR") (TEMPO Mode, circuit 1 program B)<br />* bit 0 = 1 if (OPTARIF[0-2] == "BBR") and (bits 4 and 3 of OPTARIF[3] == 11) and (PTEC == "HCJB" or "HPJB" or "HCJW" or "HPJW" or "HCJR") (TEMPO Mode, circuit 1 program C)<br />* bit 0 = 0 in other cases<br /><br />0b000000x0 with x (bit 1) defined below.<br /><br />• bit 1 = 1 if (OPTARIF[0-2] == "BBR") and (bits 2 to 0 of OPTARIF[3] == 001) and (PTEC == "HPJR") (TEMPO Mode, circuit 2 program CHAU 1)<br />• bit 1 = 1 if (OPTARIF[0-2] == "BBR") and (bits 2 to 0 of OPTARIF[3] == 010) and (PTEC == "HCJR" or "HPJR") (TEMPO Mode, circuit 2 program CHAU 2)<br />• bit 1 = 1 if (OPTARIF[0-2] == "BBR") and (bits 2 to 0 of OPTARIF[3] == 011) and (PTEC == "HPJW" or "HCJR" or "HPJR") (TEMPO Mode, circuit 2 program CHAU 3)<br />• bit 1 = 1 if (OPTARIF[0-2] == "BBR") and (bits 2 to 0 of OPTARIF[3] == 100) and (PTEC == "HCJW" or "HPJW" or "HCJR" or "HPJR") (TEMPO Mode, circuit 2 program CHAU 4)<br />• bit 1 = 1 if (OPTARIF[0-2] == "BBR") and (bits 2 to 0 of OPTARIF[3] == 101) and (PTEC == "HPJB" or "HCJW" or "HPJW" or "HCJR" or "HPJR") (TEMPO Mode, circuit 2 program CHAU 5)<br />• bit 1 = 1 if (OPTARIF[0-2] == "BBR") and (bits 2 to 0 of OPTARIF[3] == 110) (TEMPO Mode, circuit 2 program CHAU 6)<br />• bit 1 = 1 if (OPTARIF[0-2] == "BBR") and (bits 2 to 0 of OPTARIF[3] == 111) and (PTEC == "HPJB" or "HPJW" or "HPJR") (TEMPO Mode, circuit 2 program CHAU 7)<br />• bit 1 = 0 in other cases | 0b0000000x with x (bit 0) defined below.<br /><br />* bit 0 = 1 if PTEC is present in TIC frame and PTEC == "HC.." (HPHC Mode)<br />* bit 0 = 1 if PTEC is present in TIC frame and PTEC == "HN.." (EJP Mode)<br />* bit 0 = 1 if (OPTARIF[0-2] == "BBR") and (bits 4 and 3 of OPTARIF[3] == 01) and (PTEC == "HCJB" or "HCJW" or "HCJR") (TEMPO Mode, circuit 1 program A)<br />* bit 0 = 1 if (OPTARIF[0-2] == "BBR") and (bits 4 and 3 of OPTARIF[3] == 10) and (PTEC == "HCJB" or "HPJB" or "HCJW" or "HCJR") (TEMPO Mode, circuit 1 program B)<br />* bit 0 = 1 if (OPTARIF[0-2] == "BBR") and (bits 4 and 3 of OPTARIF[3] == 11) and (PTEC == "HCJB" or "HPJB" or "HCJW" or "HPJW" or "HCJR") (TEMPO Mode, circuit 1 program C)<br />* bit 0 = 0 in other cases<br /><br />0b000000x0 with x (bit 1) defined below.<br /><br />• bit 1 = 1 if (OPTARIF[0-2] == "BBR") and (bits 2 to 0 of OPTARIF[3] == 001) and (PTEC == "HPJR") (TEMPO Mode, circuit 2 program CHAU 1)<br />• bit 1 = 1 if (OPTARIF[0-2] == "BBR") and (bits 2 to 0 of OPTARIF[3] == 010) and (PTEC == "HCJR" or "HPJR") (TEMPO Mode, circuit 2 program CHAU 2)<br />• bit 1 = 1 if (OPTARIF[0-2] == "BBR") and (bits 2 to 0 of OPTARIF[3] == 011) and (PTEC == "HPJW" or "HCJR" or "HPJR") (TEMPO Mode, circuit 2 program CHAU 3)<br />• bit 1 = 1 if (OPTARIF[0-2] == "BBR") and (bits 2 to 0 of OPTARIF[3] == 100) and (PTEC == "HCJW" or "HPJW" or "HCJR" or "HPJR") (TEMPO Mode, circuit 2 program CHAU 4)<br />• bit 1 = 1 if (OPTARIF[0-2] == "BBR") and (bits 2 to 0 of OPTARIF[3] == 101) and (PTEC == "HPJB" or "HCJW" or "HPJW" or "HCJR" or "HPJR") (TEMPO Mode, circuit 2 program CHAU 5)<br />• bit 1 = 1 if (OPTARIF[0-2] == "BBR") and (bits 2 to 0 of OPTARIF[3] == 110) (TEMPO Mode, circuit 2 program CHAU 6)<br />• bit 1 = 1 if (OPTARIF[0-2] == "BBR") and (bits 2 to 0 of OPTARIF[3] == 111) and (PTEC == "HPJB" or "HPJW" or "HPJR") (TEMPO Mode, circuit 2 program CHAU 7)<br />• bit 1 = 0 in other cases |


**Comment:**
0 means switch is opened, 1 means switch is closed.

----------------------





#### CurrentDeliveredTier 0x0101
Attribute of cluster 0x070D Daily Schedule:

* Type: 8-bit Enumeration
* Range: {0, 48}
* Access: Read Only
* Reportable: Yes
* Default value / Reset value: 0x01

**Values:**

| **TIC mode**  | **Singlephase**                                              | **Threephase**                                               |
|---------------|--------------------------------------------------------------|--------------------------------------------------------------|
| **STD Conso** | NTARF                                                        | NTARF                                                        |
| **STD Prod**  | NTARF                                                        | NTARF                                                        |
| **HST**       | * 0x01 if PTEC == "TH.." or "HC.." or "HN.." or "HCJB"<br />* 0x02 if PTEC == "HP.." or "PM.." or "HPJB"<br />* 0x03 if PTEC == "HCJW"<br />* 0x04 if PTEC == "HPJW"<br />* 0x05 if PTEC == "HCJR"<br />* 0x06 if PTEC == "HPJR" | * 0x01 if PTEC == "TH.." or "HC.." or "HN.." or "HCJB"<br />* 0x02 if PTEC == "HP.." or "PM.." or "HPJB"<br />* 0x03 if PTEC == "HCJW"<br />* 0x04 if PTEC == "HPJW"<br />* 0x05 if PTEC == "HCJR"<br />* 0x06 if PTEC == "HPJR" |


**Comment:**
Current tier number (1 to 10).

Same as attribute ActiveRegisterTierDelivered of Metering cluster.

----------------------





#### CurrentTierLabel 0x0102
Attribute of cluster 0x070D Daily Schedule:

* Type: Octet String
* Range: {1, 17}
* Access: Read Only
* Reportable: No
* Default value / Reset value: Empty string

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | LTARF           | LTARF          |
| **STD Prod**  | LTARF           | LTARF          |
| **HST**       | PTEC            | PTEC           |


**Comment:**
Label of tier curently in use.

----------------------





#### LinkyPeakPeriodStatus 0x0103
Attribute of cluster 0x070D Daily Schedule:

* Type: 8-bit BitMap
* Range: [0x00, 0xFF]
* Access: Read Only
* Reportable: Yes
* Default value / Reset value: 0x00

**Values:**

| **TIC mode**  | **Singlephase**                                              | **Threephase**                                               |
|---------------|--------------------------------------------------------------|--------------------------------------------------------------|
| **STD Conso** | * bit 0 : STGE bit 24<br />* bit 1 : STGE bit 25<br />* bit 2 : STGE bit 26<br />* bit 3 : STGE bit 27<br />* bit 4 : STGE bit 28<br />* bit 5 : STGE bit 29<br />* bit 6 : STGE bit 30<br />* bit 7 : STGE bit 31 | * bit 0 : STGE bit 24<br />* bit 1 : STGE bit 25<br />* bit 2 : STGE bit 26<br />* bit 3 : STGE bit 27<br />* bit 4 : STGE bit 28<br />* bit 5 : STGE bit 29<br />* bit 6 : STGE bit 30<br />* bit 7 : STGE bit 31 |
| **STD Prod**  | * bit 0 : STGE bit 24<br />* bit 1 : STGE bit 25<br />* bit 2 : STGE bit 26<br />* bit 3 : STGE bit 27<br />* bit 4 : STGE bit 28<br />* bit 5 : STGE bit 29<br />* bit 6 : STGE bit 30<br />* bit 7 : STGE bit 31 | * bit 0 : STGE bit 24<br />* bit 1 : STGE bit 25<br />* bit 2 : STGE bit 26<br />* bit 3 : STGE bit 27<br />* bit 4 : STGE bit 28<br />* bit 5 : STGE bit 29<br />* bit 6 : STGE bit 30<br />* bit 7 : STGE bit 31 |
| **HST**       | * bits 1 and 0 = 01 if PTEC == "HCJB" or "HPJB"<br />* bits 1 and 0 = 10 if PTEC == "HCJW" or "HPJW"<br />* bits 1 and 0 = 11 if PTEC == "HCJR" or "HPJR"<br />* bits 1 and 0 = 00 in other cases<br /><br />* bits 3 and 2 = 01 if DEMAIN is present and DEMAIN == "BLEU"<br />* bits 3 and 2 = 10 if DEMAIN is present and DEMAIN == "BLAN"<br />* bits 3 and 2 = 11 if DEMAIN is present and DEMAIN == "ROUG"<br />* bits 3 and 2 = 00 in other cases<br /><br />* bits 5 and 4 = 01 if PEJP is present<br />* bits 5 and 4 = 00 in other cases<br /><br />* bits 7 and 6 = 01 if PTEC == "PM.."<br />* bits 7 and 6 = 00 in other cases<br /> | * bits 1 and 0 = 01 if PTEC == "HCJB" or "HPJB"<br />* bits 1 and 0 = 10 if PTEC == "HCJW" or "HPJW"<br />* bits 1 and 0 = 11 if PTEC == "HCJR" or "HPJR"<br />* bits 1 and 0 = 00 in other cases<br /><br />* bits 3 and 2 = 01 if DEMAIN is present and DEMAIN == "BLEU"<br />* bits 3 and 2 = 10 if DEMAIN is present and DEMAIN == "BLAN"<br />* bits 3 and 2 = 11 if DEMAIN is present and DEMAIN == "ROUG"<br />* bits 3 and 2 = 00 in other cases<br /><br />* bits 5 and 4 = 01 if PEJP is present<br />* bits 5 and 4 = 00 in other cases<br /><br />* bits 7 and 6 = 01 if PTEC == "PM.."<br />* bits 7 and 6 = 00 in other cases<br /> |


**Comment:**
Indicates:
* The current day color (only for TEMPO contract) : bits 1 and 0
* The next day color (only for TEMPO contract) : bits 3 and 2
* If a peak period is planned : bits 5 and 4
* If a peak period is active : bits 7 and 6


Current day color (bits 1 and 0):
* 00 : not TEMPO contract
* 01 : Low - blue
* 10 : Medium - white
* 11 : High - red


Next day color (bits 3 and 2):
* 00 : unknown or not TEMPO contract
* 01 : Low - blue
* 10 : Medium - white
* 11 : High - red


Peak period prior notice (bits 5 and 4):
* 00 : No peak period is planned
* 01 : Peak period 1 prior notice
* 10 : Peak period 2 prior notice
* 11 : Peak period 3 prior notice


Peak period (bits 7 and 6):
* 00 : Off peak
* 01 : On Peak period 1 
* 10 : On Peak period 2 
* 11 : On Peak period 3 



----------------------





#### PeakStartTime  0x0104
Attribute of cluster 0x070D Daily Schedule:

* Type: UTCTime
* Range: [0x00000000, 0xFFFFFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0xFFFFFFFF

**Values:**

| **TIC mode**  | **Singlephase**                                              | **Threephase**                                               |
|---------------|--------------------------------------------------------------|--------------------------------------------------------------|
| **STD Conso** | * Default value if DPM1 and DPM2 and DPM3 are not present in TIC frame<br />* min (DPM1, DPM2, DPM3) in other cases (next peak period start time) | * Default value if DPM1 and DPM2 and DPM3 are not present in TIC frame<br />* min (DPM1, DPM2, DPM3) in other cases (next peak period start time) |
| **STD Prod**  | * Default value if DPM1 and DPM2 and DPM3 are not present in TIC frame<br />* min (DPM1, DPM2, DPM3) in other cases (next peak period start time) | * Default value if DPM1 and DPM2 and DPM3 are not present in TIC frame<br />* min (DPM1, DPM2, DPM3) in other cases (next peak period start time) |
| **HST**       | Default value                                                | Default value                                                |


**Comment:**
Start time of the next peak period arriving.

----------------------





#### PeakEndTime  0x0105
Attribute of cluster 0x070D Daily Schedule:

* Type: UTCTime
* Range: [0x00000000, 0xFFFFFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0xFFFFFFFF

**Values:**

| **TIC mode**  | **Singlephase**                                              | **Threephase**                                               |
|---------------|--------------------------------------------------------------|--------------------------------------------------------------|
| **STD Conso** | * Default value if DPM1 and DPM2 and DPM3 are not present in TIC frame<br />* FPM1 if PeakStartTime == DPM1<br />* FPM2 if PeakStartTime == DPM2<br />* FPM3 if PeakStartTime == DPM3 | * Default value if DPM1 and DPM2 and DPM3 are not present in TIC frame<br />* FPM1 if PeakStartTime == DPM1<br />* FPM2 if PeakStartTime == DPM2<br />* FPM3 if PeakStartTime == DPM3 |
| **STD Prod**  | * Default value if DPM1 and DPM2 and DPM3 are not present in TIC frame<br />* FPM1 if PeakStartTime == DPM1<br />* FPM2 if PeakStartTime == DPM2<br />* FPM3 if PeakStartTime == DPM3 | * Default value if DPM1 and DPM2 and DPM3 are not present in TIC frame<br />* FPM1 if PeakStartTime == DPM1<br />* FPM2 if PeakStartTime == DPM2<br />* FPM3 if PeakStartTime == DPM3 |
| **HST**       | Default value                                                | Default value                                                |


**Comment:**
End time of the next peak period arriving.

----------------------





#### CurrentTariffLabel 0x0106
Attribute of cluster 0x070D Daily Schedule:

* Type: Octet String
* Range: {1, 25}
* Access: Read Only
* Reportable: No
* Default value / Reset value: Empty string

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | NGTF            | NGTF           |
| **STD Prod**  | NGTF            | NGTF           |
| **HST**       | OPTARIF         | OPTARIF        |


**Comment:**
Label of Tariff (contract name).

----------------------




### Commands

#### PublishSchedule 0x00
Command:

* Client / Server: Server - Generated

**Comment:**
Publish a day schedule for current or next day.

ERL Device shall implement 0x00, 0x01 and 0x06 daily schedule commands. However, it is not mandatory for a client device (example: sleepy device) to support the reception of Daily Schedule server commands generated. In this case, the Client device shall not bound to the server.

If a Daily Schedule client device is able to receive one Schedule command it must support all  Schedule commands.

When Historical TIC Mode is used, DailySchedule commands are not used. If a client device sends a GetSchedule command, the GetSchedule command response will always be "NOT_FOUND".

When Standard TIC Mode is used, Publish Command shall be automatically send to devices bound to the ERL when a next DayProfile’s Schedule is available:

* If the following day profile PJOURF+1 is not the same than the current day profile (ie : NJOURF+1 is different form NJOURF). It is intended that the PublishSchedule command will be send just after midnight one day before. During the first day, when the first connection is done, if a client device is bound to the daily Schedule calendar server, the ERL shall send the PJOURF+1 Schedule instantly. If NJOURF has the same value as NJOURF+1 the PJOURF+1 schedule may be also applied for the current day. 

* If a PPOINTE field appears in the standard TIC, PublishScheduleCommand shall be send.

##### Parameters

###### ProviderID
Command parameter:

* Type: Unsigned 32-bit integer
* Range: [0x00000000, 0xFFFFFFFF]

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | 0x00000000      | 0x00000000     |
| **STD Prod**  | 0x00000000      | 0x00000000     |
| **HST**       | Not applicable  | Not applicable |


**Comment:**
Provider ID

0x00000000 or provider specific

----------------------





###### IssuerEventID
Command parameter:

* Type: Unsigned 32-bit integer
* Range: [0x00000000, 0xFFFFFFFF]

**Values:**

| **TIC mode**  | **Singlephase**                                    | **Threephase**                                     |
|---------------|----------------------------------------------------|----------------------------------------------------|
| **STD Conso** | Timestamp of DATE when a new schedule is published | Timestamp of DATE when a new schedule is published |
| **STD Prod**  | Timestamp of DATE when a new schedule is published | Timestamp of DATE when a new schedule is published |
| **HST**       | Not applicable                                     | Not applicable                                     |


**Comment:**
Value of the TIC Field DATE converted in UTC when the ERL detects that it must publish a new Schedule : 
* When NJOURF+1 is different form NJOURF
* When STGE bits 28 and 29 become non zero.

----------------------





###### ScheduleID
Command parameter:

* Type: Unsigned 32-bit integer
* Range: [0x00000000, 0xFFFFFFFF]

**Values:**

| **TIC mode**  | **Singlephase**                                              | **Threephase**                                               |
|---------------|--------------------------------------------------------------|--------------------------------------------------------------|
| **STD Conso** | If the next schedule is not a peak period: (PJOURF+1)<br />* Current day : NJOURF <br />* Following day : NJOURF+1 <br /><br />If the next Schedule is a peak period: (PPOINTE)<br />* 101(d) if PM1 is used<br />* 102(d) if PM2 is used<br />* 103(d) if PM3 is used | If the next schedule is not a peak period: (PJOURF+1)<br />* Current day : NJOURF <br />* Following day : NJOURF+1<br /><br />If the next Schedule is a peak period: (PPOINTE)<br />* 101(d) if PM1 is used<br />* 102(d) if PM2 is used<br />* 103(d) if PM3 is used |
| **STD Prod**  | If the next schedule is not a peak period: (PJOURF+1)<br />* Current day : NJOURF <br />* Following day : NJOURF+1<br /><br />If the next Schedule is a peak period: (PPOINTE)<br />* 101(d) if PM1 is used<br />* 102(d) if PM2 is used<br />* 103(d) if PM3 is used | If the next schedule is not a peak period: (PJOURF+1)<br />* Current day : NJOURF <br />* Following day : NJOURF+1<br /><br />If the next Schedule is a peak period: (PPOINTE)<br />* 101(d) if PM1 is used<br />* 102(d) if PM2 is used<br />* 103(d) if PM3 is used |
| **HST**       | Not applicable                                               | Not applicable                                               |


**Comment:**
Day reference for the current day or the next day:
* For a non-peak day, day reference can be 1 to 99
* For a peak day, day reference is 100 + mobile peak used (1, 2 or 3)


Mobile peak (PM1, PM2 or PM3) used is the first in the future between DPM1, DPM2 and DPM3.

----------------------





###### DayID
Command parameter:

* Type: Unsigned 16-bit integer
* Range: [0x0000, 0xFFFF]

**Values:**

| **TIC mode**  | **Singlephase**                                              | **Threephase**                                               |
|---------------|--------------------------------------------------------------|--------------------------------------------------------------|
| **STD Conso** | If the next schedule is not a peak period: (PJOURF+1)<br />* Current day : NJOURF <br />* Following day : NJOURF+1<br /><br />If the next Schedule is a peak period: (PPOINTE)<br />* 101(d) if PM1 is used<br />* 102(d) if PM2 is used<br />* 103(d) if PM3 is used | If the next schedule is not a peak period: (PJOURF+1)<br />* Current day : NJOURF <br />* Following day : NJOURF+1<br /><br />If the next Schedule is a peak period: (PPOINTE)<br />* 101(d) if PM1 is used<br />* 102(d) if PM2 is used<br />* 103(d) if PM3 is used |
| **STD Prod**  | If the next schedule is not a peak period: (PJOURF+1)<br />* Current day : NJOURF <br />* Following day : NJOURF+1<br /><br />If the next Schedule is a peak period: (PPOINTE)<br />* 101(d) if PM1 is used<br />* 102(d) if PM2 is used<br />* 103(d) if PM3 is used | If the next schedule is not a peak period: (PJOURF+1)<br />* Current day : NJOURF <br />* Following day : NJOURF+1<br /><br />If the next Schedule is a peak period: (PPOINTE)<br />* 101(d) if PM1 is used<br />* 102(d) if PM2 is used<br />* 103(d) if PM3 is used |
| **HST**       | Not applicable                                               | Not applicable                                               |


**Comment:**
Day reference for the current day or the next day. Same as Schedule ID.
* For a non-peak day, day reference can be 1 to 99
* For a peak day, day reference is 100 + mobile peak used (1, 2 or 3)


Mobile peak (PM1, PM2 or PM3) used is the first in the future between DPM1, DPM2 and DPM3.

----------------------





###### StartTime
Command parameter:

* Type: UTCTime
* Range: [0x00000000, 0xFFFFFFFF]

**Values:**

| **TIC mode**  | **Singlephase**                                              | **Threephase**                                               |
|---------------|--------------------------------------------------------------|--------------------------------------------------------------|
| **STD Conso** | * If the Schedule concerns the current schedule: 0x00000000<br />* If the Schedule concerns the following PJOURF+1 schedule: Tomorrow midnight UTC Time<br />* If the Schedule concerns the following PPOINTE schedule: the first in the future between DPM1 or DPM2 or DPM3 converted in UTC Time<br />* If the Schedule is just after a peak period (PPOINTE), the UTC Start Time is the FPM1 or FPM2 or FPM3 of the just past peak period. | * If the Schedule concerns the current schedule: 0x00000000<br />* If the Schedule concerns the following PJOURF+1 schedule: Tomorrow midnight UTC Time<br />* If the Schedule concerns the following PPOINTE schedule: the first in the future between DPM1 or DPM2 or DPM3 converted in UTC Time<br />* If the Schedule is just after a peak period (PPOINTE), the UTC Start Time is the FPM1 or FPM2 or FPM3 of the just past peak period. |
| **STD Prod**  | * If the Schedule concerns the current schedule: 0x00000000<br />* If the Schedule concerns the following PJOURF+1 schedule: Tomorrow midnight UTC Time<br />* If the Schedule concerns the following PPOINTE schedule: the first in the future between DPM1 or DPM2 or DPM3 converted in UTC Time<br />* If the Schedule is just after a peak period (PPOINTE), the UTC Start Time is the FPM1 or FPM2 or FPM3 of the just past peak period. | * If the Schedule concerns the current schedule: 0x00000000<br />* If the Schedule concerns the following PJOURF+1 schedule: Tomorrow midnight UTC Time<br />* If the Schedule concerns the following PPOINTE schedule: the first in the future between DPM1 or DPM2 or DPM3 converted in UTC Time<br />* If the Schedule is just after a peak period (PPOINTE), the UTC Start Time is the FPM1 or FPM2 or FPM3 of the just past peak period. |
| **HST**       | Not applicable                                               | Not applicable                                               |


**Comment:**
Start time of the published day schedule.

----------------------





###### ScheduleType
Command parameter:

* Type: 8-bit Enumeration
* Range: [0x00, 0xFF]

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | 0x00            | 0x00           |
| **STD Prod**  | 0x00            | 0x00           |
| **HST**       | Not applicable  | Not applicable |


**Comment:**
Type of schedule published.

The ERL interface supports "Linky Schedule" type (0x00).

----------------------





###### ScheduleTimeReference
Command parameter:

* Type: Unsigned 8-bit integer
* Range: [0x00, 0xFF]

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase**  |
|---------------|-----------------|-----------------|
| **STD Conso** | 0x02 Local time | 0x02 Local time |
| **STD Prod**  | 0x02 Local time | 0x02 Local time |
| **HST**       | Not applicable  | Not applicable  |


**Comment:**
Time Reference.

----------------------





###### ScheduleName
Command parameter:

* Type: Octet String
* Range: {1, 13}

**Values:**

| **TIC mode**  | **Singlephase**                                              | **Threephase**                                               |
|---------------|--------------------------------------------------------------|--------------------------------------------------------------|
| **STD Conso** | * If Current day : NJOURF <br />* If Following day : NJOURF+1 <br />* If PPOINTE : "PMx" with x = 1 for PM1, 2 for PM2 and 3 for PM3 | * If Current day : NJOURF <br />* If Following day : NJOURF+1 <br />* If PPOINTE : "PMx" with x = 1 for PM1, 2 for PM2 and 3 for PM3 |
| **STD Prod**  | * If Current day : NJOURF <br />* If Following day : NJOURF+1 <br />* If PPOINTE : "PMx" with x = 1 for PM1, 2 for PM2 and 3 for PM3 | * If Current day : NJOURF <br />* If Following day : NJOURF+1 <br />* If PPOINTE : "PMx" with x = 1 for PM1, 2 for PM2 and 3 for PM3 |
| **HST**       | Not applicable                                               | Not applicable                                               |


**Comment:**
Name of the published day schedule


Mobile peak (PM1, PM2 or PM3) used is the first in the future between DPM1, DPM2 and DPM3.

----------------------





#### GetSchedule 0x00
Command:

* Client / Server: Server - Received

**Comment:**
Request to the ERL interface for getting available day schedules : the current one and / or the next one.

ERL Device shall implement 0x00, 0x01 and 0x05 daily schedule commands. If a Daily Schedule client device is able to receive one Schedule command it must support all  Schedule commands.

Not supported if HST Mode is used.

##### Parameters

###### ProviderID
Command parameter:

* Type: Unsigned 32-bit integer
* Range: [0x00000000, 0xFFFFFFFF]

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | 0x00000000      | 0x00000000     |
| **STD Prod**  | 0x00000000      | 0x00000000     |
| **HST**       | Not applicable  | Not applicable |


**Comment:**
Provider ID.

0x00000000 or provider specific.

----------------------





###### EarliestStartTime
Command parameter:

* Type: UTCTime
* Range: [0x00000000, 0xFFFFFFFF]

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | Client defined  | Client defined |
| **STD Prod**  | Client defined  | Client defined |
| **HST**       | Not applicable  | Not applicable |


**Comment:**
UTC timestamp. The Earliest Start Time parameter is used to indicate from which date the client device wants to retrieve Daily Schedules.


ERL Meter Interface is able to send current Schedule and the following schedule only.

----------------------





###### MinIssuerEventID
Command parameter:

* Type: Unsigned 32-bit integer
* Range: [0x00000000, 0xFFFFFFFF]

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | 0xFFFFFFFF      | 0xFFFFFFFF     |
| **STD Prod**  | 0xFFFFFFFF      | 0xFFFFFFFF     |
| **HST**       | Not applicable  | Not applicable |


**Comment:**
Min Issuer Event ID. Not used by the ERL interface.

----------------------





###### NumberOfSchedules
Command parameter:

* Type: Unsigned 8-bit integer
* Range: [0x00, 0xFF]

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | 0x01 or 0x02    | 0x01 or 0x02   |
| **STD Prod**  | 0x01 or 0x02    | 0x01 or 0x02   |
| **HST**       | Not applicable  | Not applicable |


**Comment:**
Represents the number of schedules requested according to EarliestStartTime and the current and following schedules availability in the ERL interface.

----------------------





###### ScheduleType
Command parameter:

* Type: 8-bit Enumeration
* Range: [0x00, 0xFF]

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | 0X00            | 0X00           |
| **STD Prod**  | 0X00            | 0X00           |
| **HST**       | Not applicable  | Not applicable |


**Comment:**
Schedule type requested by the client. ERL interface supports only "Linky Schedule" type (0x00).

----------------------





#### PublishDayProfile 0x01
Command:

* Client / Server: Server - Generated

**Comment:**
Publish the details of a day profile.

ERL Device shall implement 0x00, 0x01 and 0x06 daily schedule commands. If a Daily Schedule client device is able to receive one Schedule command it must support all  Schedule commands.

Not supported if HST Mode is used.

##### Parameters

###### ProviderID
Command parameter:

* Type: Unsigned 32-bit integer
* Range: [0x00000000, 0xFFFFFFFF]

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | 0x00000000      | 0x00000000     |
| **STD Prod**  | 0x00000000      | 0x00000000     |
| **HST**       | Not applicable  | Not applicable |


**Comment:**
Provider ID

0x00000000 or provider specific

----------------------





###### IssuerEventID
Command parameter:

* Type: Unsigned 32-bit integer
* Range: [0x00000000, 0xFFFFFFFF]

**Values:**

| **TIC mode**  | **Singlephase**                                              | **Threephase**                                               |
|---------------|--------------------------------------------------------------|--------------------------------------------------------------|
| **STD Conso** | Value of the TIC Field DATE when the ERL received the GetDayProfile command. | Value of the TIC Field DATE when the ERL received the GetDayProfile command. |
| **STD Prod**  | Value of the TIC Field DATE when the ERL received the GetDayProfile command. | Value of the TIC Field DATE when the ERL received the GetDayProfile command. |
| **HST**       | Not applicable                                               | Not applicable                                               |


**Comment:**
Issuer Event ID

----------------------





###### DayID
Command parameter:

* Type: Unsigned 16-bit integer
* Range: [0x0000, 0xFFFF]

**Values:**

| **TIC mode**  | **Singlephase**                          | **Threephase**                           |
|---------------|------------------------------------------|------------------------------------------|
| **STD Conso** | Day ID of detailed published day profile | Day ID of detailed published day profile |
| **STD Prod**  | Day ID of detailed published day profile | Day ID of detailed published day profile |
| **HST**       | Not applicable                           | Not applicable                           |


**Comment:**
Day ID received in the GetDayProfile command.

----------------------





###### TotalNumberOfScheduleEntries
Command parameter:

* Type: Unsigned 8-bit integer
* Range: [0x00, 0xFF]

**Values:**

| **TIC mode**  | **Singlephase**                                              | **Threephase**                                               |
|---------------|--------------------------------------------------------------|--------------------------------------------------------------|
| **STD Conso** | * If Current Day :<br />Number of blocks in the current Day Profile stored in the ERL (from H00:00 to H23:59).<br /> <br />* If Following Day: <br />Number of blocks in the Schedule PJOURF+1.<br /><br />* If Peak schedule:<br />Number of blocks in the Day Profile PPOINTE. | * If Current Day:<br />Number of blocks in the current Day Profile stored in the ERL (from H00:00 to H23:59).<br /> <br />* If Following Day: <br />Number of blocks in the Schedule PJOURF+1.<br /><br />* If Peak schedule:<br />Number of blocks in the Day Profile PPOINTE. |
| **STD Prod**  | * If Current Day:<br />Number of blocks in the current Day Profile stored in the ERL (from H00:00 to H23:59).<br /> <br />* If Following Day: <br />Number of blocks in the Schedule PJOURF+1.<br /><br />* If Peak schedule:<br />Number of blocks in the Day Profile PPOINTE. | * If Current Day:<br />Number of blocks in the current Day Profile stored in the ERL (from H00:00 to H23:59).<br /> <br />* If Following Day: <br />Number of blocks in the Schedule PJOURF+1.<br /><br />* If Peak schedule:<br />Number of blocks in the Day Profile PPOINTE. |
| **HST**       | Not applicable                                               | Not applicable                                               |


**Comment:**
A Linky Schedule is composed of 1 to 11 blocks named scheduled entries to describe one day between 00:00 and 23:59. 


Each block provides:
* Start Time in minutes since 00:00 of the day : 1 x unsigned 16-bit integer
* Register tier associated to this period of time : 1 x unsigned 8-bit integer
* Auxiliary Load Switches State : 1 x unsigned 8-bit integer

----------------------





###### CommandIndex
Command parameter:

* Type: Unsigned 8-bit integer
* Range: [0x00, 0xFF]

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | Server defined  | Server defined |
| **STD Prod**  | Server defined  | Server defined |
| **HST**       | Not applicable  | Not applicable |


**Comment:**
For ERL interface, Linky Schedule type usually fits in one command (command index is usually 0).

----------------------





###### TotalNumberOfCommands
Command parameter:

* Type: Unsigned 8-bit integer
* Range: [0x00, 0xFF]

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | Server defined  | Server defined |
| **STD Prod**  | Server defined  | Server defined |
| **HST**       | Not applicable  | Not applicable |


**Comment:**
For ERL interface, Linky Schedule type usually fits in one command (total number of commands is usually 1).

----------------------





###### ScheduleType
Command parameter:

* Type: 8-bit Enumeration
* Range: [0x00, 0xFF]

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | 0x00            | 0x00           |
| **STD Prod**  | 0x00            | 0x00           |
| **HST**       | Not applicable  | Not applicable |


**Comment:**
Type of detailed published schedule.

ERL interface supports only "Linky Schedule" type (0x00).

----------------------





###### DayScheduleEntries
Command parameter:

* Type: List of Schedule Entries
* Range: {1, 11}

**Values:**

| **TIC mode**  | **Singlephase**                                              | **Threephase**                                               |
|---------------|--------------------------------------------------------------|--------------------------------------------------------------|
| **STD Conso** | 1 to 11 Schedule Entries giving details of the published day profile | 1 to 11 Schedule Entries giving details of the published day profile |
| **STD Prod**  | 1 to 11 Schedule Entries giving details of the published day profile | 1 to 11 Schedule Entries giving details of the published day profile |
| **HST**       | Not applicable                                               | Not applicable                                               |


**Comment:**
List of blocks (schedule entries) describing the detailed published day profile. A block contains Start Time in minutes since 00:00, register tier associated to this period of time, and Auxiliary Load Switches State associated to this period of time 


Can be the current day profile, the next day profile or a peak day profile depending of the request.


A Linky Schedule is composed of 1 to 11 blocks named scheduled entries to describe one day between 00:00 and 23:59.


Each block provides :
* Start Time in minutes since 00:00 of the day : 1 x unsigned 16-bit integer
* Register tier associated to this period of time : 1 x unsigned 8-bit integer
* Auxiliary Load Switches State : 1 x unsigned 8-bit integer

----------------------





#### GetDayProfile 0x01
Command:

* Client / Server: Server - Received

**Comment:**
Request to the ERL interface for getting details of a day profile.

ERL Device shall implement 0x00, 0x01 and 0x05 daily schedule commands. If a Daily Schedule client device is able to receive one Schedule command it must support all  Schedule commands.

Not supported if HST Mode is used.

##### Parameters

###### ProviderID
Command parameter:

* Type: Unsigned 32-bit integer
* Range: [0x00000000, 0xFFFFFFFF]

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | 0x00000000      | 0x00000000     |
| **STD Prod**  | 0x00000000      | 0x00000000     |
| **HST**       | Not applicable  | Not applicable |


**Comment:**
Provider ID.

0x00000000 or provider specific.

----------------------





###### DayID
Command parameter:

* Type: Unsigned 16-bit integer
* Range: [0x0000, 0xFFFF]

**Values:**

| **TIC mode**  | **Singlephase**                                              | **Threephase**                                               |
|---------------|--------------------------------------------------------------|--------------------------------------------------------------|
| **STD Conso** | Day ID provided in the Publish Schedule command previously sent by ERL interface | Day ID provided in the Publish Schedule command previously sent by ERL interface |
| **STD Prod**  | Day ID provided in the Publish Schedule command previously sent by ERL interface | Day ID provided in the Publish Schedule command previously sent by ERL interface |
| **HST**       | Not applicable                                               | Not applicable                                               |


**Comment:**
Day ID requested by the client to the ERL interface to retrieve details of the associated day profile.

----------------------





#### GetScheduleCancellation 0x05
Command:

* Client / Server: Server - Received

**Comment:**
This command initiates the return of the last CancelSchedule command held on the associated server. This command has no payload.

ERL Device shall implement 0x00, 0x01 and 0x05 daily schedule commands. If a Daily Schedule client device is able to receive one Schedule command it must support all  Schedule commands.

Not supported if HST Mode is used.


#### CancelAllSchedules 0x06
Command:

* Client / Server: Server - Generated

**Comment:**
Cancel all day schedules already sent.
This command has no payload. The CancelAllSchedules Command is send:
* If the CurrentTariffLabel attribute changes.
* If the TIC Mode switches from Standard Mode to Historical Mode.

In these cases, all Schedules stored by client devices bound to the Daily Schedule ERL Server must be deleted.

ERL Device shall implement 0x00, 0x01 and 0x06 daily schedule commands. If a Daily Schedule client device is able to receive one Schedule command it must support all  Schedule commands.

Not supported if HST Mode is used.

<div style="page-break-after: always;"></div>












##  Meter Identification 0x0b01
This cluster provides attributes and commands for determining advanced information about utility metering device.

* Mandatory / Optional: M

* Client / Server: ( S )



| **Identifier** | **Name**       | **Type**                | **Range**            | **Access** | **Reportable** |
|----------------|----------------|-------------------------|----------------------|------------|----------------|
| 0x0000         | CompanyName    | String                  | {0, 16}              | Read Only  | No             |
| 0x0001         | MeterTypeID    | Unsigned 16-bit integer | [0x0000, 0xFFFF]     | Read Only  | Yes            |
| 0x0004         | DataQualityID  | Unsigned 16-bit integer | [0x0000, 0xFFFF]     | Read Only  | No             |
| 0x0006         | Model          | Octet String            | {0, 16}              | Read Only  | No             |
| 0x000C         | POD            | String                  | {0, 16}              | Read Only  | Yes            |
| 0x000D         | AvailablePower | Signed 24-bit integer   | [0x000000, 0xFFFFFF] | Read Only  | Yes            |
| 0x000E         | PowerThreshold | Signed 24-bit integer   | [0x000000, 0xFFFFFF] | Read Only  | Yes            |


### Attributes

#### CompanyName 0x0000
Attribute of cluster 0x0b01 Meter Identification:

* Type: String
* Range: {0, 16}
* Access: Read Only
* Reportable: No
* Default value / Reset value: Empty string

**Values:**

| **TIC mode**  | **Singlephase**    | **Threephase**     |
|---------------|--------------------|--------------------|
| **STD Conso** | ADSC chars 1 and 2 | ADSC chars 1 and 2 |
| **STD Prod**  | ADSC chars 1 and 2 | ADSC chars 1 and 2 |
| **HST**       | ADCO chars 1 and 2 | ADCO chars 1 and 2 |


**Comment:**
Aims at finding the manufacturer name. Identifiants-Euridis-Liste-CC-TT

----------------------





#### MeterTypeID 0x0001
Attribute of cluster 0x0b01 Meter Identification:

* Type: Unsigned 16-bit integer
* Range: [0x0000, 0xFFFF]
* Access: Read Only
* Reportable: Yes
* Default value / Reset value: 0x0000

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | 0x0000          | 0x0000         |
| **STD Prod**  | 0x0001          | 0x0001         |
| **HST**       | 0x0000          | 0x0000         |


**Comment:**
This field indicates whether the counter is in consumer or producer mode. STGE bit8 implicit.

----------------------





#### DataQualityID 0x0004
Attribute of cluster 0x0b01 Meter Identification:

* Type: Unsigned 16-bit integer
* Range: [0x0000, 0xFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x0003

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | 0x0003          | 0x0003         |
| **STD Prod**  | 0x0003          | 0x0003         |
| **HST**       | 0x0003          | 0x0003         |


**Comment:**
Flag for Not Certified Data.

----------------------





#### Model  0x0006
Attribute of cluster 0x0b01 Meter Identification:

* Type: Octet String
* Range: {0, 16}
* Access: Read Only
* Reportable: No
* Default value / Reset value: Empty string

**Values:**

| **TIC mode**  | **Singlephase**    | **Threephase**     |
|---------------|--------------------|--------------------|
| **STD Conso** | ADSC chars 5 and 6 | ADSC chars 5 and 6 |
| **STD Prod**  | ADSC chars 5 and 6 | ADSC chars 5 and 6 |
| **HST**       | ADCO chars 5 and 6 | ADCO chars 5 and 6 |


**Comment:**
Linky Meter model from serial number (cf. note Enedis 54E).

----------------------





#### POD 0x000C
Attribute of cluster 0x0b01 Meter Identification:

* Type: String
* Range: {0, 16}
* Access: Read Only
* Reportable: Yes
* Default value / Reset value: Empty string

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | PRM             | PRM            |
| **STD Prod**  | PRM             | PRM            |
| **HST**       | 0x00            | 0x00           |


**Comment:**
Point of Delivery (does not exist in historical mode).

----------------------





#### AvailablePower 0x000D
Attribute of cluster 0x0b01 Meter Identification:

* Type: Signed 24-bit integer
* Range: [0x000000, 0xFFFFFF]
* Access: Read Only
* Reportable: Yes
* Default value / Reset value: 0d000000

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase**   |
|---------------|-----------------|------------------|
| **STD Conso** | PREF * 1000     | PREF * 1000      |
| **STD Prod**  | PREF * 1000     | PREF * 1000      |
| **HST**       | ISOUSC * 200    | ISOUSC * 200 * 3 |


**Comment:**
Subscribed power equivalent to historical TIC subscribed current.

----------------------





#### PowerThreshold 0x000E
Attribute of cluster 0x0b01 Meter Identification:

* Type: Signed 24-bit integer
* Range: [0x000000, 0xFFFFFF]
* Access: Read Only
* Reportable: Yes
* Default value / Reset value: 0d36000

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase**   |
|---------------|-----------------|------------------|
| **STD Conso** | PCOUP * 1000    | PCOUP * 1000     |
| **STD Prod**  | PCOUP * 1000    | PCOUP * 1000     |
| **HST**       | ISOUSC * 200    | ISOUSC * 200 * 3 |


**Comment:**
Cutoff power only available with standard TIC.


Cutoffpower can temporarly be lower than the subscribed power. The historical TIC mode would not take into account this change.

----------------------




<div style="page-break-after: always;"></div>












##  Electrical Measurement 0x0b04
This cluster provides a mechanism for querying data about the electrical properties as measured by the device.

* Mandatory / Optional: M

* Client / Server: ( S )



| **Identifier** | **Name**                              | **Type**                | **Range**                | **Access** | **Reportable** |
|----------------|---------------------------------------|-------------------------|--------------------------|------------|----------------|
| 0x0000         | MeasurementType                       | 32-bit Bitmap           | [0x00000000, 0xFFFFFFFF] | Read Only  | No             |
| 0x0304         | TotalActivePower                      | Signed 32-bit integer   | [-8388607, 8388607]      | Read Only  | Yes            |
| 0x0306         | TotalApparentPower                    | Unsigned 32-bit integer | [0x00000000, 0xFFFFFFFF] | Read Only  | Yes            |
| 0x0402         | PowerMultiplier                       | Unsigned 32-bit integer | [0x00000000, 0xFFFFFFFF] | Read Only  | No             |
| 0x0403         | PowerDivisor                          | Unsigned 32-bit integer | [0x00000000, 0xFFFFFFFF] | Read Only  | No             |
| 0x0505         | RMSVoltage                            | Unsigned 16-bit integer | [0x0000, 0xFFFF]         | Read Only  | Yes            |
| 0x0508         | RMSCurrent                            | Unsigned 16-bit integer | [0x0000, 0xFFFF]         | Read Only  | Yes            |
| 0x050B         | ActivePower                           | Signed 16-bit integer   | [-32768, 32767]          | Read Only  | Yes            |
| 0x050F         | ApparentPower                         | Unsigned 16-bit integer | [0x0000, 0xFFFF]         | Read Only  | Yes            |
| 0x0511         | AverageRMSVoltageMeasurementPeriod    | Unsigned 16-bit integer | [0x0000, 0xFFFF]         | Read Write | No             |
| 0x0600         | ACVoltageMultiplier                   | Unsigned 16-bit integer | [0x0001, 0xFFFF]         | Read Only  | No             |
| 0x0601         | ACVoltageDivisor                      | Unsigned 16-bit integer | [0x0001, 0xFFFF]         | Read Only  | No             |
| 0x0602         | ACCurrentMultiplier                   | Unsigned 16-bit integer | [0x0001, 0xFFFF]         | Read Only  | No             |
| 0x0603         | ACCurrentDivisor                      | Unsigned 16-bit integer | [0x0001, 0xFFFF]         | Read Only  | No             |
| 0x0604         | ACPowerMultiplier                     | Unsigned 16-bit integer | [0x0001, 0xFFFF]         | Read Only  | No             |
| 0x0605         | ACPowerDivisor                        | Unsigned 16-bit integer | [0x0001, 0xFFFF]         | Read Only  | No             |
| 0x0905         | RMSVoltagePhB                         | Unsigned 16-bit integer | [0x0000, 0xFFFF]         | Read Only  | Yes            |
| 0x0908         | RMSCurrentPhB                         | Unsigned 16-bit integer | [0x0000, 0xFFFF]         | Read Only  | Yes            |
| 0x090B         | ActivePowerPhB                        | Signed 16-bit integer   | [-32768, 32767]          | Read Only  | Yes            |
| 0x090F         |  ApparentPowerPhB                     | Unsigned 16-bit integer | [0x0000, 0xFFFF]         | Read Only  | Yes            |
| 0x0911         | AverageRMSVoltageMeasurementPeriodPhB | Unsigned 16-bit integer | [0x0000, 0xFFFF]         | Read Write | No             |
| 0x0A05         | RMSVoltagePhC                         | Unsigned 16-bit integer | [0x0000, 0xFFFF]         | Read Only  | Yes            |
| 0x0A08         | RMSCurrentPhC                         | Unsigned 16-bit integer | [0x0000, 0xFFFF]         | Read Only  | Yes            |
| 0x0A0B         | ActivePowerPhC                        | Signed 16-bit integer   | [-32768, 32767]          | Read Only  | Yes            |
| 0x0A0F         | ApparentPowerPhC                      | Unsigned 16-bit integer | [0x0000, 0xFFFF]         | Read Only  | Yes            |
| 0x0A11         | AverageRMSVoltageMeasurementPeriodPhC | Unsigned 16-bit integer | [0x0000, 0xFFFF]         | Read Write | No             |


### Attributes

#### MeasurementType 0x0000
Attribute of cluster 0x0b04 Electrical Measurement:

* Type: 32-bit Bitmap
* Range: [0x00000000, 0xFFFFFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x00000000

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | 0x0000000D      | 0x0000003D     |
| **STD Prod**  | 0x0000000D      | 0x0000003D     |
| **HST**       | 0x0000000D      | 0x0000003D     |


**Comment:**
In STD Mode, if IRMS2 is present in TIC frame, three phases. Else, single phase.


In HST Mode, if IINST2 is present in TIC frame, three phases. Else, single phase.

----------------------





#### TotalActivePower 0x0304
Attribute of cluster 0x0b04 Electrical Measurement:

* Type: Signed 32-bit integer
* Range: [-8388607, 8388607]
* Access: Read Only
* Reportable: Yes
* Default value / Reset value: 0x00000000

**Values:**

| **TIC mode**  | **Singlephase**                                       | **Threephase**                                        |
|---------------|-------------------------------------------------------|-------------------------------------------------------|
| **STD Conso** | SINSTS                                                | SINSTS                                                |
| **STD Prod**  | SINSTS if STGE bit9 == 0 or -SINSTI if STGE bit9 == 1 | SINSTS if STGE bit9 == 0 or -SINSTI if STGE bit9 == 1 |
| **HST**       | PAPP                                                  | PAPP                                                  |


**Comment:**
Total active power (in W) consumed (positive) or produced (negative) by smart meter.


The TIC does not transmit instantaneous active power but instantaneous apparent power.

----------------------





#### TotalApparentPower 0x0306
Attribute of cluster 0x0b04 Electrical Measurement:

* Type: Unsigned 32-bit integer
* Range: [0x00000000, 0xFFFFFFFF]
* Access: Read Only
* Reportable: Yes
* Default value / Reset value: 0x00000000

**Values:**

| **TIC mode**  | **Singlephase**                                      | **Threephase**                                       |
|---------------|------------------------------------------------------|------------------------------------------------------|
| **STD Conso** | SINSTS                                               | SINSTS                                               |
| **STD Prod**  | SINSTS if STGE bit9 == 0 or SINSTI if STGE bit9 == 1 | SINSTS if STGE bit9 == 0 or SINSTI if STGE bit9 == 1 |
| **HST**       | PAPP                                                 | PAPP                                                 |


**Comment:**
Total apparent power (in VA) seen by smart meter. An apparent power is always positive.

----------------------





#### PowerMultiplier 0x0402
Attribute of cluster 0x0b04 Electrical Measurement:

* Type: Unsigned 32-bit integer
* Range: [0x00000000, 0xFFFFFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x00000001

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | Default value   | Default value  |
| **STD Prod**  | Default value   | Default value  |
| **HST**       | Default value   | Default value  |


**Comment:**
Power multiplier.

----------------------





#### PowerDivisor 0x0403
Attribute of cluster 0x0b04 Electrical Measurement:

* Type: Unsigned 32-bit integer
* Range: [0x00000000, 0xFFFFFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x00000001

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | Default value   | Default value  |
| **STD Prod**  | Default value   | Default value  |
| **HST**       | Default value   | Default value  |


**Comment:**
Power divisor.

----------------------





#### RMSVoltage 0x0505
Attribute of cluster 0x0b04 Electrical Measurement:

* Type: Unsigned 16-bit integer
* Range: [0x0000, 0xFFFF]
* Access: Read Only
* Reportable: Yes
* Default value / Reset value: 0xFFFF

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | URMS1           | URMS1          |
| **STD Prod**  | URMS1           | URMS1          |
| **HST**       | Default value   | Default value  |


**Comment:**
RMS voltage in STD Mode only (Single phase).

RMS voltage phase A in STD Mode only (Three phases).

----------------------





#### RMSCurrent 0x0508
Attribute of cluster 0x0b04 Electrical Measurement:

* Type: Unsigned 16-bit integer
* Range: [0x0000, 0xFFFF]
* Access: Read Only
* Reportable: Yes
* Default value / Reset value: 0xFFFF

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | IRMS1           | IRMS1          |
| **STD Prod**  | IRMS1           | IRMS1          |
| **HST**       | IINST           | IINST1         |


**Comment:**
RMS current (single phase).

RMS current phase A (three phases).

----------------------





#### ActivePower 0x050B
Attribute of cluster 0x0b04 Electrical Measurement:

* Type: Signed 16-bit integer
* Range: [-32768, 32767]
* Access: Read Only
* Reportable: Yes
* Default value / Reset value: 0xFFFF

**Values:**

| **TIC mode**  | **Singlephase**                                        | **Threephase**                                        |
|---------------|--------------------------------------------------------|-------------------------------------------------------|
| **STD Conso** | SINSTS                                                 | SINSTS1                                               |
| **STD Prod**  | SINSTS if STGE bit9 == 0 or  -SINSTI if STGE bit9 == 1 | SINSTS1 if SINSTS1 > 0<br />URMS1 x -IRMS1 if SINSTS1 == 0 |
| **HST**       | PAPP                                                   | 200 x IINST1                                          |


**Comment:**
Active power (in W) on phase A in three phases.

Equal to TotalActivePower in single phase.

Positive for consumption, negative for production.

----------------------





#### ApparentPower 0x050F
Attribute of cluster 0x0b04 Electrical Measurement:

* Type: Unsigned 16-bit integer
* Range: [0x0000, 0xFFFF]
* Access: Read Only
* Reportable: Yes
* Default value / Reset value: 0xFFFF

**Values:**

| **TIC mode**  | **Singlephase**                                       | **Threephase**                                       |
|---------------|-------------------------------------------------------|------------------------------------------------------|
| **STD Conso** | SINSTS                                                | SINSTS1                                              |
| **STD Prod**  | SINSTS if STGE bit9 == 0 or  SINSTI if STGE bit9 == 1 | SINSTS1 if SINSTS1 > 0<br />URMS1 x IRMS1 if SINSTS1 == 0 |
| **HST**       | PAPP                                                  | 200 x IINST1                                         |


**Comment:**
Apparent power (in VA) on phase A if three phases.

Equal to TotalApparentPower if single phase.

Apparent power is always positive.

----------------------





#### AverageRMSVoltageMeasurementPeriod 0x0511
Attribute of cluster 0x0b04 Electrical Measurement:

* Type: Unsigned 16-bit integer
* Range: [0x0000, 0xFFFF]
* Access: Read Write
* Reportable: No
* Default value / Reset value: 0x0000

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | 1               | 1              |
| **STD Prod**  | 1               | 1              |
| **HST**       | Default value   | Default value  |


**Comment:**
Average RMS Voltage Measurement Period.

----------------------





#### ACVoltageMultiplier 0x0600
Attribute of cluster 0x0b04 Electrical Measurement:

* Type: Unsigned 16-bit integer
* Range: [0x0001, 0xFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x0001

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | Default value   | Default value  |
| **STD Prod**  | Default value   | Default value  |
| **HST**       | Default value   | Default value  |


----------------------





#### ACVoltageDivisor 0x0601
Attribute of cluster 0x0b04 Electrical Measurement:

* Type: Unsigned 16-bit integer
* Range: [0x0001, 0xFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x0001

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | Default value   | Default value  |
| **STD Prod**  | Default value   | Default value  |
| **HST**       | Default value   | Default value  |


----------------------





#### ACCurrentMultiplier 0x0602
Attribute of cluster 0x0b04 Electrical Measurement:

* Type: Unsigned 16-bit integer
* Range: [0x0001, 0xFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x0001

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | Default value   | Default value  |
| **STD Prod**  | Default value   | Default value  |
| **HST**       | Default value   | Default value  |


----------------------





#### ACCurrentDivisor 0x0603
Attribute of cluster 0x0b04 Electrical Measurement:

* Type: Unsigned 16-bit integer
* Range: [0x0001, 0xFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x0001

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | Default value   | Default value  |
| **STD Prod**  | Default value   | Default value  |
| **HST**       | Default value   | Default value  |


----------------------





#### ACPowerMultiplier 0x0604
Attribute of cluster 0x0b04 Electrical Measurement:

* Type: Unsigned 16-bit integer
* Range: [0x0001, 0xFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x0001

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | Default value   | Default value  |
| **STD Prod**  | Default value   | Default value  |
| **HST**       | Default value   | Default value  |


----------------------





#### ACPowerDivisor 0x0605
Attribute of cluster 0x0b04 Electrical Measurement:

* Type: Unsigned 16-bit integer
* Range: [0x0001, 0xFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x0001

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | Default value   | Default value  |
| **STD Prod**  | Default value   | Default value  |
| **HST**       | Default value   | Default value  |


----------------------





#### RMSVoltagePhB 0x0905
Attribute of cluster 0x0b04 Electrical Measurement:

* Type: Unsigned 16-bit integer
* Range: [0x0000, 0xFFFF]
* Access: Read Only
* Reportable: Yes
* Default value / Reset value: 0xFFFF

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | Default value   | URMS2          |
| **STD Prod**  | Default value   | URMS2          |
| **HST**       | Default value   | Default value  |


**Comment:**
RMS voltage phase B, only in STD Mode and three phases.

----------------------





#### RMSCurrentPhB 0x0908
Attribute of cluster 0x0b04 Electrical Measurement:

* Type: Unsigned 16-bit integer
* Range: [0x0000, 0xFFFF]
* Access: Read Only
* Reportable: Yes
* Default value / Reset value: 0xFFFF

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | Default value   | IRMS2          |
| **STD Prod**  | Default value   | IRMS2          |
| **HST**       | Default value   | IINST2         |


**Comment:**
RMS current phase B for three phases.

----------------------





#### ActivePowerPhB 0x090B
Attribute of cluster 0x0b04 Electrical Measurement:

* Type: Signed 16-bit integer
* Range: [-32768, 32767]
* Access: Read Only
* Reportable: Yes
* Default value / Reset value: 0x8000

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase**                                        |
|---------------|-----------------|-------------------------------------------------------|
| **STD Conso** | Default value   | SINSTS2                                               |
| **STD Prod**  | Default value   | SINSTS2 if SINSTS2 > 0<br />URMS2 x -IRMS2 if SINSTS2 == 0 |
| **HST**       | Default value   | 200 x IINST2                                          |


**Comment:**
Active power (in W) of phase B. Only for three phases.

Positive for consumption, negative for production.

----------------------





####  ApparentPowerPhB 0x090F
Attribute of cluster 0x0b04 Electrical Measurement:

* Type: Unsigned 16-bit integer
* Range: [0x0000, 0xFFFF]
* Access: Read Only
* Reportable: Yes
* Default value / Reset value: 0xFFFF

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase**                                        |
|---------------|-----------------|-------------------------------------------------------|
| **STD Conso** | Default value   | SINSTS2                                               |
| **STD Prod**  | Default value   | SINSTS2 if SINSTS2 > 0<br />URMS2 x IRMS2 if  SINSTS2 == 0 |
| **HST**       | Default value   | 200 x IINST2                                          |


**Comment:**
Apparent power (in VA) of phase B. Only for three phases.

Apparent power is always positive.

----------------------





#### AverageRMSVoltageMeasurementPeriodPhB 0x0911
Attribute of cluster 0x0b04 Electrical Measurement:

* Type: Unsigned 16-bit integer
* Range: [0x0000, 0xFFFF]
* Access: Read Write
* Reportable: No
* Default value / Reset value: 0x0000

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | 1               | 1              |
| **STD Prod**  | 1               | 1              |
| **HST**       | Default value   | Default value  |


**Comment:**
Average RMS Voltage Measurement Period phase B.

----------------------





#### RMSVoltagePhC 0x0A05
Attribute of cluster 0x0b04 Electrical Measurement:

* Type: Unsigned 16-bit integer
* Range: [0x0000, 0xFFFF]
* Access: Read Only
* Reportable: Yes
* Default value / Reset value: 0xFFFF

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | Default value   | URMS3          |
| **STD Prod**  | Default value   | URMS3          |
| **HST**       | Default value   | Default value  |


**Comment:**
RMS voltage phase C, only in STD Mode and three phases.

----------------------





#### RMSCurrentPhC 0x0A08
Attribute of cluster 0x0b04 Electrical Measurement:

* Type: Unsigned 16-bit integer
* Range: [0x0000, 0xFFFF]
* Access: Read Only
* Reportable: Yes
* Default value / Reset value: 0xFFFF

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | Default value   | IRMS3          |
| **STD Prod**  | Default value   | IRMS3          |
| **HST**       | Default value   | IINST3         |


**Comment:**
RMS current phase C for three phases.

----------------------





#### ActivePowerPhC 0x0A0B
Attribute of cluster 0x0b04 Electrical Measurement:

* Type: Signed 16-bit integer
* Range: [-32768, 32767]
* Access: Read Only
* Reportable: Yes
* Default value / Reset value: 0x8000

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase**                                        |
|---------------|-----------------|-------------------------------------------------------|
| **STD Conso** | Default value   | SINSTS3                                               |
| **STD Prod**  | Default value   | SINSTS3 if SINSTS3 > 0<br />URMS3 x -IRMS3 if SINSTS3 == 0 |
| **HST**       | Default value   | 200 x IINST3                                          |


**Comment:**
Active power (in W) of phase C. Only for three phases.

Positive for consumption, negative for production.

----------------------





#### ApparentPowerPhC 0x0A0F
Attribute of cluster 0x0b04 Electrical Measurement:

* Type: Unsigned 16-bit integer
* Range: [0x0000, 0xFFFF]
* Access: Read Only
* Reportable: Yes
* Default value / Reset value: 0xFFFF

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase**                                        |
|---------------|-----------------|-------------------------------------------------------|
| **STD Conso** | Default value   | SINSTS3                                               |
| **STD Prod**  | Default value   | SINSTS3 if SINSTS3 > 0<br />URMS3 x IRMS3 if  SINSTS3 == 0 |
| **HST**       | Default value   | 200 x IINST3                                          |


**Comment:**
Apparent power (in VA) of phase C. Only for three phases.

Apparent power is always positive.

----------------------





#### AverageRMSVoltageMeasurementPeriodPhC 0x0A11
Attribute of cluster 0x0b04 Electrical Measurement:

* Type: Unsigned 16-bit integer
* Range: [0x0000, 0xFFFF]
* Access: Read Write
* Reportable: No
* Default value / Reset value: 0x0000

**Values:**

| **TIC mode**  | **Singlephase** | **Threephase** |
|---------------|-----------------|----------------|
| **STD Conso** | 1               | 1              |
| **STD Prod**  | 1               | 1              |
| **HST**       | Default value   | Default value  |


**Comment:**
Average RMS Voltage Measurement Period phase C.

----------------------




<div style="page-break-after: always;"></div>












##  Diagnostic 0x0b05
The diagnostics cluster provides access to information regarding the operation of the stack over time. This information is useful to installers and other network administrators who wish to know how a particular device is functioning on the network.

* Mandatory / Optional: M

* Client / Server: ( S )



| **Identifier** | **Name**        | **Type**                | **Range**        | **Access** | **Reportable** |
|----------------|-----------------|-------------------------|------------------|------------|----------------|
| 0x0000         | NumberOfResets  | Unsigned 16-bit integer | [0x0000, 0xFFFF] | Read Only  | No             |
| 0x011C         | LastMessageLQI  | Unsigned 8-bit integer  | [0x00, 0xFF]     | Read Only  | No             |
| 0x011D         | LastMessageRSSI | Signed 8-bit integer    | [-127, 127]      | Read Only  | No             |


### Attributes

#### NumberOfResets 0x0000
Attribute of cluster 0x0b05 Diagnostic:

* Type: Unsigned 16-bit integer
* Range: [0x0000, 0xFFFF]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x0000

**Comment:**
Number of reset stored in non volatile Memory.

----------------------





#### LastMessageLQI 0x011C
Attribute of cluster 0x0b05 Diagnostic:

* Type: Unsigned 8-bit integer
* Range: [0x00, 0xFF]
* Access: Read Only
* Reportable: No

**Comment:**
Link quality indicator of the last message received (no standard agreement for calculating LQI).

----------------------





#### LastMessageRSSI 0x011D
Attribute of cluster 0x0b05 Diagnostic:

* Type: Signed 8-bit integer
* Range: [-127, 127]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0

**Comment:**
Received signal strenght indication for the last message received.

----------------------




<div style="page-break-after: always;"></div>












##  Global attributes
The ClusterRevision global attribute is mandatory for all cluster instances, client and server, conforming to ZCL revision 6 (ZCL6) and later ZCL revisions.

* Mandatory / Optional: M

* Client / Server: ( C&S )



| **Identifier** | **Name**        | **Type**                | **Range**        | **Access** | **Reportable** |
|----------------|-----------------|-------------------------|------------------|------------|----------------|
| 0xFFFD         | ClusterRevision | Unsigned 16-bit integer | [0x0000, 0xFFFE] | Read Only  | No             |


### Attributes

#### ClusterRevision 0xFFFD
Attribute of cluster attributes Global:

* Type: Unsigned 16-bit integer
* Range: [0x0000, 0xFFFE]
* Access: Read Only
* Reportable: No
* Default value / Reset value: 0x0000

**Comment:**
The ClusterRevision global attribute is mandatory for all cluster instances, client and server, conforming to ZCL revision 6 (ZCL6) and later ZCL revisions.

----------------------




