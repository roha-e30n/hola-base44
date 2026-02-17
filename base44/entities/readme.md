# Base44 Entity

Links
* https://docs.base44.com/developers/references/sdk/docs/type-aliases/entities
* https://docs.base44.com/developers/backend/resources/entities/entity-schemas
* https://docs.base44.com/developers/backend/resources/entities/user-schema
* https://docs.base44.com/Building-your-app/Using-media (upload limits)

## Limits

* 10 MB data files (CSV, JSON) - file upload limits in the AI chat
* 50 MB data files (CSV, JSON) - file upload limits on your live app
* 5.000 row read limit

## Built-in fields

* 458 byte built-in metadata fields per row
* 70.000 rows ~ 50 MB / (458 meta data + 256 user data) 

| Field | Type | Description | Index | Space |
|---|---|---|---|---|
| id | string | Unique identifier for the record | unique | 48 |
| created_date | datetime | When the record was created | sort | 46 |
| updated_date | datetime	| When the record was last updated | sort  | 46 |
| created_by | string | Email of the user who created the record | filter | 87 |
| created_by_id | string | ID of the user who created the record | | 22 |
| is_deleted (internal) | boolean | Soft delete flag | trash | 25 |
| deleted_date (internal) | datetime | When the record was deleted | sort | 46 |
| is_sample (internal) | boolean | Whether the record is sample data | | 12 |
| entity_name (internal) | string | Name of the entity type | | 33 |
| app_id (internal) | string | App ID | app | 48 |
| environment (internal) | string | Either prod or dev | env | 45 |
