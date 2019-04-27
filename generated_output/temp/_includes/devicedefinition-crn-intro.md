
{% assign id = {{page.id}} %}

{{site.data.structuredefinitions.[id].description}}

#### Scope and Usage

The profile is to be used for the WHT CRN project to capture the specific device information that is the present in the GUDID database for devices used to treat women with various health conditions.

#### Mandatory Data Elements and Terminology

The following data-elements are mandatory (i.e data MUST be present).

**must have:**

1. manufacturer

**Additional Profile specific implementation guidance:**

When available, the DeviceDefinition data elements manufacturer, deviceName, modelNumber and type should be populated when found in the GUDID database using the deviceIdentifier. 

In order to retrieve the AccessGUDID data the following APIs should be used: 

* The Device Lookup API [GET /devices/lookup (https://accessgudid.nlm.nih.gov/resources/developers/device_lookup_api)] allows users to retrieve the Manufacturer.Organization.name (returned as companyName), deviceName (retuned as brandName), and modelNumber (returned as versionModelNumber) by sending the device identifier.
* The Device SNOMED API [GET /devices/snomed (https://accessgudid.nlm.nih.gov/resources/developers/device_snomed_api)] allows users to retrieve the device type – i.e., the SNOMED code and term by sending the device identifier.  

Note: Implementer must generate a UMLS single-use ticket to retrieve the coded value.

