---
page_title: "cloudflare_schema_validation_schemas Data Source - Cloudflare"
subcategory: ""
description: |-
  
---

# cloudflare_schema_validation_schemas (Data Source)



## Example Usage

```terraform
data "cloudflare_schema_validation_schemas" "example_schema_validation_schemas" {
  zone_id = "023e105f4ecef8ad9ca31a8372d0c353"
  schema_id = "f174e90a-fafe-4643-bbbc-4a0ed4fc8415"
  omit_source = true
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `zone_id` (String) Identifier.

### Optional

- `filter` (Attributes) (see [below for nested schema](#nestedatt--filter))
- `omit_source` (Boolean) Omit the source-files of schemas and only retrieve their meta-data.
- `schema_id` (String) UUID.

### Read-Only

- `created_at` (String)
- `id` (String) UUID.
- `kind` (String) The kind of the schema
Available values: "openapi_v3".
- `name` (String) A human-readable name for the schema
- `source` (String) The raw schema, e.g., the OpenAPI schema, either as JSON or YAML
- `validation_enabled` (Boolean) An indicator if this schema is enabled

<a id="nestedatt--filter"></a>
### Nested Schema for `filter`

Optional:

- `omit_source` (Boolean) Omit the source-files of schemas and only retrieve their meta-data.
- `validation_enabled` (Boolean) Filter for enabled schemas


