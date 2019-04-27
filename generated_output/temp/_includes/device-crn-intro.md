
{% assign id = {{page.id}} %}

{{site.data.structuredefinitions.[id].description}}

#### Scope and Usage

The profile is to be used for the WHT CRN project to capture the specific device information used to treat women with various health conditions.

#### Mandatory Data Elements and Terminology

The following data-elements are mandatory (i.e data MUST be present).

**must have:**

1. identifier
1. patient

**Additional Profile specific implementation guidance:**

The udiCarrier can only contain either carrierAIDC or carrierHRF along with its appropriate entryType.
In case an organization wants to represent both carrierAIDC or carrierHRF, then multiple udiCarrier entries must be used.
Also refer to the invariants present on the various data elements in the profile.

In order to parse the UDI – the AccessGUDID Parse UDI API should be used: GET /parse_udi (https://accessgudid.nlm.nih.gov/resources/developers/parse_udi_api).

The Parse UDI API allows users to pass a UDI and return each part of the UDI in a structured format (specifically the serialNumber, lotNumber, expirationDate, distinctIdentifier (returned as donation_id) or manufacturineDate).
