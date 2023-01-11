---
sidebar_position: 1
title: Azure Benefits
labels: azure
---

## Overview

If you have been assigned a licence for Visual Studio Enterprise, you might be aware that it also includes $150 monthly credits in Azure. This document will guide you through the setup process and transferring to your personal tenant (assuming that you have one).

:::note
Transferring the subscription is of course optional, but in most cases this is beneficial due to insufficient privileges or not want to setup your own DNS/custom domains in company tenant etc.
:::

---

## Visual Studio

Ok, so first off we should verify that you have the correct entitlement.

1. Go to [my.visualstudio.com](https://my.visualstudio.com/), sign in with your company account
1. Click `Subscriptions`
1. Under `Subscription / Program` Visual Studio Enterprise (MPN) should be listed.
   ![img](@site/static/img/mpn/mpn-active-sub.png)
1. If you don't have this, contact your manager.
1. If you do, this means that you are eligible for the Azure Benefit. Go back to the start page to activate it if you haven't already.
   ![img](@site/static/img/mpn/mpn-enable-sub.png)

:::info
This will provision a new Azure subscription named `Visual Studio Enterprise Subscription – MPN` in the tenant linked to your user account and give you Owner permission on it.
:::

---

## Azure

1. Next you should log in to the Azure portal with your personal account. Ensure you that you:
   1. are in the correct tenant (lab/personal)
   2. have sufficient privileges to invite guest users
2. Invite the account with the Visual Studio Enterprise subscription to your personal tenant. (business account)
   1. This lets you select your lab tenant later when we will transfer the subscription.

---

1. Log in to the Azure portal with your business account, ensure that you are in business tenant and that your subscription isn't  excluded by Azure portal subscription filter.
1. Find your personal MPN subscription in the overview, it might be more than one subscriptions with same name.
   1. You should be able to distinguish your subscription based on permission. You should have `Owner` permission on yours.
   ![img](@site/static/img/mpn/mpn-sub-iam.png)
1. Navigate back to the subscription overview.
   ![img](@site/static/img/mpn/mpn-sub-transfer.png)
1. Click "Change directory",
1. Select your personal tenant (should now be visible as a destination).

:::caution
Transferring the subscription to another tenant will have an impact on RBAC assignments and Managed Identities. Review impact  before you accept transfer.
:::

1. Click "Change".

:::note
NOTE: It can take a while (~1-2 hours) before the subscription appears in your personal tenant.
:::

1. Switch back to personal tenant (with your business account)
1. You should find the transferred subscription in the subscription overview.
1. You can now delegate permissions to you personal account if you prefer to use that.

:::tip
Make sure to cleanup costly resources when you are not using them. When you run out of credits, the subscription will be disabled and cannot be used until your subscription enter a new billing period.
:::

Now go enjoy your credits!
