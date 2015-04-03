---
layout: with-sidebar
title: Service Connect Schema
type: schema
---

_Updated July 2014_

## Data Attributes

A dataset containing these attributes powers the Service Connect app.  While several fields are optional, they greatly improve the user experience for both citizen users and administrators.  

An example can be found [here](https://scs.demo.socrata.com/Government/NOLA-311-App-Data/kdi4-pasu).  

| Attribute                             | API Field                          | Type        | Required | Role within app                     |
| ---                                   | ---                                | ---         | ---      | ---                                 |
| Ticket ID                             | `ticket_id`                        | Plain Text  | Yes      | Unique ID, search                   |
| Issue Type                            | `issue_type`                       | Plain Text  | Yes      | Categorization, filtering           |
| Secondary Issue Type                  | `secondary_issue_type`             | Plain Text  | No       | Secondary categorization, filtering |
| Issue Description                     | `issue_description`                | Plain Text  | Yes      | User-facing context                 |
| Street Address                        | `street_address`                   | Plain Text  | No       | Search                              |
| City                                  | `city`                             | Plain Text  | No       | Search                              |
| State / Province                      | `state`                            | Plain Text  | No       | Search                              |
| ZIP / Postal Code                     | `zip_code`                         | Number      | No       | Search                              |
| Neighborhood / District / Ward / etc. | `neighborhood_district`            | Plain Text  | Yes      | Filtering, categorization           |
| Supvervisor District / Ward / etc.    | `neighborhood_district_secondary`  | Plain Text  | No       | Filtering, categorization           |
| Ticket Created Date / Time            | `ticket_created_date_time`         | Date & Time | Yes      | Filtering, charting                 |
| Ticket Last Updated Date / Time       | `ticket_last_updated_date_time`    | Date & Time | No       | Filtering, charting                 |
| Ticket Closed Date / Time             | `ticket_closed_date_time`          | Date & Time | Yes      | Filtering, charting                 |
| Ticket Status                         | `ticket_status`                    | Plain Text  | Yes (Must be Open or Closed)     | Filtering, charting                 |
| Image                                 | `image`                            | URL         | No       | User-facing context                 |
| Location                              | `location`                         | Location    | Yes      | Mapping                             |

## Optional Category Mapping

Sometimes issue categories don't have citizen-friendly names.  If a publisher wishes to present a given issue category with a friendlier name, they can optionally populate a dataset, with the fields below, and the app will display alternative names within the user interface.  

An example can be found [here](https://scs.demo.socrata.com/Government/NOLA-311-Category-Names/n4pj-tfiu).  

| Attribute                       | API Field                | Type       | Required | Role within app                                                   |
| ---                             | ---                      | ---        | ---      | ---                                                               |
| Source Name                     | `source_name`            | Plain Text | No       | Identifies name within source dataset                             |
| Category Display Name           | `display_name`           | Plain Text | No       | Alternative citizen-facing category name                          |
| Secondary Category Display Name | `secondary_display_name` | Plain Text | No       | Alternative citizen-facing category name for secondary categories |

## Neighborhood / District Geospatial Data

The Service Connect App requires a Shapefile that corresponds to the `neighborhood_district` field.

If used, the Service Connect App requires a second shapefile that corresponds to the `neighborhood_district_secondary` field.
