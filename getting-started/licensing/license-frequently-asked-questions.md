---
title: Frequently Asked Questions
page_title: Installing License Key - Frequently Asked Questions
description: The article lists the frequently asked questions (FAQ) on how to install a license key for the Telerik UI for WPF product.
slug: license-frequently-asked-questions
tags: installing,ui,for,wpf,file,license,key,ci,service,faq,asked,questions
published: True
position: 3
---

# Frequently Asked Questions About Installing Telerik License Key

This article lists the answers to the most frequently asked questions (FAQs) about working with the Telerik UI for WPF license key.

## Will the product function with an expired license key?

This depends on your license type.

* __Perpetual licenses__ will continue to function normally with an expired license key. However, the following will happen if you update or install a package version which is released after the expiration date of the license:

	* A watermark appears on application startup.
	* A modal dialog appears on application startup.
	* A warning message is logged in the build log.	
		
		See the [Invalid License]({%slug license-activation-errors-and-warnings%}#invalid-license) section for more information.

* __Subscription licenses__ will prevent you from building the application with an expired license key. Deployed applications will continue to function normally.

* __Trial licenses__ will prevent you from building or running the application. The following will happen if you try to build or run the application:
	
	* A watermark appears on application startup.
	* A modal dialog appears on application startup.
	* A warning message is logged in the build log.	
		
		See the [Invalid License]({%slug license-activation-errors-and-warnings%}#invalid-license) section for more information.

## I updated the version of the UI for WPF packages in my project and the invalid license errors have appeared. What is the cause of this behavior?

If this happens, the possible reason is that the end date of the license activated in your application is before the release date of the newly installed UI for WPF. To fix this issue:

1. [Download a new license key]({%slug installing-license-key%}#downloading-the-license-key).
2. [Activate the new license key]({%slug installing-license-key%}) in your project.

## Can I use the same license key in multiple builds?

You can use your personal license key in multiple pipelines, builds, and environments.

However, each individual developer must use a unique personal license key.

## Does the license key expire?

Yes, the license key expires at the end of your support subscription:

* For trial users, this is at the end of your 30-day trial.

* For commercial license holders, this is when your subscription term expires.

You will need to obtain and install a new license key after starting a trial, renewing a license, or upgrading a license.

> An expired perpetual license key is valid for all Telerik UI for WPF versions published before its expiration date.

## Do I need an Internet connection to activate the license?

No, the license activation and validation are performed entirely offline.

The license is not validated with our services at any point in the project lifecycle.

## Do I have to add the license key to source control?

No, you do not have to add the `telerik-license.txt` license key file or its contents to source control.

Build servers must use the `TELERIK_LICENSE` environment variable described in [Adding the License Key to CI Services]({%slug installing-license-to-ci-services%}).

> Do not store the license key in plaintext, for example, in a GitHub Actions Workflow definition.

## What happens if both the environment variable and the license key file are present?

If both the `TELERIK_LICENSE` environment variable and the `telerik-license.txt` file are present, then the environment variable will be used.

To enforce the use of the license key file, unset the environment variable.

## My team has more than one license holder. Which key do we have to use?

To activate Telerik UI for WPF, you can use any of the keys associated with your subscriptions.

## Are earlier versions of Telerik UI for WPF affected?

No, versions released prior to Jan 2025 (Q1) do not require a license key.

## What happens if I make a change to non-Telerik parts of the code after the subscription expires?

This depends on your license:

* If you have a perpetual license, you can build the application with the Telerik components.

* If you have an expired subscription license, the build will fail.

## See Also

* [License Activation Errors and Warnings]({%slug license-activation-errors-and-warnings%})
* [Setting Up Your License Key]({%slug installing-license-key%})
* [Adding the License Key to CI Services]({%slug installing-license-to-ci-services%})
