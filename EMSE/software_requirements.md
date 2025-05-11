# EMSE: Software Requirements 
## Lecture 1: Introduction
### Why Software Requirements?
*„The hardest single part of
building a software system is
deciding precisely what to
build.* - Fred Brooks

- Fixing errors at the requirements stage reduces costs significantly, compared to dragging them through until software operation (curve from 1x at requirements to 150x at production/operational stage, cost increases throughout development process)
- Study by gartner:
- - Common Project failure factors include **incomplete requirements** and no customer requirements
- - Common project success factors include **customer involvment**, and a **clear statement of requirements**

_How can we find out, what the customer requires from our software?_

- Empirical research: **Observation + Data, systematically!**
- - Meaning: What protocol, what data has been collected how, what did you do to remove potential biases? Is there awareness about internal and external biases?
- - Goals: Explore (Understand phenomena and identify problems) and Evaluate (check/improve hypotheses, measure impact)
- - Strategies: Qualitative and Quantitative, both are important, combining them is common (methodological pluralism, triangulation)
- Threats to validity of empirical studies (Seminar)

- Requirements are ever changing, this change must be managed
- You can do too much ("Analysis paralysis")

### Types of Requirements:
- Functional
- - requirements regarding result of behaviour of functions of the systems
- Nonfunctional
- - Not directly related to functional behaviour, phrased as constraints or negative assertions 
- - Constraints
- - - Limit the solution space beyond what is necessary for meeting given functional and quality requirements
- - Quality requirements (ISO 25010)
- -	- Maintainability, Usability, Reliability, Adaptability, Security, Compatibility, Suitability, Performance, Portability...

#### _Requirements is about asking the right questions_
**Questions need to be asked about:** 

- users
    * What type of users? How many types?
    * What training required for users?
    * easy to learn important?
    * protect users from errors?
    * what IO devices are available?
    * what kind of documentation for who?
- hardware
    * for what hardware is the system going to be?
    * characteristics (ram, storage, cpu, network)
- performance
    * speed, throughput, response time constraints?
    * size/capacity constraints?
- system interfaces
    * input from systems outside?
    * output going to systems outside?
    * format or medium constraints?
- quality
    * requirements for reliability/availability
    * fault tolerance and detection
    * acceptable dowwntime per 24h
    * restart time
    * response to input errors
    * response to extreme conditions
- environment
    * Physical: where, how many sites, conditions
    * system modifications? what will change likely?
    * security issues: physical security? data access control?...
- maintenance and operation
    * Backups, installation, maintenance
- data
    * What data? why? 
    * what collection processes, labelling and prep?
    * data quality? smells?
    * quality oflabellers?
- ...

Questions are typically answered during elicitation and analysis

### Requirements engineering
Software engineering is a subset of Systems engineering
Software engineering is a modelling and problem-solving activity, which is knowledge intensive and rationale driven

Definition **Requirement**: “a statement of **what** the system must do, how it must **behave**, the
**properties** it must exhibit, the **qualities** it must possess, and the
**constraints** that the system and its development must satisfy”

Definition **Requirements Engineering** (RE): branch of systems engineering concerned with

- desired **properties** and **constraints** of software-intensive systems
- **goals** to be achieved in the software's environment
- **assumptions** about environment

**Basically: formulating, documenting and maintaining software requirements**

#### Views on RE: 

- Engineering view: systematic and repeatable techniques that ensure completeness, consistency and relevance of requirements
- Lifecycle view: Discovery of purpose by identifying stakeholders and their needs, documenting them in a way that is amenable to analysis, communication/discussion and implementation
- Knowledge view: making/documenting/dealing with decisions about functionality of a system

#### Activities of RE:

- Requirements elicitation/development: discovering, understanding the user's needs and constraints
- Requirements analysis: refining needs and constraints, as understood by developers. results in technical specification/analysis model, formal/semiformal notation (UML)
- Requirements specification: clear and precise documentation, end result of elicitation, natural language
- Requirements verification: Ensuring completeness, correctness, consistency and clarity of requirements
- Requirements Management: scheduling, negotiating, coordinating, documenting RE activities

RE process consists of formulating, documenting and maintainging SW requirements
most important tools: common sense and creativity, making it as easy as possible

#### RE (soft) skills
- Analytical thinking
- Empathy
- Communication skills
- Conflict resolution skills
- Moderation skills
- Self-confidence
- Persuasiveness

#### Requirements Elicitation vs Analysis:
- Elicitation: Definition of systems in terms understood by user/customer -> yields Requirements Specification (natural lang)
- Analysis: Definition of systems in terms understood by developer -> yields Technical Specification/Analysis Model ([semi-]formal like UML, Z..)
- **RE process combines both activites!**

#### Types of Req Elicitation
- Greenfield Engineering
    * from scratch, no prior system
    * triggered by user needs, reqs come from users and clients

- Re-engineering
    * redesign/reimpl of existing systems using new tech
    * triggered by tech enabler

- Interface engineering
    * existing service into a new environment
    * triggered by tech enable or new market needs

#### Req Eli challenges
- accurate communication
    * gap between users (app domain knowledge) and devs (solution domain knowledge)
    * challenges:
        + Identifying appropriate system
        + Providing unambiguous spec
        + Leaving out unwanted features
        + Defining system boundaries

#### Main Req Eli techniques
Goal: bridging gap between user and dev

- Interview/Surveys: pre-selected questions to be answered by users
- Observation: observing users in their operational environment
- Scenario: use of the system as a series of interactiong between user and system
- Use case: describes a set of scenarios (scenario: instance of use case)
- Mockup: cheap prototype that shows what software will look like without having built it

### Requirements Management
managing and documenting RE activities

#### Functional requirements for a Requirements Management System
- shared repository for requirements
- multi-user access
- automatic specification document creation
- manage change of requirements
- create dependencies between requirements
- provide traceability of requirements throughout artifacts of system
- set priorities
- assign reqs to releases
- ...

#### measuring requirement quality
- validation is a QA step performed after elicitation/analysis
- Correctness:
    * represents the client's view

- Completeness:
    * "all" possible scenarios in which the system can be used are described
- Consistency:
    * no contradicting requirements
- Clarity:
    * Reqs can only be interpreted in one way
- Realism:
    * Reqs can be implemented and delivered
- Traceability:
    * Each system component and behaviour can be traced to a set of reqs

#### Prioritized Reqs
- High:
    * must be demonstrated at system delivery
    * Addressed during analysis design and impl
- Medium:
    * demonstrated in future iterations
- Low
    * in the future, impact only on analysis model

#### Aspects of prioritization include:
- Importance
- Cost
- Risk
- Time
- Financial benefit
- Penalty

#### Requirements depend on each other!
- Tradeoff analyis

#### Rationale management
- explain and capture rationale behind decisions, increases explainability and understand for stakeholders which eases adaptability and maintainability


	

## Lecture 02: Requirements Elicitation

### Motivation

_Requirements elicitation is the practice of researching and discovering the needs and acquiring knowledge about:_

- Stakeholders
- Expectations
- Current State
- Domain
- Tasks
- System and its context

#### System context 

- part of environment that is relevant for definition and understanding of requirements of a system that is to be developed
- people, systems in operation, business processes, laws, standards..
- System boundary:
    * which aspects belong to the system? which belong to the system context?
- context boundary:
    * Which aspects belong to the context? which belong to irrelevant environment?

#### Requirements sources
- Stakeholders
- Documents (laws norms standards wiki feedback blogs reports..)
- systems in production (competition, previous systems, systems in env)

#### Elicitation methods and research

Elicitation methods are a category of research tasks that use **visual, verbal** or **written** stimuli to encourage participants to talk about their ideas
We utilise concept and guidelines of Empirical Research methods (such as interviews, observations):
	- Stakeholders
	- Data collection
	- Data analysis

### Stakeholders

- people involved in the project or affected by its execution
- Stakeholders are the main source of goals and requirements of the project
- people with different backgrounds must collaborate (see challenges of Req Eli)
- Role of Req Engineer: identify stakeholders, assess their characteristics
    * expectations, importance to the project and requirements they bring

#### Population Sampling
A sample is a subset of subjects used to study a population

##### Types of sampling
  - Non-probability Sampling:
    -   Subjects have not equal chance of being selected
    -   Suitable for Pilot/Case studies and hypothesis development
   - Probability Sampling:

    	-   Every subject has an equal chance of being selected
    	-   Randomized process no bias
    	-   Suitable for verifying hypothesis and representativeness 
   - Convenience Sampling:

    	-   Subjects are selected based on easy access
    	-   Colleagues, Friends, Volunteers, Family
   - Sequential Sampling:

   		- Non-probability
    	- iterative, subjects, study, additional subjects, study more
    	
   - Snowball Sampling:
    	- subjects recommend subjects with similar trait of interest
    	- Helps to identify subjects
   
### Requirements Elicitation Methods

Main techniques: Interview/questionnaire, Observation, Workshop, Scenario/use case, Mockup

### Qualitative methods (Interview, Workshop, Focus Group, Case Study ((Observation))
Used to gather an in-depth understanding of human behavior and the reasons that govern such behavior
Characteristics:

-   Unstructured data
-   Small sample size
-   Categorization and summary
-   Subjective conclusion
 
#### Interview
Includes open questions, conventional method for elicitation
Are:

- Subjective
- Qualitative
- Exploratory
- Involve users

Interview guideline:

- Use templates, prepare questions and first drafts
- iterate
- dry runs
- do not influence subjects (stating what they should say/how they should answer)
- stay in scope, help subjects to focus
- listen actively, suggest ideas
- 60-90min

Don't:

- ask irrelevant questions
- ask multiple concepts at once
- ask too long questions
- ask confusing/misleading questions
- ask too technical questions

#### Workshop
Subjective, Qualitative, user involvment, open/closed questions and other tasks
conventional method for elicitation
A structured meeting with carefully selected stakeholders
work together to define create refine and close on deliverables
often includes several types of stakeholders

Workshop guideline:

- no idea is bad
- plan an agenda
- timebox discussions
- flip charts to capture ideas
- include right stakeholders, but keep it small

Are:

- Interactive
- giving all users right to express thoughts
- generating a lot of subjective feedback
- composed of users that normally do not have decision making authority

#### Focus Group
representative groupof users who participate in facilitated elicitation
useful for exploring users preferences and needs
valuable if there is no widespread access to end users


Workshops and focus groups must be facilitated
Facilitator doesnt have to be expert
Keep users on topic without influencing
Qualify subjective feedback, record for review


### Quantitative Methods (Surveys, Observations, Experiments, Data Analysis, Content Analysis, Simulation, ...)

Characteristics:

- Large sample size
- Structured data
- Statistically significant results
- Generalizable to some extend


#### Questionnaires

Subjective, Quantitative, Evaluative, involve many users

Guidelines:

- Describe your objective
- max 15 minutes
- Iterate and improve questions
-   - Remove unclear
-   - Put the least important last
-   - Match quesitons with answers
-   - Think about outliers
- Exclude non-serious subjects (incomplete answers, use check questions, random order of questions and answers)
- Motivate and give incentives (importance, share results, raffle gifts, dedicated analysis offers)
- Use Likert or semantic scales
- Use meaningful abbreviations for analysis
- Run statistical tests te remove random results
- Focus on quesi-experimentation instead of summaries


#### Observation
Objective, Quali/Quant, Exploratory, users + researchers
Guidelines:


- observe less but in realistic env
- use observation template (time, observation, postponed questions)
- report what you observe at least twice
- peer debriefing to identify relevant observations
- avoid talking to subjects during observation
- iterate


### Question Types
Exploratory
Baserate
Correlation
Design
Causal Relationship


Be concrete and precise with questions

### Requirements Elicitation Session
Prepare (scope, agenda, resources, questions)

Perform activities

Follow-up (share notes, document open issues)




## Lecture 3: Prototyping
_"Prototyping is externalizing and making concrete a design idea for the purpose of evaluation" - Bill Verplank_


