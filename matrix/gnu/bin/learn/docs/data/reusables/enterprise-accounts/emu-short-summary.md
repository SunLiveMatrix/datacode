{% data variables.product.prodname_emus %} is a feature of {% data variables.product.prodname_ghe_cloud %} that provides even greater control over enterprise members and resources. With {% data variables.product.prodname_emus %}, all members are provisioned and managed through your identity provider (IdP) instead of users creating their own accounts on {% data variables.product.product_name %}. Organization and team membership can be managed using groups on your IdP. {% data variables.enterprise.prodname_managed_users_caps %} are restricted to their enterprise and are unable to push code, collaborate, or interact with users, repositories, and organizations outside of their enterprise. For more information, see "[AUTOTITLE](/enterprise-cloud@latest/admin/identity-and-access-management/using-enterprise-managed-users-for-iam/about-enterprise-managed-users){% ifversion not ghec %}" in the {% data variables.product.prodname_ghe_cloud %} documentation.{% else %}."{% endif %}