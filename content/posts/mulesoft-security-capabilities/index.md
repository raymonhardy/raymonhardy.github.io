+++
title = 'Mulesoft Security Capabilities'
date = 2023-06-28T07:07:07+01:00
tags = ['Security','Cloud Security', 'Mulesoft','API']
draft = false
images = [ "api_tokenization.jpg.jpg", "image_02.png" ]

+++

After working with Mulesoft for a while, I wanted to write this blog post because I didn't see very many resourse that were comprehensive on Mulesoft and it's security capabilities. Many of these findings were by google searching, reviewing Mulesoft documentation and talking with Mulesoft reps for security capabilities. This post is not intented to include all of Mulesoft security capabilities but is just good starter for those looking to use Mulesoft security.

### Mulesoft Documentation

The Mulesoft Docs will be your best friend. The Mulesoft documentation is very handy when applying security capatibilities to your environment. The location of these docs are located here: [Mulesoft Docs General](https://docs.mulesoft.com/general/).

****

## Mulesoft Basic Background

I am going to just go over some basic knowledge of Mulesoft and certain vocabulary that is good to know. This is only basic information but to just give you some background.

### Mulesoft Cloud Implemenations

If you are selecting a hosting platfrom type based on the industry and security requirements needed. It is important to select the right implementation. Mulesoft cloud options are:

- Full Cloud:
  - CloudHub 1.0/2.0:
    - Location:
      - US Cloud
      - EU Cloud
- Hybrid Cloud:
  - Runtime Fabric - Kubernetes Cluster
- Private Cloud
  - Anypoint Platform Private Cloud Edition
- Government Cloud
  - MuleSoft Government Cloud

If you are coming into a cyber security role after selection of the hosting option is already done it is very crucial to know your Mulesoft environment your organization has. Know specifically Anypoint Hosting type as well as where your control and runtime plane are.

### API Types

Mulesoft recommends creating and deploying API types in mind. Here are Mulesoft recommendations: [Type of APIs](https://www.mulesoft.com/resources/api/types-of-apis).

I broke them down into how I see them.

- Experience - Public APIs that the end user will be interacting with.
- Process - Middle man APIs configure and push data to the internal APIs (System APIs)
- System - Internal APIs that interact with the backend servers and do the heavy lifting.

Knowing what API type is essential when assessing security risk and what policies to put into place for them.

### Other Key Areas

- Design Center - Place to create, design and configure APIs using RAML files.
- Exchange - Location to see all API assets and use for documenation of APIs.
- Access Managment - User provisioning and logging.
- API Manager - Location to do API administration and policies.
- Runtime Manager - Location to view all checked in APIs currently running live.

****

## Mulesoft Security

### Anypoint Security

If you pay for Mulesoft top tier you will get some out of the box security features. Consult with your Mulesoft administrator or rep to see if what tier you might have. Many them are included here: [Anypoint Security](https://docs.mulesoft.com/anypoint-security/).

#### Edge Policies

Here you can apply security settings on the edge similar to CDN capabilities. Things such as provides denial-of-service (DoS), IP allowlists, HTTP limits, and Web Application Firewall (WAF) policies to protect your APIs. If you do not use a CDN for your web apps or APIs

#### Tokenization

If you are transmitting sensitive data for example credit card data and currently don't use a seperate tool for tokenization Mulesoft has capabilities to tokenize the data to scope out compliance requirements. A good example of how to implement tokenization is represented here:

![Mulesoft Implementation](/posts/mulesoft-security-capabilities/images/api-tokenization.jpg)


#### Secrets Manager

Lastly if you need a secrets manager to control access to private keys, passwords, certificates, and other secrets.

Secrets manager can store and manage the following secret types:

- TLS Context
- Keystore
- Truststore
- Certificates
- Certificate Pin Set
- CRL Distributor

### API Manager - Policies

There are a variety of methods to apply to individual APIs or all APIs.

Policy Implementation Types:

- Autmoated policies - Method to apply globally baseline policies to all Mulesoft APIs.
- Manual Policies - Method to apply unique policies to individual APIs or specific group of APIs.

Depending on the security requirements of the organization and if they have certain policies to apply Mulesoft has options to configure them.

Policy Configuration Types:

- Included Policies - Policies that are included out of the box with certain thresholds.
- Custom Policies -  Policies that can be adjusted to certain thresholds by the user.

To apply these policies you will need select the certain API or APIs (automated policies) that you want to apply these policies on within the API Manager. Review with your Mulesoft admin and Software developers these policies [Mulesoft Policies](https://docs.mulesoft.com/gateway/1.4/policies-included-directory).

### API Governance - Rulesets

Mulesoft gives the ability to apply certain API governance rulesets to give security results or compliance guidances on Mulesoft APIs within the Mulesoft Design Center. This helps to find certain security requirements or vulnerabilities and even quality issues found within the API RAML file or API configuration. This feature is still relatively new from the time of this blog post.

To apply these Rulesets and get the results in Design Center you will apply certain tags to the APIs you want to apply to. You will need access to the API Governance center and be able to create a new Profile. These rulesets then use tags to apply the rulesets on.

Mulesoft also lets you create custom rulesets if there is a specific requirement your organziation is looking for.

Some helpful out of the box rulesets for security include:

- Authentication Security Best Practices
- HTTPS Enforcement
- OWASP API Security Top 10 2019 Checklist

![Alt text](/posts/mulesoft-security-capabilities/images/mulesoft-rulesets.jpg "a title")

[Mulesoft Exchange](https://www.mulesoft.com/exchange/?search=&type=ruleset)

### MQ Queue Encryption Configuration

With Mulesoft you have the capability to enrypt all messages in the queue. This feature is very useful for sensitiv information sent to that queue and will be stored temporarily. You will have to work work with other departments to see if that data will be sensitive or not. Mulesoft also has the option to encrypt those messages in rest as well.

Here is a useful link to that confiruation for the encrypting queues: [Mulesoft Queue Encryption](https://docs.mulesoft.com/mq/mq-understanding#encrypt_queue).

****

## Conclusion

Like I mentioned above this is just a basic starter into Mulesoft security configurations. There a plenty more and detailed areas to configure your APIs. I hope this helps someone looking to make those security configurations and can give a good jump start into Mulesoft capabilities as a API gateway.


