---

copyright:
  years: 2021, 2023
lastupdated: "2023-03-29"

keywords: dnr, ResellOne, migrate

subcollection: dns

---

{{site.data.keyword.attribute-definition-list}}

# Migrating from IBM ResellOne to Tucows
{: #resellone-migration}

In the period between 2 November 2021 - 10 November 2021, for migration, your domains will be in a frozen state. No transfer, renewal, or other actions can happen during this period. If any of your domains are about to expire, complete renewal actions immediately (before the 1 November 2021 deadline).
{: important}

On 8 November 2021, depending on how many domains you are managing, Tucows, and IBM Cloud will automatically migrate your domains and reseller accounts over to Tucows’ retail domain platform, [Hover](https://hover.com/){: external} or the [OpenSRS](https://manage.opensrs.com/){: external} reseller platform.

Before you check out the migration options, read the [Common FAQs](/docs/dns?topic=dns-resellone-migration#resellone-common-faq).

* Under 100 domains - Hover is the default migration option. Alternatively, you can choose OpenSRS. For more information, see [If you have fewer than 100 domains](/docs/dns?topic=dns-resellone-migration#resellone-basic-tier) and [specific FAQs](/docs/dns?topic=dns-resellone-migration#resellone-basic-tier-faq).
* 100 - 499 domains - OpenSRS is the default option. Alternatively, you can choose Hover. For more information, see [If you have more than 100 domains](/docs/dns?topic=dns-resellone-migration#resellone-startup-tier) and [specific FAQs](/docs/dns?topic=dns-resellone-migration#resellone-startup-tier-faq).
* 500+ domains - OpenSRS is the default migration option. For more information, see [If you have more than 100 domains](/docs/dns?topic=dns-resellone-migration#resellone-startup-tier) and [specific FAQs](/docs/dns?topic=dns-resellone-migration#resellone-growth-tier-faq).

## Common FAQs
{: #resellone-common-faq}

### When does the IBM ResellOne end of service take effect?
{: #resellone-eos-date}
{: faq}
{: support}

End of service takes effect on 1 November 2021. For more information, see the [End of Service announcement](/docs/dns?topic=dns-resellone-eos).

### What are the benefits of migrating to Hover?
{: #hover-benefits}
{: faq}
{: support}

As a Hover customer, you benefit from a clean and intuitive domain management control panel. You also get an expanded selection of premium top-level domains, and great customer support.

### What are the benefits of migrating to OpenSRS?
{: #opensrs-benefits}
{: faq}
{: support}

As a direct OpenSRS reseller, you are able to fully manage your domains with greater ease. You get a greater selection of premium top-level domains and be able to offer your customers an expanded selection to automate your domain management experience. Post migration, you benefit from improved availability of your business-critical domain services and extra features, including:

* Brandable user communications
* Scalability
* Exceptional reliability
* Flexible integration

### What service agreement do I follow after migration to Hover?
{: #hover-service-agreement-after-migration}
{: faq}
{: support}

After migration, you automatically transition to Tucows’ retail domains brand Hover's [Terms Of Service](https://www.hover.com/tos){: external}.

### What service agreement do I follow after migration to a Tucows OpenSRS Reseller account?
{: #opensrs-service-agreement-after-migration}
{: faq}
{: support}

After migration, you automatically transition to the OpenSRS/Tucows’ Inc. Master Services Agreement. You can find this from the [OpenSRS website](https://opensrs.com/wp-content/uploads/Master_Domain_Registration_Agreement.html){: external}.

Additional resources can be found in [OpenSRS Documentation](https://opensrs.com/resources/documentation/){: external}.

### If I have more questions, who can I contact?
{: #additional-questions}
{: faq}
{: support}

If you have questions, contact [IBM Cloud Support](/docs/dns?topic=dns-gettinghelp-with-dns).

## If you have fewer than 100 domains
{: #resellone-basic-tier}

If you have fewer than 100 domains under management, your domains are automatically migrated to a retail account on Hover, Tucows’ retail domains brand in the period between 2 November 2021 - 10 November 2021. On the day of migration, the registrant/owner email address receives an email from Hover that contains:

* A welcome message
* Login instructions
* Instructions to add your billing information and set up 2FA
* Steps to double check your account information
* Hover’s contact information and support hours

Tucows moves all domains with the same registrant or owner email address into the same Hover account. If all the domains that you manage have the same registrant email, these domains migrate to a single Hover account. If you manage domains for multiple registrants, and therefore have multiple registrant/owner emails on file, Tucows creates multiple Hover accounts, one for each unique registrant email.

### Specific FAQs (for under 100 domains)
{: #resellone-basic-tier-faq}

#### What if I don't want all domains transferred to a single account?
{: #decline-transfer}
{: faq}
{: support}

If you want to have all your domains transferred to multiple accounts, ensure that all domains in your IBM account have the same registrant or owner email address. If you do not complete this step, domains are moved into independent retail accounts.

#### What if I don't want to move to Hover?
{: #decline-move-hover}
{: faq}
{: support}

If you don’t think Hover is a suitable option, and you’d rather be set up with a reseller account, Tucows can migrate you to their OpenSRS reseller platform instead. To migrate your account to OpenSRS, reach out to [IBM Cloud Support](/docs/dns?topic=dns-gettinghelp-with-dns) by 1 October 2021. If you don’t act, your domains are automatically moved to Hover retail accounts.

#### By what date do I need to notify IBM to switch to a Tucows’ OpenSRS Reseller account?
{: #date-to-notify}
{: faq}
{: support}

Notify IBM by 1 October 2021 to switch to a Tucows’ OpenSRS Reseller account.

#### What happens if I don’t respond to the email from Hover?
{: #no-response}
{: faq}
{: support}

If you don't respond to the email from Hover, your domains are moved to Tucows’ Retail division, Hover. All emails from Hover are sent directly to the registrant/owner email addresses on file. Failing to take action requires you to speak with the Hover support team.

## If you have more than 100 domains
{: #resellone-startup-tier}

By default, Tucows and IBM Cloud will move your domains from your Softlayer ResellOne account into the pre-provisioned OpenSRS Reseller account between 2 November 2021 - 10 November 2021. Your domains remain available within the Softlayer ResellOne account until this time.

On 11 November 2021, you’ll be able to log in to your OpenSRS account. Here’s how:

1.	Head to https://manage.opensrs.com/.
2.	Select the **Forgot Password** option.
3.	You are prompted for your username. Your OpenSRS username is your IBM username followed by `_srs` (for example, `username_srs`).
4.	After you’re logged in, you’ll want to add funding to your account and set up your branding preferences.

For more information, see the [OpenSRS Reseller Quickstart Guide](https://support.opensrs.com/support/solutions/articles/201000063205){: external}.

### Specific FAQs (for 100-499 domains)
{: #resellone-startup-tier-faq}

#### Can I opt out of being migrated to OpenSRS?
{: #100-499-opt-out}
{: faq}
{: support}

Yes, you can choose to be migrated to Tucows’ retail domain platform, Hover. Contact [IBM Cloud Support](https://cloud.ibm.com/unifiedsupport/supportcenter) before 1 October 2021.

#### Are all my brand settings carried over from the ResellOne reseller account?
{: #are-brand-settings-carried-over}
{: faq}
{: support}

Yes, all your branding settings, along with any customized messaging content, are carried over to your new account at OpenSRS.

#### Can I migrate to OpenSRS before the end of service date?
{: #100-499-migrate-before-eos}
{: faq}
{: support}

Yes, you can migrate to OpenSRS before the end of service date. However, we recommend waiting for your account to be automatically migrated, as all your customizations are copied over. Allow us to do the heavy lifting for you.

#### What happens if I don’t respond to any of the emails?
{: #100-499-no-response-email}
{: faq}
{: support}

Your reseller account automatically moves to the Tucows’ OpenSRS reseller platform if you don't respond to the emails. A password reset email is triggered, which remains active for 24 hours.

#### If I choose to migrate to OpenSRS, when can I access my account in the new Tucows’ OpenSRS Reseller account?
{: #100-499-when-to-access}
{: faq}
{: support}

Accounts are provisioned in October 2021 at OpenSRS. You are able to access your accounts by using your IBM username with `_srs` at the end (for example, `username_srs`). You can use the **Forgot Password** link if you need to reset your password.

   If you reset your password, the same email address is used from your previous account.
   {: note}

#### How do I connect to OpenSRS’ API?
{: #100-499-how-to-connect}
{: faq}
{: support}

You can find information about OpenSRS’ API in the [OpenSRS API guide](https://domains.opensrs.guide/docs/overview){: external}, which is located in the Connection Information section.

### Specific FAQs (for 500 domains or more)
{: #resellone-growth-tier-faq}

#### Will all my brand settings be carried over from the ResellOne reseller account?
{: #500-settings-carried-over}
{: faq}
{: support}

Yes, all your branding settings, along with any customized messaging content, are carried over to your new account at OpenSRS.

#### Can I migrate to OpenSRS before the end of service date?
{: #500-migrate-before-eos}
{: faq}
{: support}

Yes, you can migrate to OpenSRS before the end of service date. However, we recommend waiting for your account to be automatically migrated, when all your customizations are copied over. Allow us to do the heavy lifting for you.

#### When can I access my account in the new Tucows’ OpenSRS Reseller account?
{: #500-when-to-access}
{: faq}
{: support}

Accounts are provisioned in October 2021 at OpenSRS. You are able to access your accounts by using your IBM username followed by `_srs` (for example, `username_srs`). You can use the **Forgot Password** link if you need to reset your password.

   If you reset your password, the same email address is used from your previous account.
   {: note}

#### How do I connect to OpenSRS’ API?
{: #500-how-to-connect}
{: faq}
{: support}

You can find information about OpenSRS’ API in the [OpenSRS API guide](https://domains.opensrs.guide/docs/overview){: external}, which is located in the Connection Information section.
