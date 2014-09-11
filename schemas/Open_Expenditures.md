---
layout: with-sidebar
title: Open Expenditures Schema
type: schema
---

_Updated July 2014_

## Data Attributes

The entire ledger is represented as a single dataset of transactions down to the invoice distribution level. This is a summary of the data schema; a full version of the schema is documented and kept up-to-date [here](https://docs.google.com/a/socrata.com/document/d/1KM8zWA3ZM5NrmzXmrtBdrGTWRYkzpgiMwcUMELdRe-A). Two optional auxiliary datasets are documented at that location.

Some of these fields may vary from implementation to implementation.

| Attribute                        | API Field                   | Type        | Required | Value Required |
| ---                              | ---                         | ---         | ---      | ---            |
| Fiscal Year                      | `fiscal_year`               | Number      | Yes      | Yes            |
| Fiscal Period                    | `fiscal_period`             | Number      | Yes      | Yes            |
| Service                          | `service`                   | Plain Text  | Yes      | Yes            |
| Department                       | `department`                | Plain Text  | Yes      | Yes            |
| Program                          | `program`                   | Plain Text  | Yes      | Yes            |
| Expense Category                 | `expense_category`          | Plain Text  | Yes      | Yes            |
| Vendor Name                      | `vendor`                    | Plain Text  | Yes      | Yes            |
| Vendor Number                    | `vendor_id`                 | Plain Text  | Yes      | Yes            |
| Vendor Zip                       | `vendor_zip`                | Plain Text  | No       | No             |
| Payment Number                   | `payment_id`                | Plain Text  | Yes      | Yes            |
| Payment Method                   | `payment_method`            | Plain Text  | No       | No             |
| Payment Issue Date               | `payment_date`              | Date/Time   | Yes      | No             |
| Payment Status                   | `payment_status`            | Plain Text  | No       | No             |
| Invoice Number                   | `invoice_id`                | Plain Text  | Yes      | Yes            |
| Invoice Line Number              | `invoice_line`              | Number      | Yes      | Yes            |
| Invoice Line Distribution Number | `invoice_distribution_line` | Number      | Yes      | No             |
| Invoice Date                     | `invoice_date`              | Date/Time   | Yes      | No             |
| Amount                           | `amount`                    | Number      | Yes      | Yes            |
| Description                      | `description`               | Plain Text  | Yes      | No             |

