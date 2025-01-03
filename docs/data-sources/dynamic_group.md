---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "googleworkspace_dynamic_group Data Source - terraform-provider-googleworkspace"
subcategory: ""
description: |-
  Dynamic group data source in the Terraform Googleworkspace provider. Dynamic Group resides under the https://www.googleapis.com/auth/cloud-identity.groups client scope.
---

# googleworkspace_dynamic_group (Data Source)

Dynamic group data source in the Terraform Googleworkspace provider. Dynamic Group resides under the `https://www.googleapis.com/auth/cloud-identity.groups` client scope.



<!-- schema generated by tfplugindocs -->
## Schema

### Optional

- `email` (String) The group's email address. If your account has multiple domains,select the appropriate domain for the email address. The email must be unique.
- `id` (String) The unique ID of a group. A group id can be used as a group request URI's groupKey.

### Read-Only

- `description` (String) An extended description to help users determine the purpose of a group.For example, you can include information about who should join the group,the types of messages to send to the group, links to FAQs about the group, or related groups.
- `labels` (Map of String) One or more label entries that apply to the Group. Currently supported labels contain a key with an empty value.
- `name` (String) The group's display name.
- `query` (String) The dynamic group query.
