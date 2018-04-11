---
title: Event ID 12 - RegistryEvent (Object create and delete)
description: Registry key and value create and delete operations map to this event type.
log.type: sysmon
sysmon.version: 7.01
sysmon.rule: RegistryEvent
author: Roberto Rodriguez (@Cyb3rWard0g)
date: 04/11/2018
---

# Event ID 12: RegistryEvent (Object create and delete)

## Description
Registry key and value create and delete operations map to this event type, which can be useful for monitoring for changes to Registry autostart locations, or specific malware registry modifications.[Sysmon Source](https://docs.microsoft.com/en-us/sysinternals/downloads/sysmon#event-id-12-registryevent-object-create-and-delete)

## Event Log Illustration

![alt text](/resources/images/event-12.png "Event 12 illustration")

## Event XML

```
<Event xmlns="http://schemas.microsoft.com/win/2004/08/events/event">
  <System>
    <Provider Name="Microsoft-Windows-Sysmon" Guid="{5770385F-C22A-43E0-BF4C-06F5698FFBD9}" /> 
    <EventID>12</EventID> 
    <Version>2</Version> 
    <Level>4</Level> 
    <Task>12</Task> 
    <Opcode>0</Opcode> 
    <Keywords>0x8000000000000000</Keywords> 
    <TimeCreated SystemTime="2018-04-11T06:02:54.827237700Z" /> 
    <EventRecordID>11761339</EventRecordID> 
    <Correlation /> 
    <Execution ProcessID="6028" ThreadID="4132" /> 
    <Channel>Microsoft-Windows-Sysmon/Operational</Channel> 
    <Computer>DESKTOP-WARDOG</Computer> 
    <Security UserID="S-1-5-18" /> 
  </System>
  <EventData>
    <Data Name="EventType">CreateKey</Data> 
    <Data Name="UtcTime">2018-04-11 06:02:54.817</Data> 
    <Data Name="ProcessGuid">{A98268C1-9595-5ACD-0000-0010C2380200}</Data> 
    <Data Name="ProcessId">2052</Data> 
    <Data Name="Image">C:\Program Files\Common Files\Microsoft Shared\ClickToRun\OfficeClickToRun.exe</Data> 
    <Data Name="TargetObject">HKU\.DEFAULT\Software\Microsoft\Office\16.0\Common</Data> 
  </EventData>
</Event>
```