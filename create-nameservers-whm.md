---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Create your own nameservers in Cpanel/WHM

This article gives steps for how to create your own nameservers using Web Host Manager (WHM). If you run into problems after following these steps, please submit a support ticket referencing this article.

1. First, decide what the names of your nameservers will be. For example, let’s say that my hosting company is called “Awesome Server Hosting” so I’d like to setup `ns1.awesomeserverhosting.com` and `ns2.awesomeserverhosting.com`.

* Login to WHM on your server by going to https://XX.XX.XX.XX:2087 in your browser.

* To set up your name servers, select the first option in the left-hand bar, which should be “Basic cPanel/WHM Setup”. 

 * Here you can set the name of your primary, secondary, tertiary and quaternary name servers.

 * When you’re done, select the “Save” button.

2. Now create the Zone file for “awesomeserverhosting.com” in my server. There are two ways to do this task:

First method: Create the domain account for “awesomeserverhosting.com”. Instructions for this are outside of the scope of this article, please consult the [cPanel documentation](http://www.cpanel.net/support/docs/11//whm/account_functions_creatnewacct.html) for more information: 

   * Select “Add a DNS Zone” under “DNS Functions” in the left-hand sidebar.

   * Provide the IP aaddress where the main website is hosted for “awesomeserverhosting.com” and of course, the domain name.

   **Note: Do this only if you do not plan on hosting `awesomeserverhosting.com` on this server!**

   * Under the heading **Networking Setup** click on **Nameserver IPs**.

   * Provide the names of your name servers. For example, submit `ns1.awesomeserverhosting.com` and then `ns2.awesomeserverhosting.com`.

   * In the left-hand bar, locate **Nameserver Setup** under **Service Configuration**.

   * A message similar to this one will be displayed: “We recommend you do not enable the nameserver unless you are going to use it. If you wish to disable the nameserver you can always turn it off in the Service Manager”.

   * We’re here to get our name servers up and running, so select the button marked **Proceed >>**. The `cPanel` tool will make sure that you have the proper packages installed to your server and that they are configured to work properly to host your name services. Now you’re all set!

External Links:

* [cPanel documentation](http://www.cpanel.net/support/docs/11//whm/account_functions_creatnewacct.html)
