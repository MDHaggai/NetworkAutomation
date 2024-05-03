#Phase 1: Start read-only processes


Phase 1 provides basic functionality through three functions: the automation orchestration system, the UI and the device abstraction layer. This phase starts with automated, read-only processes that archive configurations, collect troubleshooting data and validate network configurations against templates.

The elements in Phase 1 include the following:


Automation orchestration:

The core orchestration engine controls the automation process. It includes scaling features, like parallel processing and distributed agents. Several commercial products and open source packages are available to perform this function.


UI:

Commercial products usually feature a GUI and an API, which is critical for later phases of automation. Open source projects might rely on a command-line interface for administrative control and an API for programmatic control.


Abstraction layer:

The abstraction layer provides a model that hides the differences between device vendors, greatly simplifying the network device interface. The abstraction layer might be built into some orchestration systems.







#Phase 2: Add a network source of truth






Phase 2 adds a network source of truth (NSoT) database and an interface to a trouble-ticketing system. The elements in this phase include the following:


NSoT database:

The NSoT stores information about the desired network state that the automation orchestration system uses to validate -- and, in later stages, correct -- the network's operation. This data might include address assignments, network protocol neighbors, interface operational state and reachability.


Automatic trouble ticketing:

An interface to a trouble-ticketing system enables the automation orchestration system to create tickets when the network state and the NSoT differ. Remediation is initially manual but becomes increasingly automated as the organization matures.






#Phase 3: Store configuration templates and scripts






Phase 3 begins the transition to an infrastructure-as-code operational model. The elements in this phase include the following:



Source code management repository:

A source code repository, typically based on Git, is used to store configuration templates, saved configurations and scripts. It is tightly integrated with the automation orchestration system to build device configurations from stored templates and NSoT data -- for example, generating the configurations for all network equipment for a data center pod.


Workflows:

Phase 3 is where the workflows begin transitioning from manual to automated. Workflows might be instantiated through scripts that are stored in the source code repository. Commercial products often provide multiple mechanisms for controlling workflows, including graphical editors and APIs.


Chatbots:

Chatbots enable the automation system to communicate workflow and state information to unified communications chat rooms in which network staff collaborate on implementation and troubleshooting. This is a particularly effective mechanism for distributed network teams where members might work remotely.





#Phase 4: Implement network feedback






Phase 4 provides a feedback mechanism from the network. Up to this point, the network has provided little feedback, except for validation checks against the NSoT data. The elements in Phase 4 include the following:


Telemetry and monitoring:

Historically, network monitoring has relied on Simple Network Management Protocol, but more modern implementations use streaming telemetry. Networks will need to use both mechanisms for some time to come.


Monitoring and management databases:

The monitored data needs to be stored somewhere, either in a relational database for relationship-type data -- such as device type and interface list -- or in a time-series database for interface performance variables.
Action triggers. Monitoring the network is beneficial only if the results drive responses. Action triggers use either rule sets or machine learning to detect anomalies, issue alerts and open trouble tickets. More advanced implementations trigger automated workflows to begin remediation without human intervention, such as routing around a failed link.






#Phase 5: Automate change testing and validation





Phase 5, the last phase in the architecture, is to automate change testing and validation. Here's what's involved:


Virtual network testing:

The principal driver of network change control is the practice of testing a change in the lab before deploying it into production. The lab uses virtual, software-simulated devices to model the production network's key parameters. Proposed changes instantiate the virtual network, run pre-change tests to validate the lab is functioning as intended, apply the change, and run post-change tests to validate the desired result was achieved.


Change validation testing:

If the virtual network testing succeeds, the change can be applied to the production network. The release follows the same three-step process: validation of the pre-change state, application of the change and then post-change validation of the resulting state.
The end goal


  The network automation architecture described in this project is a framework. Network teams can modify it to fit their organization's needs and to accommodate the capabilities of the tools they select.

   The eventual goal is to build a continuous integration, continuous delivery and continuous deployment process in which small, well-defined network changes are automatically deployed only after passing stringent tests. This practice, known as NetOps or NetDevOps, enables teams to migrate their network to infrastructure as code using many of the same concepts and techniques as successful software development methods.
