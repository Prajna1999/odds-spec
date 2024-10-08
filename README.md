# Detailed Open Flood Data Standard Documentation

Version 2.1

## Table of Contents

1. [Introduction](#1-introduction)
2. [Metadata](#2-metadata)
3. [Hazard](#3-hazard)
4. [Exposure](#4-exposure)
5. [Vulnerability](#5-vulnerability)
6. [Impact](#6-impact)
7. [Response](#7-response)
8. [Recovery](#8-recovery)
9. [Data Collection](#9-data-collection)

## 1. Introduction

The Open Flood Data Standard (OFDS) provides a comprehensive framework for collecting, organizing, and sharing flood event data. This expanded version includes more detailed field types and additional subcategories to capture a wider range of flood-related information.

## 2. Metadata

| Field | Type | Description |
|-------|------|-------------|
| standard_version | string | Version of the OFDS used |
| uid | string | Unique identifier for the dataset |
| title | string | Brief description of the event |
| collected_by | object | Information about the data collector |
| collection_date | datetime | Date and time of data collection |
| published_date | datetime | Date and time of data publication |
| published_by | object | Information about the publishing organization |
| license | string | License under which the data is published |
| data_quality | object | Metrics describing the quality of the data |
| notes | string | Additional relevant information |
| methodology_url | string | URL to detailed methodology description |
| version_history | array of objects | List of previous versions and changes |

## 3. Hazard

| Field | Type | Description |
|-------|------|-------------|
| id | string | Unique identifier for the hazard event |
| peril_type | string | Type of hazard (e.g., "Flood") |
| sub_type | string | Specific type of flood |
| secondary_hazards | array of objects | List of secondary hazards triggered by the flood |
| event | object | Details about the flood event |
| affected_area | object | Geographic information about the affected area |
| intensity | object | Measures of flood intensity |
| duration | object | Duration of the flood event |
| return_period | object | Estimated return period of the event |
| flood_cause | string | Primary cause of flooding (e.g., "Heavy rainfall", "Dam failure") |
| historical_context | object | Comparison to previous flood events |

## 4. Exposure

| Field | Type | Description |
|-------|------|-------------|
| pre_event | object | Pre-event exposure data |
| population | object | Population statistics |
| - total | number | Total population in affected area |
| - density | object | Population density |
| - vulnerable_groups | object | Breakdown of vulnerable populations |
| -- elderly | number | Number of elderly people (e.g., 65+) |
| -- children | number | Number of children (e.g., under 18) |
| -- disabled | number | Number of people with disabilities |
| -- low_income | number | Number of people below poverty line |
| buildings | object | Building inventory |
| - residential | object | Residential building data |
| - commercial | object | Commercial building data |
| - industrial | object | Industrial building data |
| critical_infrastructure | object | Count of critical facilities |
| - hospitals | number | Number of hospitals |
| - schools | number | Number of schools |
| - power_plants | number | Number of power plants |
| - water_treatment | number | Number of water treatment facilities |
| agriculture | object | Agricultural land use data |
| - crop_types | array of objects | List of main crop types and areas |
| transportation | object | Transportation infrastructure |
| - roads | object | Road network data |
| - railways | object | Railway network data |
| - airports | object | Airport facilities |

## 5. Vulnerability

| Field | Type | Description |
|-------|------|-------------|
| building_vulnerability | object | Vulnerability functions for different building types |
| - residential | object | Vulnerability function for residential buildings |
| - commercial | object | Vulnerability function for commercial buildings |
| - industrial | object | Vulnerability function for industrial buildings |
| crop_vulnerability | object | Vulnerability functions for crops |
| infrastructure_vulnerability | object | Vulnerability functions for infrastructure |
| social_vulnerability | object | Indicators of social vulnerability |
| - poverty_rate | number | Percentage of population below poverty line |
| - literacy_rate | number | Percentage of literate population |
| - access_to_healthcare | number | Percentage with easy access to healthcare |
| - social_cohesion_index | number | Index measuring community cohesion |

## 6. Impact

| Field | Type | Description |
|-------|------|-------------|
| human | object | Human casualties and displacement |
| - fatalities | object | Death toll information |
| - injured | object | Injury information |
| - missing | object | Missing persons information |
| - displaced | object | Displacement information |
| buildings | object | Damage to buildings |
| - residential | object | Damage to residential buildings |
| - commercial | object | Damage to commercial buildings |
| - industrial | object | Damage to industrial buildings |
| infrastructure | object | Damage to infrastructure |
| - transportation | object | Damage to transportation infrastructure |
| - utilities | object | Damage to utility infrastructure |
| agriculture | object | Agricultural losses |
| - crops | object | Crop damage information |
| - livestock | object | Livestock losses |
| economic | object | Direct and indirect economic losses |
| - direct_losses | object | Immediate economic losses |
| - indirect_losses | object | Long-term economic impacts |
| social | object | Social impacts |
| - education | object | Impact on education system |
| - health | object | Impact on health services |
| - cultural_heritage | object | Damage to cultural sites |
| environment | object | Environmental impacts |
| - ecosystems | object | Impact on ecosystems |
| - water_quality | object | Effects on water quality |
| - soil_erosion | object | Soil erosion data |

## 7. Response

| Field | Type | Description |
|-------|------|-------------|
| early_warning | object | Information about early warning systems |
| - warning_issued_date | datetime | Date and time warning was issued |
| - lead_time | object | Warning lead time |
| - dissemination_coverage | number | Percentage of population reached |
| emergency_response | object | Details of emergency response operations |
| - resources_deployed | object | Resources used in response |
| - response_time | object | Time taken to initiate response |
| evacuation | object | Evacuation statistics |
| - total_evacuated | number | Number of people evacuated |
| - evacuation_routes | array of objects | Information on evacuation routes |
| temporary_housing | object | Temporary housing provisions |
| relief_distribution | object | Distribution of relief supplies |
| - food | object | Food aid distribution |
| - water | object | Clean water distribution |
| - medical_supplies | object | Medical supply distribution |
| debris_removal | object | Debris removal operations |
| search_and_rescue | object | Search and rescue operations data |

## 8. Recovery

| Field | Type | Description |
|-------|------|-------------|
| short_term | object | Immediate recovery activities |
| - infrastructure_restoration | object | Temporary infrastructure repairs |
| - emergency_shelter | object | Emergency shelter provisions |
| long_term | object | Long-term reconstruction and restoration efforts |
| - housing_reconstruction | object | Permanent housing reconstruction |
| - livelihood_restoration | object | Programs to restore livelihoods |
| - infrastructure_improvement | object | Long-term infrastructure upgrades |
| build_back_better | object | Initiatives to improve resilience |
| - flood_resilient_structures | object | Flood-resistant building initiatives |
| - improved_drainage | object | Drainage system improvements |
| economic_recovery | object | Economic recovery programs |
| psychological_support | object | Mental health and support programs |

## 9. Data Collection

| Field | Type | Description |
|-------|------|-------------|
| methodology | array of objects | List of data collection methods used |
| - type | string | Type of data collection method |
| - description | string | Description of the method |
| - accuracy | object | Accuracy metrics of the method |
| update_frequency | string | Frequency of data updates |
| limitations | string | Known limitations of the data collection process |
| data_sources | array of objects | List of data sources |
| quality_control | object | Quality control measures applied |
| gaps | array of strings | Identified gaps in data collection |