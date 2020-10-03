
## Collateral Adapter Spring Boot SOAP endpoint


This endpoint is a proof of concept to validate integration of third party application to the Collateral Management Solution

## Key feature required 

 
 - SOAP XSD definition
 - WSDL Generation from XSD
 - Basic Authentication via HttpInterceptors
 - Cloud native support (Docker+ Kubernetes)
 - Discoverability via API gateway (e.g. IBM API connect)
  
 
  
## Contract first approach

For SOAP clients of collateral platform the Collateral Adapter 
provide Webservice Contract and Endpoint
Unlike  
  
## Security options:

- User password authentication
(https://tutorialflix.com/How-to-implement-security-in-SOAP-webservice-using-Spring-WS/)
- Certificated bases authentication 
(https://zoltanaltfatter.com/2016/04/30/soap-over-https-with-client-certificate-authentication/)


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