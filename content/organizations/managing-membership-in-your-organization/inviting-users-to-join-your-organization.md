---
title: Inviting users to join your organization
intro: 'You can invite anyone to become a member of your organization using their username or email address for {% data variables.location.product_location %}.'
permissions: Organization owners can invite users to join an organization.
redirect_from:
  - /articles/adding-or-inviting-members-to-a-team-in-an-organization
  - /articles/inviting-users-to-join-your-organization
  - /github/setting-up-and-managing-organizations-and-teams/inviting-users-to-join-your-organization
versions:
  fpt: '*'
  ghec: '*'
topics:
  - Organizations
  - Teams
shortTitle: Invite users to join
---

## About organization invitations

If your organization has a paid per-user subscription, an unused license must be available before you can invite a new member to join the organization or reinstate a former organization member. For more information, see "[About per-user pricing](/articles/about-per-user-pricing)."

{% data reusables.organizations.org-invite-scim %}

If your organization requires members to use two-factor authentication, users that you invite must enable two-factor authentication before accepting the invitation. For more information, see "[Requiring two-factor authentication in your organization](/organizations/keeping-your-organization-secure/requiring-two-factor-authentication-in-your-organization)" and "[Securing your account with two-factor authentication (2FA)](/github/authenticating-to-github/securing-your-account-with-two-factor-authentication-2fa)."

{% ifversion fpt %}Organizations that use {% data variables.product.prodname_ghe_cloud %}{% else %}You{% endif %} can implement SCIM to add, manage, and remove organization members' access to {% data variables.product.prodname_dotcom_the_website %} through an identity provider (IdP). For more information, see "[About SCIM for organizations](/enterprise-cloud@latest/organizations/managing-saml-single-sign-on-for-your-organization/about-scim-for-organizations){% ifversion fpt %}" in the {% data variables.product.prodname_ghe_cloud %} documentation.{% else %}."{% endif %}

## Inviting a user to join your organization

{% data reusables.profile.access_org %}
{% data reusables.user-settings.access_org %}
{% data reusables.organizations.people %}
{% data reusables.organizations.invite_member_from_people_tab %}
{% data reusables.organizations.invite_to_org %}
{% data reusables.organizations.choose-to-restore-privileges %}
{% data reusables.organizations.choose-user-role %}
{% data reusables.organizations.add-user-to-teams %}
{% data reusables.organizations.send-invitation %}
{% data reusables.organizations.user_must_accept_invite_email %} {% data reusables.organizations.cancel_org_invite %}

{% ifversion organization-invitation-enhancements %}
## Retrying or canceling expired invitations

Invitations expire after 7 days. You can retry or cancel expired invitations, either one by one or in bulk. Failed invitations to outside collaborators can also be found in this view.

{% data reusables.profile.access_org %}
{% data reusables.user-settings.access_org %}
{% data reusables.organizations.people %}
{% data reusables.organizations.retrying-or-deleting-expired-invitations %}
{% endif %}

## Further reading
- "[Adding organization members to a team](/articles/adding-organization-members-to-a-team)"
