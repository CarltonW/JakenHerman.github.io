---
layout: post
title: How to setup Azure VPN
excerpt: "How to setup Azure VPN back to your on-premises environment"
modified: 2020-11-19
tags: [Howto,Azure,VPN,gateway]
comments: true
image:
feature: sample-image-2.jpg
categories: [Azure]
---

If you're just getting started using Azure one of the first things you might be asked to do is create a site-to-site vpn connection between your on-premises network and Azure. In this post I will walk through setting up an Azure VPN with an on-premises network. Before we get started there are some requirements for your on-premises environment.<br>

>### __On-Premises Requirements__
>
>- **On-premises endpoint** 
>- **On-premises public IP**
>- **On-premises private subnet**
<br/>

>### __Resources required in Azure to setup a Site-to-Site VPN__
>
>- **Virtual Network Gateway**
>- **Virtual Network**
>- **Local Network Gateway**
>- **Public IP address**
>- **Connection**

<br>
<br>
<center>The Virtual Network Gateway is the resource that ties all of other components together when setting up your VPN. Let's get started creating that resource. From the portal choose <b>Create new Resource<b> and search for "Virtual Network Gateway".</center> 
![Find Virtual Network Gateway in Azure](/img/azurevpn/001-CreateVirtualNetworkGateway.png "Azure Portal find Virtual Network Gateway")
<br>
<br>
![Create Virtual Network Gateway in Azure](/img/azurevpn/1-CreateVirtualNetworkGateway.png "Azure Portal create Virtual Network Gateway")
<br>
<br>
![Virtual Network Gateway Settings in Azure](/img/azurevpn/2-VirtualNetworkGatewayPart1.png "Azure Portal Virtual Network Gateway settings")
<br>
<br>
![Create the Virtual Network in Azure](/img/azurevpn/3-CreateVirtualNetwork.png "Azure Portal create Virtual Network")
<br>
<br>
![Create the Virtual Network Gateway check SKU in Azure](/img/azurevpn/4-CreateVnetGateway2.png "Azure Portal create Virtual Network Gateway check SKU")
<br>
<br>
![Confirm Virtual Network Gateway settings in Azure](/img/azurevpn/5-VNetGatewayConfirm.png "Azure Portal Confirm Virtual Network Gateway settings")
<br>
<br>
![Virtual Network Created in Azure](/img/azurevpn/6-VnetCreated.png "Azure Portal Virtual Network Created")
<br>
<br>
![Add local network gateway in Azure](/img/azurevpn/9-AddLocalNetworkGateway.png "Azure Portal add local network gateway")
<br>
<br>
![Choose local Network gateway in Azure](/img/azurevpn/10-ChooseLocalNetworkGateway.png "Azure Portal choose local network gateway")
<br>
<br>
![Create local network gateway in Azure](/img/azurevpn/11-CreateLocalNetworkGateway.png "Azure Portal create local network gateway")
<br>
<br>
![Enter subnet for Local network in Azure](/img/azurevpn/12-LocalNetworkGateway.png "Azure Portal setup local subnet for on-prem network")
<br>
<br>
![Add Connection in Azure](/img/azurevpn/13-AddConnection.png "Azure Portal add Connection")
<br>
<br>
![Create connection between on-prem and Azure](/img/azurevpn/14-CreateConnection.png "Azure Portal create connection between on-prem and vnet")
<br>
<br>
![Settings for Connection in Azure](/img/azurevpn/15-ConnectionSave.png "Azure Portal settings for Connection before saving")
<br>
<br>
![Verify connection settings in Azure](/img/azurevpn/16-VerifyConnectionSettings.png "Azure Portal verify connection settings")
<br>
<br>
![VPN resources are now created in Azure](/img/azurevpn/17-ConnectionCreatedAllResources.png "Azure Portal all resources required for VPN")
<br>
<br>
![Download configuration for local router setup in Azure](/img/azurevpn/18-DownloadConfig.png "Azure Portal download config file for local network")
<br>
<br>
![Verify device type before download in Azure](/img/azurevpn/19-ChooseRouterType.png "Azure Portal verify device type before download")
<br>
<br>
![Complete settings for on-prem network device in notepad](/img/azurevpn/20-ConfigSettings.png "settings necessary for on-prem network device setup")
<br>
<br>
![VPN is now connected to Virtual Network Created in Azure](/img/azurevpn/21-VPNConnected.png "Azure Portal Virtual Network Created")

<br>
<br>
>__References:__<br>
[https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpn-gateway-settings](https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpn-gateway-settings)<br>