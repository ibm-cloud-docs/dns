---

copyright:
  years: 2021
lastupdated: "2021-08-03"

keywords: dnr, ResellOne, migrate

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:tip: .tip}
{:external: target="_blank" .external}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}
{:faq: data-hd-content-type='faq'}
{:support: data-reuse='support'}

# Migrating from IBM ResellOne to Tucows
{: #resellone-migration}

Depending on how many domains you are managing, Tucows and IBM Cloud will automatically migrate your domains and reseller accounts over to Tucows’ retail domain platform, [Hover](https://hover.com/){:external} or the [OpenSRS](https://manage.opensrs.com/){:external} reseller platform.

Before checking out the migration options, read [Common FAQs](/docs/dns?topic=dns-resellone-migration#resellone-common-faq).

* Under 100 domains - Hover is the default migration option. Alternatively, you can choose OpenSRS. For more information, see [If you have fewer than 100 domains](/docs/dns?topic=dns-resellone-migration#resellone-basic-tier) and [specific FAQs](/docs/dns?topic=dns-resellone-migration#resellone-basic-tier-faq).
* 100 - 499 domains - OpenSRS is the default option. Alternatively, you can choose Hover. For more information, see [If you have more than 100 domains](/docs/dns?topic=dns-resellone-migration#resellone-startup-tier) and [specific FAQs](/docs/dns?topic=dns-resellone-migration#resellone-startup-tier-faq).
* 500+ domains - OpenSRS is the default migration option. For more information, see [If you have more than 100 domains](/docs/dns?topic=dns-resellone-migration#resellone-startup-tier) and [specific FAQs](/docs/dns?topic=dns-resellone-migration#resellone-growth-tier-faq).

## Common FAQs
{: #resellone-common-faq}

### When will the IBM ResellOne End of Service take effect?
{: faq}
{: support}

End of Service takes effect on 1 November 2021. For more information, see the [End of Service announcement](/docs/dns?topic=dns-resellone-eos).

### What are the benefits of migrating to Hover?
{: faq}
{: support}

As a Hover customer, you’ll benefit from a clean and intuitive domain management control panel. You'll also get an expanded selection of premium top-level domains, and great customer support.

### What are the benefits of migrating to OpenSRS?
{: faq}
{: support}

As a direct OpenSRS reseller, you’ll be able to fully manage your domains with greater ease. You'll get a greater selection of premium top-level domains and be able to offer your customers an expanded selection to automate your domain management experience. Post migration, you’ll benefit from improved availability of your business-critical domain services and additional features, including:

* Brandable end-user communications
* Scalability
* Exceptional reliability
* Flexible integration
* Competitive pricing

### What service agreement do I follow after migration to Hover?
{: faq}
{: support}

After migration, you are automatically transitioned to Tucows’ retail domains brand Hover's [Terms Of Service](https://www.hover.com/tos){:external}.

### What service agreement do I follow after migration to a Tucows OpenSRS Reseller account?
{: faq}
{: support}

After migration, you are automatically transitioned to the OpenSRS/Tucows’ Inc. Master Services Agreement. You can find this from the [OpenSRS website](https://opensrs.com/wp-content/uploads/Master_Services_Agreement.html){:external}.

Additional resources can be found in [OpenSRS Documentation](https://opensrs.com/resources/documentation/){:external}.

### If I have more questions, who can I contact?
{: faq}
{: support}

If you have questions, contact [IBM Cloud Support](/docs/dns?topic=dns-gettinghelp-with-dns).


## If you have fewer than 100 domains
{: #resellone-basic-tier}

If you have fewer than 100 domains under management, on 1 November 2021 your domains are automatically migrated to a retail account on Hover, Tucows’ retail domains brand. On the day of migration, the registrant/owner email address will receive an email from Hover that contains:  

* A welcome message
* Login instructions
* Instructions to add your billing info and set up 2FA
* Steps to double check your account information
* Hover’s contact information and support hours

Tucows will move all domains with the same registrant/owner email address into the same Hover account. If all the domains that you manage have the same registrant email, these domains migrate to a single Hover account. If you manage domains for multiple registrants, and therefore have multiple registrant/owner emails on file, Tucows creates multiple Hover accounts, one for each unique registrant email.

### Specific FAQs (for under 100 domains)
{: #resellone-basic-tier-faq}

#### What if I don't want all domains transferred to a single account?
{: faq}
{: support}

If you want to have all your domains transferred to multiple accounts, ensure that all domains in your IBM account have the same registrant/owner email address. If you do not perform this step, domains are moved into independent retail accounts.

#### What if I don't want to move to Hover?
{: faq}
{: support}

If you don’t think Hover is a suitable option, and you’d rather be set up with a reseller account, Tucows can migrate you to their OpenSRS reseller platform instead. To migrate your account to OpenSRS, reach out to [IBM Cloud Support](/docs/dns?topic=dns-gettinghelp-with-dns) by 1 October 2021. If you don’t take action, your domains are automatically moved to Hover retail accounts.

#### By what date do I need to notify IBM to be switched to a Tucows’ OpenSRS Reseller account?
{: faq}
{: support}

You must notify IBM by 1 October 2021 to switch to a Tucows’ OpenSRS Reseller account.

#### What happens if I don’t respond to the email from Hover?
{: faq}
{: support}

If you don't respond to the email from Hover, your domains are moved to Tucows’ Retail division, Hover. All emails from Hover are sent directly to the registrant/owner email addresses on file. Failing to take action will require you to speak with the Hover support team.

## If you have more than 100 domains
{: #resellone-startup-tier}

For now, just sit tight! By default, Tucows and IBM Cloud will move your domains from your Softlayer ResellOne account into the pre-provisioned OpenSRS Reseller account between 1 November 2021 and 4 November 2021. Your domains will remain available within the Softlayer ResellOne account until this time.

On 1 November 2021, you’ll be able to log in to your OpenSRS account. Here’s how:

1.	Head to https://manage.opensrs.com/.
2.	Select the **Forgot Password** option.
3.	You’ll be prompted for your username. Your OpenSRS username is your IBM username followed by `_srs` (for example, `username_srs`).
4.	After you’re logged in, you’ll want to add funding to your account and set up your branding preferences.

For more information on how to get started, see the [OpenSRS Reseller Quickstart Guide](https://help.opensrs.com/hc/en-us/articles/115005518768-Reseller-Quickstart-Guide){:external}.

### Specific FAQs (for 100-499 domains)
{: #resellone-startup-tier-faq}

#### Can I opt out of being migrated to OpenSRS?
{: faq}
{: support}

Yes, you can choose to be migrated to Tucows’ retail domain platform, Hover. You must contact IBM Cloud Support (https://cloud.ibm.com/unifiedsupport/supportcenter) before 1 October 2021.

#### What pricing tier will I be set at?
{: faq}
{: support}

To view your set pricing tier, you can log in to your [Reseller Control Panel](https://manage.opensrs.com/){:external} and navigate to **Billing & Payments**. There, you'll see the tier listed under **Pricing Tier Plan**. You can also see the OpenSRS Pricing page located here.

#### Are all my brand settings carried over from the ResellOne reseller account?
{: faq}
{: support}

Yes, all your branding settings, along with any customized messaging content, are carried over to your new account at OpenSRS.

#### Can I migrate to OpenSRS before the End of Service date?
{: faq}
{: support}

Yes, you can migrate to OpenSRS before the End of Service date. However, we recommend waiting for your account to be automatically migrated, as all your customizations are copied over. Allow us to do the heavy lifting for you.

#### What happens if I don’t respond to any of the emails?
{: faq}
{: support}

Your reseller account automatically moves to the Tucows’ OpenSRS reseller platform if you don't respond to the emails. A password reset email is triggered, which remains active for 24 hours.

#### If I choose to migrate to OpenSRS, when can I access my account and add funding in the new Tucows’ OpenSRS Reseller account?
{: faq}
{: support}

Accounts are provisioned in October 2021 at OpenSRS. You will be able to access your accounts using your IBM username with `_srs` at the end (for example, `username_srs`). You can use the **Forgot Password** link if you need to reset your password.

   If you reset your password, the same email address is used from your previous account.
   {: note}

#### If I choose to migrate to OpenSRS, will my funds be transferred to OpenSRS?
{: faq}
{: support}

Reach out to [IBM Cloud Support](/docs/dns?topic=dns-gettinghelp-with-dns) for details. In your OpenSRS Reseller account, you are required to add your funding on activation.

#### How do I connect to OpenSRS’ API?
{: faq}
{: support}

You can find information about OpenSRS’ API in the [OpenSRS API guide](https://domains.opensrs.guide/docs/overview){:external}, located in the Connection Information section.

### Specific FAQs (for 500 domains or more)
{: #resellone-growth-tier-faq}

#### What pricing tier will I be set at?
{: faq}
{: support}

To view your set pricing tier, you can log in to your Reseller Control Panel and navigate to “Billing & Payments”. There you will see the tier listed in the Pricing Tier Plan section. You can also see the OpenSRS Pricing page located here.

#### Will all my brand settings be carried over from the ResellOne reseller account?
{: faq}
{: support}

Yes, all your branding settings, along with any customized messaging content, are carried over to your new account at OpenSRS.

#### Can I migrate to OpenSRS before the End of Service date?
{: faq}
{: support}

Yes, you can migrate to OpenSRS before the End of Service date. However, we recommend waiting for your account to be automatically migrated, as all your customizations are copied over. Allow us to do the heavy lifting for you.

#### When can I access my account and add funding in the new Tucows’ OpenSRS Reseller account?
{: faq}
{: support}

Accounts are provisioned in October 2021 at OpenSRS. You will be able to access your accounts using your IBM username followed by `_srs` (for example, `username_srs`). You can use the **Forgot Password** link if you need to reset your password.

   If you reset your password, the same email address is used from your previous account.
   {: note}

#### How do I connect to OpenSRS’ API?
{: faq}
{: support}

You can find information about OpenSRS’ API in the [OpenSRS API guide](https://domains.opensrs.guide/docs/overview){:external}, located in the Connection Information section.
