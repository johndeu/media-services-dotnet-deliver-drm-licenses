---
services: media-services
platforms: dotnet
author: Juliako
---

# This Repository is for the legacy v2 API which is now deprecated. Customers should migrate to use the v3 API only.

Please use the latest v3 API for .NET. 
- [Configure the v3 API for .NET](https://docs.microsoft.com/en-us/azure/media-services/latest/configure-connect-dotnet-howto)
- See the v3 Tutorials [Tutorial: Encode a remote file based on URL and stream the video - .NET](https://docs.microsoft.com/en-us/azure/media-services/latest/stream-files-dotnet-quickstart)
- Check out the [v3 .NET Samples repo](https://github.com/Azure-Samples/media-services-v3-dotnet)

The new .NET SDK is located here in Nuget
https://www.nuget.org/packages/Microsoft.Azure.Management.Media/

To install the newest SDK using the .NET CLI
```
dotnet add package Microsoft.Azure.Management.Media
```

## IMPORTANT! Update your Azure Media Services REST API and SDKs to v3 by 29 February 2024

Because version 3 of Azure Media Services REST API and client SDKs for .NET and Java offers more capabilities than version 2, we’re retiring version 2 of the Azure Media Services REST API and client SDKs for .NET and Java. We encourage you to make the switch sooner to gain the richer benefits of version 3 of Azure Media Services REST API and client SDKs for .NET and Java. Version 3 provides: 

### Action Required:
To minimize disruption to your workloads, review the migration guide to transition your code from the version 2 to version 3 API and SDK before 29 February 2024. 

After 29 February 2024, Azure Media Services will no longer accept traffic on the version 2 REST API, the ARM account management API version 2015-10-01, or from the version 2 .NET client SDKs. This includes any 3rd party open-source client SDKS that may call the version 2 API.  

See [Update your Azure Media Services REST API and SDKs to v3 by 29 February 2024](https://azure.microsoft.com/en-us/updates/update-your-azure-media-services-rest-api-and-sdks-to-v3-by-29-february-2024)

# (Deprecated) Use Azure Media Services to deliver PlayReady and/or Widevine licenses with .NET
## This sample will be retired after 29 February 2024. Please migrate to the v3 API

Azure Media Services (AMS) enables you to ingest, encode, add content protection, and stream your content (see this article for details). However, there are customers who only want to use AMS to deliver licenses and/or keys and do encoding, encrypting and streaming using their on-premises servers. This samples shows how to configure AMS to deliver PlayReady and/or Widevine licenses.

For detailed information about the sample, see [Use AMS to deliver PlayReady and/or Widevine licenses or AES keys](http://azure.microsoft.com/documentation/articles/media-services-deliver-keys-and-licenses/).

## How To Run This Sample

To run this sample you will need:

- Visual Studio 2013 or 2015
- An Internet connection
- An Azure subscription
- Latest Azure Media Services .NET SDK (which will be installed when you re-build the project).

### Step 1:  Clone or download this repository.

### Step 2: Update the app.config file

Update the appSettings section of the app.config file with values of your Azure Media Services account.

		  <appSettings>
		    <add key="MediaServicesAccountName" value="MediaServicesAccountName" />
		    <add key="MediaServicesAccountKey" value="MediaServicesAccountKey" />
		    <add key="Issuer" value="http://testacs.com" />
		    <add key="Audience" value="urn:test" />
		  </appSettings>
		  
### Step 3: Get at least one streaming unit

Get at least one streaming unit for the streaming endpoint from which you plan to delivery your content. For more information, see: [configure streaming endpoints](http://azure.microsoft.com/documentation/articles/media-services-dotnet-get-started/#configure-streaming-endpoint-using-the-portal)

### Step 4:  Run the sample

Clean the solution, rebuild the solution, and run it. 


## About the code

For more information, see  [Use AMS to deliver PlayReady and/or Widevine licenses or AES keys](http://azure.microsoft.com/documentation/articles/media-services-deliver-keys-and-licenses/).

## More information

You can view AMS learning paths here:

- [AMS Live Streaming Workflow](http://azure.microsoft.com/documentation/learning-paths/media-services-streaming-live/)
- [AMS on Demand Streaming Workflow](http://azure.microsoft.com/documentation/learning-paths/media-services-streaming-on-demand/)
