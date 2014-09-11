---
layout: with-sidebar
title: Open Budget Schema
type: schema
---

_Updated July 2014_

# Introduction
Three primary datasets work together to power an Open Budget application. This is a summary of the data schema; a full version of the schema is documented and kept up-to-date [here](https://docs.google.com/a/socrata.com/document/d/1iUfkMB17vtANwF2z7_WnS-vPTTYdQFJRxsBbSR2WTk4). A shapefile and an additional auxiliary dataset are documented at that location.

## Operating Budget

The Operating Budget dataset describes the operating budget of the jurisdiction over several years.

Some of these fields may vary from implementation to implementation.

| Attribute                        | API Field                   | Type        | Required | Value Required |
| ---                              | ---                         | ---         | ---      | ---            |
| Fiscal Year                      | `fiscal_year`               | Number      | Yes      | Yes            |
| Service                          | `service`                   | Plain Text  | Yes      | Yes            |
| Department                       | `department`                | Plain Text  | Yes      | Yes            |
| Program                          | `program`                   | Plain Text  | Yes      | Yes            |
| Expense Category                 | `expense_category`          | Plain Text  | Yes      | Yes            |
| Expense Type                     | `expense_type`              | Plain Text  | Yes      | No             |
| Fund                             | `fund`                      | Plain Text  | Yes      | No             |
| Fund Type                        | `fund_type`                 | Plain Text  | Yes      | No             |
| Description                      | `description`               | Plain Text  | Yes      | No             |
| Recommended Amount               | `recommended_amount`        | Number      | Yes      | Yes            |
| Approved Amount                  | `approved_amount`           | Number      | Yes      | Yes            |

## Capital Budget

The Capital Budget dataset describes the capital budget of the jurisdiction over several years, for multiple projection years into the future.

Some of these fields may vary from implementation to implementation.

| Attribute                | API Field                 | Type        | Required | Value Required |
| ---                      | ---                       | ---         | ---      | ---            |
| Fiscal Year              | `fiscal_year`             | Number      | Yes      | Yes            |
| Service                  | `service`                 | Plain Text  | Yes      | Yes            |
| Department               | `department`              | Plain Text  | Yes      | Yes            |
| Project                  | `project`                 | Plain Text  | Yes      | Yes            |
| Project ID               | `project_id`              | Plain Text  | Yes      | Yes            |
| Fund                     | `fund`                    | Plain Text  | Yes      | No             |
| Fund Type                | `fund_type`               | Plain Text  | Yes      | No             |
| Thru FY Recommended      | `thru_fy_recommended`     | Number      | Yes      | Yes            |
| Thru FY Approved         | `thru_fy_approved`        | Number      | Yes      | Yes            |
| FY Recommended           | `fy_recommended`          | Number      | Yes      | Yes            |
| FY Approved              | `fy_approved`             | Number      | Yes      | Yes            |
| FY +1 Recommended        | `fy_plus_1_recommended`   | Number      | Yes      | Yes            |
| FY +1 Approved           | `fy_plus_1_approved`      | Number      | Yes      | Yes            |
| FY +2 Recommended        | `fy_plus_2_recommended`   | Number      | Yes      | Yes            |
| FY +2 Approved           | `fy_plus_2_approved`      | Number      | Yes      | Yes            |
| …                        | …                         | Number      | Yes      | Yes            |
| Beyond FY +n Recommended | `fy_beyond_n_recommended` | Number      | Yes      | Yes            |
| Beyond FY +n Approved    | `fy_beyond_n_approved`    | Number      | Yes      | Yes            |

## Capital Projects

The Capital Projects dataset describes the details and status of each project in the capital budget.

| Attribute                | API Field                 | Type        | Required | Value Required |
| ---                      | ---                       | ---         | ---      | ---            |
| Project                  | `project`                 | Plain Text  | Yes      | Yes            |
| Project ID               | `project_id`              | Plain Text  | Yes      | Yes            |
| Project Description      | `description`             | Plain Text  | Yes      | No             |
| Project Address          | `address`                 | Plain Text  | Yes      | No             |
| Current Phase            | `current_phase`           | Plain Text  | Yes      | No             |
| Current Phase Type       | `current_phase_type`      | Plain Text  | Yes      | No             |
| Project URL              | `project_url`             | Plain Text  | Yes      | No             |
| Latitude                 | `latitude`                | Number      | Yes      | No             |
| Longitude                | `longitude`               | Number      | Yes      | No             |
| Districts                | `districts`               | Plain Text  | Yes      | No             |

