---
services: media-services
platforms: dotnet
author: Juliako
---

# Use Azure Media Services to deliver PlayReady and/or Widevine licenses with .NET

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
