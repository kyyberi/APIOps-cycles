## Before starting to build APIs

*   <ac:link><ri:page ri:content-title="1\. API Canvas"></ri:page></ac:link> - APIs business requirements, API consumers, services needing to be built and the existing services available as API canvas?
*   <ac:link><ri:page ri:content-title="2\. Minimum Viable API Architecture (MVAA)"></ri:page></ac:link> - non-functional and funcational requirements should have been gathered using the design templates?
*   Also check the <ac:link><ri:page ri:content-title="4\. API Audit"></ri:page></ac:link>and <ac:link><ri:page ri:content-title="API design style guide"></ri:page></ac:link> for guidelines on implementation
*   Design application architecture based on the environment where the API -backends are build. Estimate runtime costs at this point.
*   Setup automatical deployments, test-automation and API publishing pipelines (this requires own guide when environment and API management platform has been selected)

## Azure API apps and Functions (serverless)

*   More information [<u>https://azure.microsoft.com/en-us/services/app-service/api/</u>](https://azure.microsoft.com/en-us/services/app-service/api/)
*   Toolchain can be selected depending on which environments used (Team server or some others, version control and deployments recommended with Git)
*   Publishing automated with MSDeploy publishing profiles
*   Runs in Azure
*   Provides OpenAPI (swagger) documentation, so can also be used with other API management solutions, if necessary (note that connection needs to be secured between Azure and possible external API management)
*   Serverless architecture with <u>[https://azure.microsoft.com/en-us/services/functions/](https://azure.microsoft.com/en-us/services/functions/)</u><span style="color: rgb(80,80,80);"> which supports several languages, including JavaScript, C#, F#, as well as scripting options such as Python, PHP, Bash, Batch, and PowerShell</span>

## IBM Bluemix, LoopBack, StrongLoop and OpenWhisk (serverless) and Serverless

*   More information [<u>https://strongloop.com/</u>](https://strongloop.com/)
*   Node -applications, can be a combination of other Bluemix services like Watson, IoT or Message Hub
*   Toolchain can be selected depending on which environments used (Jenkins, Travis etc, version control and deployments recommended with Git)
*   Provides OpenAPI (swagger) documentation.  Can also be used with other API management solutions although it's not recommended as it does not really add value as the StrongLoop apps need to be protected anyway with Bluemix API management and connection needs to be secured between Bluemix cloud, dedicated or local and possible external API management)
*   Serverless architecture with <u>[https://console.ng.bluemix.net/openwhisk/](https://console.ng.bluemix.net/openwhisk/)</u>

## AWS microservices and Lambda (serverless)

*   More information <u>[AWS Lambda](http://docs.aws.amazon.com/lambda/latest/dg/with-on-demand-https-example-configure-event-source_1.html)</u>
*   AWS Lambda supports code written in Node.js (JavaScript), Python, Java (Java 8 compatible), and C# (.NET Core)
*   can be combination of different services within AWS like DynamoDB, SQS, SES etc.
*   Toolchain can be selected depending on which environments used (Jenkins, Travis etc, version control and deployments recommended with Git)
*   Lambda APIs need to be published via AWS API gateway, which also provides automatically OpenAPI (swagger) documentation. Publishing with API management services which are running outside AWS requires a TLS secured connection with certficates between AWS API gateway and API management service (this is not supported in all public cloud deployed API management services)