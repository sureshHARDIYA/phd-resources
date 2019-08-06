# Overview

| Item            | Description                               |
| --------------- | ----------------------------------------- |
| Type of Paper   | Conference Paper                          |
| Submitted Date  | July 15, 2019                             |
| Accepted Date   | August 6, 2019                            |
| Venue           | Coimbra, Portugal                         |
| Link            | http://cs-conferences.acadiau.ca/icth-19/ |
| Conference Date | November 4, 2019 – November 7, 2019       |

# Introduction <a name="intro"></a>

The aim of this technical documentation is to provide sufficient insights for interested parties to validate prototypes developed during my Ph.D. My research falls under `software engineering` in general, however my study tries to include other fields including `health informatics`, `IoT`, and `data science`. To backup my proposed solutions for solving problem associated with my study, we have developed several web and mobile based application as prototypes. However, we must emphasis that the prototypes developed must be used as a source of inspiration or general ideas rather than complete commercial solutions.

# Outline

1. [Introduction](#intro)
2. [Architecture](#architecture)
   2.1. [Resource Server](https://github.com/sureshHARDIYA/phd-resources/blob/master/Papers/GraphQLHIE/ARCHITECTURE.md#resource-server)
   2.1. [Authorization Server](https://github.com/sureshHARDIYA/phd-resources/blob/master/Papers/GraphQLHIE/ARCHITECTURE.md#authorization-server-)
   2.1. [Mobile Client](https://github.com/sureshHARDIYA/phd-resources/blob/master/Papers/GraphQLHIE/ARCHITECTURE.md#mobile-client-)
   2.1. [Web Client](https://github.com/sureshHARDIYA/phd-resources/blob/master/Papers/GraphQLHIE/ARCHITECTURE.md#web-client-)
3. [Technologies](#technologies)
4. [Getting Started](#gettingStarted)
5. [Evaluation](#evaluation)
6. [Discussion](#discussion)
7. [FAQ](#discussion)

# Architecture <a name="architecture"></a>

The prototype contains following major components:

1. Resource Server
2. Authorization server
3. Web Client
4. Mobile Client

[A detailed description of the architecture is presented here.](https://github.com/sureshHARDIYA/phd-resources/blob/master/Papers/GraphQLHIE/ARCHITECTURE.md)

# Technologies <a name="technologies"></a>

To implement the prototype mentioned in the paper, we used several technologies. The technological decision was made based on the different studies done during the research period. The choice of these technologies [are justified in technologies section](https://github.com/sureshHARDIYA/phd-resources/blob/master/Papers/GraphQLHIE/TECHNOLOGIES.md).

# Getting Started <a name="gettingStarted"></a>

To get started with `GraphQL` [follow the tutorials written here:](https://skmukhiya.netlify.com/how-does-graphql-work/)

# Evaluation <a name="evaluation"></a>

Making an `HTTP` request to `RESTful` endpoints returns [all the attributes as shown in the response](https://github.com/sureshHARDIYA/phd-resources/blob/master/Papers/GraphQLHIE/EVALUATION.md#rest). All these attributes are not used by our self-assessment mobile application. Hence, it is referred to as `overfetching`. To solve this overfetching issue, we introduce `GraphQL`-based API. For the same request, we used `GraphQL` api to fetch [only the required attributes and the](https://github.com/sureshHARDIYA/phd-resources/blob/master/Papers/GraphQLHIE/EVALUATION.md#graphql).

# Discussion

In this section, we try to enlighten two most important challenges faced in `GraphQL` community. [Both of them are discussed here](https://github.com/sureshHARDIYA/phd-resources/blob/master/Papers/GraphQLHIE/DISCUSSION.md).

# Conclusion

# FAQs

<details>
  <summary>Can I get access to source code?</summary>
  <p> Yes, certainly you can. Email us at <a href="mailto:itsmeskm99@gmail.com">itsmeskm99@gmail.com</a> and we will give you access to the repository.</p>
</details>

<details>
  <summary>What is INTROMAT? </summary>
  <p> INTROducing Mental health through Adaptive Technology . Our vision is to improve public mental health with innovative technologies and psychological treatments. <a href="https://intromat.no/">Find more here.</a></p>
</details>

<details>
  <summary>Where to get started with GraphQL?</summary>
  <p> Start here: https://skmukhiya.netlify.com/how-does-graphql-work/</p>
</details>

<details>
  <summary>What is HL7 FHIR?</summary>
  <p> HL7 FHIR is a open standard for Health Information Exchange (HIE). <a href="http://hl7.org/fhir/">Read More here </a></p>
</details>

# References

1. <a name="1"></a>Suresh Kumar Mukhiya, Fazle Rabbi, Violet Ka I Pun, Yngve Lamo, An architectural design for creating self-reporting e-health systems. InICSE 2019Proceedings in the IEEE Digital Library(2018).
2. <a name="2"></a> Redux Quick Start Guide: A Beginner's Guide to Managing App State with Redux, James Lee, Tao Wei, Suresh Kumar Mukhiya, Packt Publishing, Feb 28, 2019
3. <a name="3"></a> Mukhiya, S. K., & Hoang Hung, K. (2018). An Architectural Style for Single Page Scalable Modern Web Application, 5(4), 6–13. Retrieved from https://www.ijrra.net/Vol5issue4/IJRRA-05-04-02.pdf
