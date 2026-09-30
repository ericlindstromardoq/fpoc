# Fingrid PoC — mock ServiceNow Table API

Static JSON in ServiceNow Table API shape (`{"result": [...]}`), served by GitHub Pages,
used as an Import Builder REST source for Fingrid AAMOS PoC use cases 4.2.1 and 4.2.3.

| Endpoint | Source file | Records |
|---|---|---|
| `api/now/table/cmdb_ci_business_app.json` | AAMOS-poc-applications.xlsx | 9 |
| `api/now/table/cmdb_rel_ci.json` | AAMOS-poc-integrations.csv | 32 |

Field names follow ServiceNow with `sysparm_exclude_reference_link=true` (reference fields as plain sys_id)
and dot-walked names (`parent.name`, `child.name`). Data is masked: application, integration and person names and descriptions are replaced with neutral labels
(Application 01…, Integration 01…, Owner A…). sys_ids, serial numbers, lifecycle, status, view and data-group values are kept
so records still match Fingrid ID / Custom ID in Ardoq.
