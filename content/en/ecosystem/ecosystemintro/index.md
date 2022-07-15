---
title: "sdmx.io ecosystem"
description: ""
date: 2022-07-14T00:00:00+00:00
draft: false
tags: ["ecosystem"]
categories: ["tools"]
---
# The sdmx.io ecosystem
The sdmx.io ecosystem is a collection of open source SDMX software tools cooperating to solve official statisics use cases.

{{< figure src="sdmxio-ecosystem-20220714.jpg" width="80%">}}

# Fusion Metadata Registry

Fusion Metadata Registry (FMR) is first and foremost a **structural metadata registry** - essentially a **database designed specifically for storing SDMX artefacts** including Concepts, Codelists and Data Structure definitions. A centralised and controlled repository for metadata is useful in many cases where statistics are collected, produced and exchanged\
How?
- sharing and re-use
- standardisation 
- harmonisation of concepts helps to make datasets comparable and consistent
- by enabling metadata and data governance

In additional to it's role as a place to store, centralise and control structures, FMR provides several additional features:

Web user interface for creating and maintaining SDMX structure artefacts
: FMR's web user interface gives metadata managers a graphical way to explore the registry's content, create new structures and maintain / modify existing structures. Many artefacts can be exported to Excel, modified and reloaded - particularly useful for maintaining large Codelists.

{{< figure src="fmr-ui-codelists.jpg" width="80%">}}

Data validation
: For both data collection and data reporting use cases, FMR supports validation of datasets for compliance with the DSD and any defined constraints. Checking data quality helps to deliver effective data governance and improves the efficiency of data exchanges, avoiding the costly re-processing or re-transmission.

FMR applies nine standard validation rules:

| **Rule**                     | **Test Applied**                                                               |
| ---------------------------- | ------------------------------------------------------------------------------ | 
| Semantically compliant       | The XML, JSON, CSV or Excel is well formed                                     |
| Duplicate observations       | Uniqueness - there is only one observation value reported for each time period |
| Mandatory attributes         | All mandatory attributes are reported                                          |
| Obs status                   | [OBS_STATUS](https://registry.sdmx.org/ws/public/sdmxapi/rest/codelist/SDMX/CL_OBS_STATUS/2.2) is consistent with the observation value |
| Time period format           | E.g. FREQ=M means the TIME_PERIOD format must be YYYY-MM                       |
| Valid calculations           | Balance equalities defined used Validation Schemes                             |
| Valid constraints            | The data is within the universe defined by *Data Constraints*                  |
| Valid representation         | Each component complies with the *representation* defined in the DSD           |
| Valid structure              | The dimensions and attributes are consistent with the DSD                      |

Conversion of SDMX data between transmission formats
: Data collectors sometimes require data to be submitted in a specific format such as SDMX-ML 2.1 *structure specific*. FMR will perform that conversion.

[More about FMR](../fmr)

# FusionXL

