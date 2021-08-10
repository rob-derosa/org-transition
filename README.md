# GitHub Organization Restructuring

## Overview

Occasionally, GitHub customers need to move an organization from one Enterprise Account to another or from a free organization into an established Enterprise Account. This guide is an effort to explain how policies are applied from the Enterprise Account level down as well as any implications or considerations that should be reviewed prior to any migrations.

## Areas to consider
 * Policies configured at the Enterprise Account level supersede any configurations at the organization level
 * SAML/SSO, when configured at the Enterprise Account level, disables SSO/SAML configuration at the organization(s) level and will invalidate any organization level tokens (PAT/SAML)
 * If an Enterprise Account has SAML/SSO configured and an organization is being migrated underneath it, any Personal Access Token, SSH key, etc will need to be re-established which may affect any existing GitHub users or CI/CD workflows
 * If an organization is being moved into a new Enterprise Account (A) from a previous Enterprise Account (B), any Enterprise Account owners/admins from (B) will need to be re-added to (A) and re-authenticated


## Default Settings for GitHub Enterprise Cloud

Below are the default settings for a newly established GitHub Enterprise Cloud account. Please consider using this as a comparison when migrating new organizations over to a new Enterprise Account as an understanding of what policies will need to be re-established or configured at the organization level.

 ### Repositories
![](/assets/repositories.png)

 ### Actions
![](/assets/actions.png)

 ### Project Policies
![](/assets/project-policies.png)

 ### Team Policies
![](/assets/team-policies.png) 
 
 ### Org Policies
![](/assets/org-policies.png)

 ### Security
![](/assets/security.png)

 ### Domains
![](/assets/domains.png)

 ### Webhooks
![](/assets/webhooks.png)
