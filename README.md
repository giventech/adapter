## Collateral Adapter Spring Boot SOAP endpoint

This endpoint is a proof of concept to validate integration of third party application with the Collateral Management Solution

## Key feature required 

 - SOAP XSD definition
 - WSDL Generation from XSD
 - Basic Authentication via HttpInterceptors
 - Cloud native support (Docker+ Kubernetes)
 - Discoverability via API gateway (e.g. IBM API connect
  
## Contract first approach

The contract to perform a Collateral REST API call is based on  XSD definition.
The Spring Boot application exposed the contract  WSDL.
Client and  3rd party application can form requests based on basic authentication  
  
## Security options:

- User password authentication
(https://tutorialflix.com/How-to-implement-security-in-SOAP-webservice-using-Spring-WS/)
- Certificated bases authentication 
(https://zoltanaltfatter.com/2016/04/30/soap-over-https-with-client-certificate-authentication/)

The current solution used basic authentication. It is specified both in SOAP and HTTP headers
Note: The Basic authentication is for proof of concept security protocols.

## Resolutions to issues:

Dependencies to JAF 1.0.2 must be resolved manually as it is not availaible from maven central repository
This dependency must be added to artifactory.

Library is available from maven repository below

 <repositories>
        <repository>
            <id>adobe-public</id>
            <url>https://repo.adobe.com/nexus/content/repositories/public/</url>
        </repository>
 </repositories>
 
 OR
 
 https://www.oracle.com/java/technologies/java-archive-downloads-java-plat-downloads.html#license-lightbox
 