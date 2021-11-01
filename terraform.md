---

copyright:
  years: 2021
lastupdated: "2021-08-25"

subcollection: dns

---

{:external: target="_blank" .external}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:note: .note}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}


# Setting up Terraform for Domain Name Registration
{: #terraform-setup-dns}

Terraform on {{site.data.keyword.cloud}} enables predictable and consistent provisioning of {{site.data.keyword.cloud_notm}} services so that you can rapidly build complex, multi-tier cloud environments following Infrastructure as Code (IaC) principles. Similar to using the {{site.data.keyword.cloud_notm}} CLI or API and SDKs, you can automate the provisioning, update, and deletion of your domain resources by using HashiCorp Configuration Language (HCL).
{: shortdesc}

Looking for a managed Terraform on {{site.data.keyword.cloud}} solution? Try out [{{site.data.keyword.bplong}}](/docs/schematics?topic=schematics-getting-started). With {{site.data.keyword.bpshort}}, you can use the Terraform scripting language that you are familiar with, but you don't have to worry about setting up and maintaining the Terraform command line and the {{site.data.keyword.cloud}} Provider plug-in. {{site.data.keyword.bpshort}} also provides pre-defined Terraform templates that you can easily install from the {{site.data.keyword.cloud}} catalog.
{: tip}

## Installing Terraform and configuring resources for domains
{: #install-terraform-dns}

To install Terraform and configure resources for domain resources:

1. Follow the [Terraform on {{site.data.keyword.cloud}} getting started tutorial](/docs/ibm-cloud-provider-for-terraform?topic=ibm-cloud-provider-for-terraform-getting-started) to install the Terraform CLI and configure the {{site.data.keyword.cloud}} Provider plug-in for Terraform. The plug-in abstracts the {{site.data.keyword.cloud}} APIs that are used to provision, update, or delete domain resources.

1. Create a Terraform configuration file that is named `main.tf`. In this file, you add the configuration to create a domain resource. For more information, see the [Terraform documentation](https://www.terraform.io/docs/language/index.html){: external}.

   The following example creates an `ibm_dns_domain_registration_nameservers` resource with an ID of `data.ibm_dns_domain_registration.dns-domain-test.id` and two name servers called `ns006.name.ibm.cloud.com` and `ns017.name.ibm.cloud.com`. The name of the domain resource is `test-domain.com`.
   
      For more information, see the [ibm_dns_domain_registration_nameservers](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/resources/dns_domain_registration_nameservers){: external} usage example.
      {: note}

   ```terraform
      resource "ibm_dns_domain_registration_nameservers" "dns-domain-test" {
        dns_registration_id = data.ibm_dns_domain_registration.dns-domain-test.id
        name_servers        = ["ns006.name.ibm.cloud.com", "ns017.name.ibm.cloud.com"]
      }

      data "ibm_dns_domain_registration" "dns-domain-test" {
        name = "test-domain.com"
      }
   ```
   {: codeblock}

1. Initialize the Terraform CLI.

   ```terraform
   terraform init
   ```
   {: pre}

1. Create a Terraform execution plan. The Terraform execution plan summarizes all the actions that need to be run to create the domain resource in your account.

   ```terraform
   terraform plan
   ```
   {: pre}

1. Create the domain resource in {{site.data.keyword.cloud_notm}}.

   ```terraform
   terraform apply
   ```
   {: pre}

1. From the [{{site.data.keyword.cloud_notm}} resource list](/resources){: external}, select the domain resource that you created and note the resource ID.
