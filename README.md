# GitHub Organization Restructuring

## Overview

Occasionally, GitHub customers need to move an organization from one Enterprise Account to another or from a free organization into an established Enterprise Account. This guide is an effort to explain how policies are applied from the Enterprise Account level down as well as any implications or considerations that should be reviewed prior to any migrations.

## Considerations
 * Policies configured at the Enterprise Account level supersede any configurations at the organization level
 * SAML, when configured at the Enterprise Account level, disables SAML configuration at the organization(s) level and will invalidate any organization level tokens (PAT/SAML/SSH)
   * Configuring SAML at the organization level is recommended if you're dealing with a small number of organizations or have multiple identity providers
  * If SAML is configured at the Enterprise Account level and an organization is being migrated underneath it, any PATs, SSH keys and SAML tokens will need to be re-established which may affect any existing GitHub users or CI/CD workflows
 * If an organization is being moved into a new Enterprise Account (A) from a previous Enterprise Account (B), any Enterprise Account owners/admins from (B) will need to be re-added to (A) and re-authenticated
 * To promote innersource and sharing of repositories within an Enterprise Account, consider setting the visibility of repositories to `Internal` - this will allow anyone within the Enterprise Account (not just your organization) to find and contribute to that project
 * [Additional information around billing at the Enterprise Account level](https://docs.github.com/en/billing/managing-billing-for-your-github-account/about-billing-for-your-enterprise)
 * [See this doc that outlines the actual process for organization restructuring](https://docs.google.com/document/d/1pHiyFH_DUHUDFoBIfGTK3LTBsuU1ZgJB9lC6iqtcoJw/edit?usp=sharing) 
