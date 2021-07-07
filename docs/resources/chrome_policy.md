---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "googleworkspace_chrome_policy Resource - terraform-provider-googleworkspace"
subcategory: ""
description: |-
  Chrome Policy resource in the Terraform Googleworkspace provider. Currently only supports policies not requiring additionalTargetKeys.
---

# googleworkspace_chrome_policy (Resource)

Chrome Policy resource in the Terraform Googleworkspace provider. Currently only supports policies not requiring additionalTargetKeys.

## Example Usage

```terraform
resource "googleworkspace_org_unit" "example" {
  name                 = "example"
  parent_org_unit_path = "/"
}

resource "googleworkspace_chrome_policy" "example" {
  org_unit_id = googleworkspace_org_unit.test.id
  policies {
    schema_name = "chrome.users.MaxConnectionsPerProxy"
    schema_values = {
      maxConnectionsPerProxy = jsonencode(34)
    }
  }
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- **org_unit_id** (String) The target org unit on which this policy is applied.
- **policies** (Block List, Min: 1) Policies to set for the org unit (see [below for nested schema](#nestedblock--policies))

### Optional

- **id** (String) The ID of this resource.

<a id="nestedblock--policies"></a>
### Nested Schema for `policies`

Required:

- **schema_name** (String) The full qualified name of the policy schema.
- **schema_values** (Map of String) JSON encoded map that represents key/value pairs that correspond to the given schema.

