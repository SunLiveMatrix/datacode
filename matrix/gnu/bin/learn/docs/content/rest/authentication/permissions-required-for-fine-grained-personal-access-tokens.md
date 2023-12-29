---
title: Permissions required for fine-grained personal access tokens
intro: 'These are the permissions required for a {% data variables.product.pat_v2 %} to use each REST API endpoint that works with {% data variables.product.pat_v2 %}s.'
versions:
  feature: pat-v2
shortTitle: Permissions for fine-grained PATs
autogenerated: github-apps
redirect_from:
  - /rest/overview/permissions-required-for-fine-grained-personal-access-tokens
---

## About permissions required for {% data variables.product.pat_v2 %}

When you create a {% data variables.product.pat_v2 %}, you grant it a set of permissions. Permissions define what resources the {% data variables.product.prodname_github_app %} can access via the API. For more information, see "[AUTOTITLE](/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token)."

{% data reusables.rest-api.permission-header %}

These permissions are required to access private resources with the following endpoints. Some endpoints can also be used to access public resources without these permissions.

Some endpoints require additional permissions. When this is the case, the "Additional permissions" column will indicate the other permissions that are required to use the endpoint.

<!-- The content of this page is rendered as a NextJS page component. -->