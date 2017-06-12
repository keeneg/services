---

copyright:

  years: 2015, 2017
lastupdated: "2017-5-01"

---

{:new_window: target="_blank"}  
{:shortdesc: .shortdesc}


# Service credentials
{: #service_credentials}

Cloud Foundry services can generate a service key, also known as a service credential. Service credentials are service-specific and vary based on how each service defines the credentials they need to generate. A service credential might contain a user name, password, host name, port and a url. However, the contents of each service credential is unique to the service that generates it. Some services might generate additional data that requires paramaters to be passed in. For example, a service might require you to input a language parameter to set the default language returned in the service key that's generated. 

## Add a new service credential
{: #add_service_credentials}

You can generate a new set of service credentials for cases where you want to manually connect an external consumer to a Bluemix service. For example, if you are trying to bind an AWS app to a Watson service, you'll need to generate a new service credential that can be used to bind these two services together.

To add a new service credential:

1. From the service details page, select the Service Credentials tab, and click **New Credential + **.
2. From the Add New Credential dialog, provide a **Name**.
3. Optionally, you can provide additional parameters as a valid JSON object containing service-specific configuration parameters, provided either in-line or in a file.

  **Note**. Most services do not require additional parameters, and for services that do, each service defines its own unique list of parameters. For a list of supported configuration parameters, see the documentation for the particular service offering.
4. Click **Add** to generate the new service credential.
