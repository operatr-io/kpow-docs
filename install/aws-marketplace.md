---
description: Purchase and Provision kPow on the AWS Marketplace
---

# AWS Marketplace

kPow is available to [purchase via the AWS Marketplace](https://aws.amazon.com/marketplace/seller-profile?id=ab356f1d-3394-4523-b5d4-b339e3cca9e0).

kPow works beautifully with Amazon MSK and runs perfectly in ECS / Fargate / EKS.

Subscribe to kPow on the AWS Marketplace and get an **automatically licensed** container billed to your AWS account monthly with the freedom to update to the latest kPow whenever you like.

{% hint style="info" %}
See our [**AWS Marketplace Seller Profile**](https://aws.amazon.com/marketplace/seller-profile?id=ab356f1d-3394-4523-b5d4-b339e3cca9e0) to see every option for purchasing kPow on AWS.
{% endhint %}

## The Basics

When you subscribe to a [kPow product on the AWS Marketplace](https://aws.amazon.com/marketplace/seller-profile?id=ab356f1d-3394-4523-b5d4-b339e3cca9e0) you gain access to a kPow AWS Marketplace container that is functionally the same as the kPow container available via [Dockerhub](https://hub.docker.com/r/operatr/kpow).

The AWS Marketplace container makes a single call to [AWSMarketplaceMetering/registerUsage](https://docs.aws.amazon.com/marketplacemetering/latest/APIReference/API_RegisterUsage.html) when kPow starts, allowing AWS to check your subscription and meter your usage if you have chosen the hourly-metered product.

The kPow AWS Marketplace container is **automatically licensed** to the AWS account that subscribes to a product and that account is billed monthly for the subscription. You **do not need to arrange a separate license with us directly** if you subscribe to a kPow product on the AWS Marketplace. It just works.

We update each kPow product on the AWS Marketplace with every major release, simply check your subscription details to find the latest container and update whenever you like.

## The Products

There are three kPow products on the AWS Marketplace.

{% hint style="info" %}
Each kPow product is functionally the same, only the billing and licensing change.
{% endhint %}

### [kPow \(Pro\) - Hourly Metered](https://aws.amazon.com/marketplace/pp/B084BTWJHD?ref_=srh_res_product_title)

Subscribe to [kPow \(Pro\)](https://aws.amazon.com/marketplace/pp/B084BTWJHD?ref_=srh_res_product_title) to gain access to a Marketplace kPow container that can connect to a single Kafka Cluster and associated Schema Registries and Kafka Connect clusters.

Start as many instances of kPow as you need from the provided container. Usage of each instance is metered and billed by the hour at the kPow headline price of **$0.16c/hr**. 

kPow \(Pro\) allows you to pay only for the kPow hours you use with no ongoing commitment.

### [kPow \(Team\) - Monthly Subscription](https://aws.amazon.com/marketplace/pp/B08KFQGJSZ?ref_=srh_res_product_title)

Subscribe to [kPow \(Team\) ](https://aws.amazon.com/marketplace/pp/B08KFQGJSZ?ref_=srh_res_product_title)to gain access to a Marketplace kPow container that can connect to up to six Kafka Clusters and their associated Schema Registries and Kafka Connect clusters at once.

kPow Team comes with a license to use the kPow container with at most six Kafka clusters, regardless of how many separate instances of kPow you start. Usage is not metered and the subscriber AWS account is billed monthly at the team subscription price of **$540/mo**.

### kPow \(Corporate\) - Monthly Subscription

This product is precisely the same as kPow \(Team\) but licensed for up to twelve Kafka Clusters and their associated Schema Registries and Kafka Connect clusters.

Usage is not metered and the subscriber AWS account is billed monthly at the corporate subscription price of **$940/mo.**

## **Technical Requirements**

The kPow Marketplace container makes a call to [AWSMarketplaceMetering/registerUsage](https://docs.aws.amazon.com/marketplacemetering/latest/APIReference/API_RegisterUsage.html) when kPow starts. This is required by AWS so they may check your marketplace subscription and meter your usage if you have chose to use kPow \(Pro\). This causes the following requirements:

#### ECS / Fargate / EKS Only

The AWS Marketplace container must be run in an ECS task \(including Fargate\) or an EKS pod.

#### IAM Roles

The AWS Marketplace container must run with an IAM role with permissions to call the AWSMarketplaceMetering/registerUsage API. Details for EKS and ECS follow.

## Request a BYOL License

Some customers pay for kPow via the AWS Marketplace but find the requirement to configure IAM Roles and to run in EKS / ECS / Fargate prohibitive or impossible. 

We offer subscription licenses alongside the hourly metered option for this exact use-case. If you chose a Team or Corporate Subscription but do not want to implement IAM Roles for your kPow containers then contact [**support@operatr.io**](mailto:support@operatr.io) ****and once we have verified your subscription we will provide you a **Bring Your Own License** \(BYOL\) license for the Marketplace container that averts the call to registerUsage and allows you to run kPow without configuring IAM roles and in environments other than EKS / ECS / Fargate.

With this option AWS acts solely as a billing agent for your usage of kPow.

## Start a Subscription to kPow on the AWS Marketplace

Getting started is easy, just choose a product from our [Marketplace Seller Profile](https://aws.amazon.com/marketplace/seller-profile?id=ab356f1d-3394-4523-b5d4-b339e3cca9e0):

![](../.gitbook/assets/screen-shot-2021-03-26-at-4.51.28-pm.png)

Selected a product and click **'Continue to Subscribe'**:

![](../.gitbook/assets/screen-shot-2021-03-26-at-4.56.45-pm.png)

Review and accept the Operatr.IO EULA:

![](../.gitbook/assets/screen-shot-2021-03-26-at-4.57.47-pm.png)

Once your subscription is activated, click **'Continue to Configuration':**

![](../.gitbook/assets/screen-shot-2021-03-26-at-5.00.22-pm.png)

Choose **'Operatr for Apache Kafka \(Pro\)'** as the delivery method, and the latest version available.

Click **'Continue to Launch':**

![](../.gitbook/assets/screen-shot-2021-03-26-at-5.02.07-pm.png)

Click **'View container image details'** at the bottom of the launch page:

![](../.gitbook/assets/screen-shot-2021-03-26-at-5.03.59-pm.png)

See **'Pull Command Instructions'** giving you access to the kPow container for your subscription.

![](../.gitbook/assets/screen-shot-2021-03-26-at-5.05.35-pm.png)

Pull the docker image listed at the bottom of the instruction into your own docker repository, or simply use it directly in a ECS / Fargate / EKS to launch kPow instances with the correct IAM permissions.

{% hint style="warning" %}
Check your subscription regularly for new releases of kPow and update accordingly!
{% endhint %}


