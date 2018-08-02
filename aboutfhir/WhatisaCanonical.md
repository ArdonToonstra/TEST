# What is a Canonical?

A canonical, or canonical URI, is a globally unique identifier for FHIR conformance resources: the resources that define the communication between systems.

## Context
When two health care systems communicate using FHIR, they send resources over the wire that conform to a certain definition: a so called Structure Definition. That's why the definition is sometimes called a conformance resource. To make sure that everybody in the world understands what that definition is precicely, each conformance resource has canonical name, which also serves as a globally unique identifier.

## URI
A canonical is an URI (a uniform resource locator), but usually it is a URL: a link. Which is also a URI. When it is a link there are three nice things that allow the author to communicate. 
Firstly, it is common practice to use the website domain of the owning organization in the canonical, to indicate who made. So conformance resources from HL7 all look like this:
```
    http://hl7.org/fhir/StructureDefinition/Patient
```
It also makes it easier to avoid conflicts with other authors, since they will never create a canonical that starts with the same base.

Secondly, it is now possible to set up a documentation site, where that canonical resolves to if you  would give it to your browser.

## Resolving
Not all canonical resolve directly to an actual website, and are therefore only used for identifying a conformance resource. Simplifier can resolve the canonical URLs of all resources that we have. You can use this page to do a manual resolve.
```
    simplifier.net/resolve
```
But you can also use this as a link resolver in your own site
```
    simplifier.net/resolve?url=<your url>
```
