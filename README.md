# Distributed-System-Revision

1. **We define a distributed system as one in which hardware or software components located at networked computers communication and coordinate their actions only by passing message. What are the consequences of defining a distributed system in this manner?**<br>
The definition leads to especially significant characteristics of distributed systems which are concurrency of components, lack of a global clock and independent failures of components.

---

2. **List and explain Five characteristics of Distributed System.**
- Parallel activities
  - Autonomous components executing concurrent tasks
- Communication via message passing
  - No shared memory
- Resource sharing
  - Printer, database, other services
- No global state
  - No single process can have knowledge of the current global state of the system
- No global clock
  - Only limited precision for processes to synchronize their clocks

---

3. **Explain what are the challenges faces by Distributed System.**
- Heterogeneity
  - Heterogeneous components must be able to interoperate
- Distribution transparency
  - Distribution should be hidden from the user as much as possible
- Fault tolerance
  - Failure of a component (partial failure) should not result in failure of the whole system
- Scalability
  - System should work efficiently with an increasing number of users
  - System performance should increase with inclusion of additional resources
- Concurrency
  - Shared access to resources must be possible
- Openness
  - Interfaces should be publicly available to ease inclusion of new components
- Security
  - The system should only be used in the way intended

---

4. **Explain what it means by Heterogeneity in Distributed System.**
- Heterogeneity is the variety and difference of networks, computer hardware, operating systems, programming languages, and implementations by different developers.
- Heterogeneous components must be able to interoperate across different:
  - Operating systems
  - Hardware architectures
  - Communication architectures
  - Programming languages
  - Software interfaces
  - Security measures
  - Information representation

---

5. **Explain at least Five transparency challenges for Distributed System.**
- Access transparency
  - Access to local or remote resources is identical
  - E.g. Network File System / Dropbox
- Location transparency
  - Access without knowledge of location
  - E.g. separation of domain name from  machine address.
- Failure transparency
  - Tasks can be completed despite failures
  - E.g. message retransmission, failure of a  Web server node should not bring down the website.
- Replication transparency
  - Access to replicated resources as if there was just one. And provide enhanced reliability and performance without knowledge of the replicas by users or application programmers.
- Migration (mobility/relocation) transparency
  - Allow the movement of resources and clients within a system without affecting the operation of users or applications. 
  - E.g. switching from one name server to another at runtime; migration of an agent/process from one node to another.
- Concurrency transparency
  - A process should not notice that there are other sharing the same resources
- Performance transparency:
  - Allows the system to be reconfigured to improve performance as loads vary
  - E.g., dynamic addition/deletion of components, switching from linear structures to hierarchical structures when the number of users increases
- Scaling transparency: 
  - Allows the system and applications to expand in scale without changes in the system structure or the application algorithms.
- Application level transparencies:
  - Persistence transparency
    - Masks the deactivation and reactivation of an object
  - Transaction transparency
    - Hides the coordination required to satisfy the transactional properties of operations

---

6. **List and explain three security mechanism which are implemented in Distributed System.**
- Encryption
  - E.g. Blowfish, RSA
- Authentication
  - E.g. password, public key authentication
- Authorization
  - E.g. access control lists

---

7. **Describe with example Distributed System usage in Health Care.**<br>
Health informatics, on online patient records, monitoring patients

---

8. **Discuss openness in Distributed System by giving it benefit and problem that may occur.**
- The openness of a computer system is the characteristic that determines whether the system can be extended and reimplemented in various ways. The openness of distributed systems is determined primarily by the degree to which new resource-sharing services can be added and be made available for use by a variety of client programs.
- Openness cannot be achieved unless the specification and documentation of the key software interfaces of the components of a system are made available to software developers. In a word, the key interfaces are published. This process is akin to the standardization of interfaces, but it often bypasses official standardization procedures, which are usually cumbersome and slow-moving.
- However, the publication of interfaces is only the starting point for adding and extending services in a distributed system. The challenge to designers is to tackle the complexity of distributed systems consisting of many components engineered by different people.
- Open distributed systems can be constructed from heterogeneous hardware and software, possibly from different vendors. But the conformance of each component to the published standard must be carefully tested and verified if the system is to work correctly.
 

---

9. **Describe what is fault masking which is one of the fault tolerance mechanism.**
- Some failures that have been detected can be hidden or made less severe.
  - Messages can be retransmitted when they fail to arrive. 
  - File data can be written to a pair of disks so that if one is corrupted, the other may still be correct. 

---

10. **Define Distributed System.**<br>
A system in which hardware or software components located at networked computers communicate and coordinate their actions only by message passing.

---

11. **What are the benefits of Distributed System?**
- Functional Separation:
  - Existence of computers with different capabilities and purposes:
  - Clients and Servers
  - Data collection and data processing
- Inherent distribution:
  - Information:
    - Different information is created and maintained by different people (e.g., Web pages)
  - People
    - Computer supported collaborative work (virtual teams, engineering, virtual surgery)
    - Retail store and inventory systems for supermarket chains (e.g., Coles, Woolworths)
- Power imbalance and load variation:
  - Distribute computational load among different computers.
- Reliability:
  - Long term preservation and data backup (replication) at different locations.
- Economies:
  - Sharing a printer by many users and reduce the cost of ownership.
  - Building a supercomputer out of a network of computers.

---

12. **Describe the way to handle scalability in Distributed System.**
- System should work efficiently at many different scales, ranging from a small Intranet to the Internet
- Remains effective when there is a significant increase in the number of resources and the number of users
- Challenges of designing scalable distributed systems:
  - Cost of physical resources
  - Cost should linearly increase with system size
  - Performance Loss
  - For example, in hierarchically structure data, search performance loss due to data growth should not be beyond O(log n), where n is the size of data
- Preventing software resources running out:
  - Numbers used to represent Internet addresses (32 bit->64bit)
  - Y2K-like problems
  - Avoiding performance bottlenecks: 
  - Use of decentralized algorithms (centralized DNS to decentralized)

---

13. **Explain what physical model of Distributed System is.**
- Physical Models – capture the hardware composition of a system in terms of computer hardware and interconnecting networks.
- This model representation of the underlying hardware elements of a distributed system that abstracts away from specific details of the computer and networking technologies employed
- Baseline physical model – how hardware or software components located at networked computers communicate and coordinate their action only by passing message. 

---

14. **A user arrives at a railway station that they has never visited before, carrying a Mobile Phone that is capable of wireless Networking. Suggest how the user could be provided with information about the local services and amenities at that station, without entering the station’s name or attributes. What technical challenges must be overcome?**
- Through scanning QR code
- GPS location
- Need suggestions on this part, will update later

---

15. **Due to the increasing maturity of distributed system infrastructure, organizations are moving towards viewing distributed systems as a utility. In this model, resources are provided by appropriate service suppliers and effectively rented rather than owned by the end user. Explain this model with respect to physical resources and software services. Can you give examples of some companies that support such software services?**
- Physical resources such as storage and processing can be made available to networked computers, removing the need to own such resources on their own. At one end of the spectrum, a user may opt for a remote storage facility for file storage requirements and/or for backups. Similarly, this approach would enable a user to rent one or more computational nodes, either to meet their basic computing needs or indeed to perform distributed computation. At the other end of the spectrum, users can access sophisticated data or indeed computational infrastructure using the sort of services now provided by companies such as Amazon and Google. Operating system virtualization is a key enabling technology for this approach, implying that users may actually be provided with services by a virtual rather than a physical node. This offers greater flexibility to the service supplier in terms of resource management.
- Software services can also be made available across the global Internet using this approach. Indeed, many companies now offer a comprehensive range of services for effective rental, including services such as email and distributed calendars. Google, for example, bundles a range of business services under the banner Google Apps This development is enabled by agreed standards for 
software services, for example as provided by web services.

---

16. **What is client-server computing? Which of these roles is an active role, and which is a passive one? Explain remote invocation in this context.**
- Server refers to a running program (a process) on a networked computer that accepts requests from programs running on other computers to perform a service and responds appropriately. The requesting processes are referred to as clients, and the overall approach is known as client-server computing. In this approach, requests are sent in messages from clients to a server and replies are sent in messages from the server to the clients. When the client sends a request for an operation to be carried out, we say that the client invokes an operation upon the server. A complete interaction between a client and a server, from the point when the client sends its request to when it receives the server’s response, is called a remote invocation. 
- The same process may be both a client and a server, since servers sometimes invoke operations on other servers. The terms ‘client’ and ‘server’ apply only to the roles played in a single request. Clients are active (making requests) and servers are passive (only waking up when they receive requests); servers run continuously, whereas clients last only as long as the applications of which they form a part. 
Note that while by default the terms ‘client’ and ‘server’ refer to processes rather than the computers that they execute upon, in everyday parlance those terms also refer to the computers themselves. 

---

17. **The INFO service manages a potentially very large set of resources, each of which can be accessed by users throughout the Internet by means of a key(a string name). Discuss an approach to the design of the names of the resources that achieves the minimum loss of performance as the number of resources in the service increase. Suggest how the INFO service can be implemented so as to avoid performance bottlenecks when the number of users become very large.**
- Controlling the performance loss: Consider the management of a set of data whose size is proportional to the number of users or resources in the system – for example, the table with the correspondence between the domain names of computers and their Internet addresses held by the Domain Name System, which is used mainly to look up DNS names such as www.amazon.com. Algorithms that use hierarchic structures scale better than those that use linear structures. But even with hierarchic structures an increase in size will result in some loss in performance: the time taken to access hierarchically structured data is O(log n), where n is the size of the set of data. For a system to be scalable, the maximum performance loss should be no worse than this.
- Avoiding performance bottlenecks: In general, algorithms should be decentralized to avoid having performance bottlenecks. We illustrate this point with reference to the predecessor of the Domain Name System, in which the name table was kept in a single master file that could be downloaded to any computers that needed it. That was fine when there were only a few hundred computers in the Internet, but it soon became a serious performance and administrative bottleneck. The Domain Name System removed this bottleneck by partitioning the name table between servers located throughout the Internet and administered locally.

---

18. **What is the main disadvantage of distributed systems which exploit the infrastructure offered by the Internet? How can this be overcome?**<br>
Internet-scale distributed systems: Building on this foundation, larger-scale distributed systems started to emerge in the 1990s in response to the dramatic growth of the Internet during this time (for example, the Google search engine was first launched in 1996). In such systems, the underlying physical infrastructure consists of a physical model that is an extensible set of nodes interconnected by a network of networks (the Internet). Such systems exploit the infrastructure offered by the Internet to become truly global. They incorporate large numbers of nodes and provide distributed system services for global organizations and across organizational boundaries. The level of heterogeneity in such systems is significant in terms of networks, computer architecture, operating systems, languages employed and the development teams involved. This has led to an increasing emphasis on open standards and associated middleware technologies such as CORBA and more recently, web services. Additional services were employed to provide end-to-end quality of service properties in such global systems. 

---

19. **What is the range of techniques covered by remote invocation?**
- Remote invocation represents the most common communication paradigm in DS, covering a range of techniques based on a two-way exchange between communicating entities in a distributed system and resulting in the calling of remote operation, procedure or methods as defined below:
  - Request-reply protocols (http)
  - Remote procedure calls (client server computing)
  - Remote method invocation (calling object can invoke a method in a remote object)

---

20. **Explain what omission failure is and give examples for process omission failure and communication omission failure.**
- The faults classified as omission failures refer to cases when process or communication channel fails to perform actions that it is supposed to do.
- Process omission failures: 
  - The chief omission failure of a process is to crash. It means the process has halted and will not execute any further step of its program ever.
  - Design of services that can survive in the presence of faults can be simplified if it can be assumed that the services on which they depend crash cleanly – the process either function correctly or stop.
  - Other process can detect such a crash by the fact that the process repeatedly fails to respond to invocation messages. However, this method of crash detection relies on the use of timeouts.
  - Timeout is a method in which one process allows a fixed period of time for something to occur. 
  - In an asynchronous system, a timeout can indicate only that a process is not responding in which it may:
  - Crashed, slow or the message has not arrived.

---

21. **What are the class of Failure propose by Hadzilacos and Toueg(1994)?**
- Hadzilacos and Toueg(1994) provide taxonomy that distinguishes between the failures of processes and communication channels. 
- These are :
  - Omission failures
  - Arbitrary failures
  - Timing failures

---

22. **Describe the security threat that could happen to a Distributed System.**
- The enemy
  - Enemy sometimes also known as the adversary that capable of sending any message to any process and reading or copying any message sent between a pair of processes. 
  - The enemy run program that generate message that make false request to services, purporting to come from authorized user. The attack may come from a computer that is legitimately or unauthorized that connected to the network.
  - The potential threats include threats to processes and threats to communication channels.
- Threat to process
  - Process that is designed to handle incoming request my receive a message from any other process in the DS and it cannot necessarily determine the identity fo the sender. Even there is communication protocols such as IP do include the address of the source computer in each message but it is not difficult for an enemy to generate a message with a forged source address. 
  - The lack of reliable knowledge of the source of a message is a threat to the correct functioning of both servers and client. 
  - Example like spoofing the mail server where enemy send unrelated mail to the original invocation.
- Threat to gateway
  - An enemy can copy , alter or inject messages as they travel across the network and its intervening gateway. 
  - Such attacks present a threat to the privacy and integrity of information as it travels over the network and to the integrity of the system
  - For example:
  - A result message containing a user’s mail item might be revealed to another user or might be altered to say something quite different. 
  - Enemy also can save copies of messages and to replay them at a later time, making it possible to reuse the same message over and over again. 
  - Example: Resending an invocation message requesting a transfer of a sum of money from one bank account to another. 
- Denial of service: This is a form of attack in which the enemy interferes with the activities of authorized users by making excessive and pointless invocations on services or message transmissions in a network, resulting in overloading of physical resource (network, CPU). Such attacks are usually made with the intention of delaying or preventing actions by other user.
- Mobile code: Process receives and executes program code from elsewhere such as email, where the code may play a Trojan horse role, purporting to fulfil an innocent purpose but the fact including code that accesses or modified resources that are legitimately available to the host process but t not to the originator of the code. 
