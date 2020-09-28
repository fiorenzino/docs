---
title: About GitHub Container Registry
intro: 'The {{ site.data.variables.product.prodname_github_container_registry }} allows you to seamlessly host and manage Docker container images in your organization or personal user account on {{ site.data.variables.product.prodname_dotcom }}. {{ site.data.variables.product.prodname_github_container_registry }} allows you to configure who can manage and access packages using fine-grained permissions.'
product: '{{ site.data.reusables.gated-features.packages }}'
versions:
  free-pro-team: '*'
---

{% note %}

**Note:** {{ site.data.variables.product.prodname_github_container_registry }} is currently in public beta and subject to change. Currently, {{ site.data.variables.product.prodname_github_container_registry }} only supports Docker image formats. During the beta, storage and bandwidth is free.

{% endnote %}


{{ site.data.reusables.package_registry.container-registry-feature-highlights }}

To share context about your package's use, you can link a repository to your container image on {{ site.data.variables.product.prodname_dotcom }}. For more information, see "[Connecting a repository to a container image](/packages/managing-container-images-with-github-container-registry/connecting-a-repository-to-a-container-image)."

### Unterstützte Formate

The {{ site.data.variables.product.prodname_container_registry }} currently only supports Docker images.


### Visibility and access permissions for container images

If you have admin permissions to a container image, you can set the container image to private or public. Public images allow anonymous access and can be pulled without authentication or signing in via the CLI.

As an admin, you can also grant access permissions for a container image that are separate from the permissions you've set at the organization and repository levels.

For container images published and owned by a user account, you can give any person an access role. For container images published and owned by an organization, you can give any person or team in the organization an access role.

| Permission role | Access description                                                                                                                               |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| Read (Gelesen)  | Can download package. <br> Can read package metadata.                                                                                      |
| Schreiben       | Can upload and download this package. <br> Can read and write package metadata.                                                            |
| Verwalten       | Can upload, download, delete, and manage this package. <br> Can read and write package metadata. <br> Can grant package permissions. |

For more information, see "[Configuring access control and visibility for container images](/packages/managing-container-images-with-github-container-registry/configuring-access-control-and-visibility-for-container-images)."

### Informationen zur Abrechnung für {{ site.data.variables.product.prodname_github_container_registry }}

{{ site.data.reusables.package_registry.billing-for-container-registry }}

### Support kontaktieren

If you have feedback or feature requests for {{ site.data.variables.product.prodname_github_container_registry }}, use the [feedback form](https://support.github.com/contact/feedback?contact%5Bcategory%5D=packages).

Contact {{ site.data.variables.contact.github_support }} about {{ site.data.variables.product.prodname_github_container_registry }} using [our contact form](https://support.github.com/contact?form%5Bsubject%5D=Re:%20GitHub%20Packages) if:

* You experience anything that contradicts the documentation.
* You encounter vague or unclear errors.
* Your published package contains sensitive data, such as GDPR violations, API Keys, or personally-identifying information.