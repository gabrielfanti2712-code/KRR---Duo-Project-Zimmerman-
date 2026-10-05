# KRR---Duo-Project-Zimmerman-
## Modelling industrial robot environments

This page contains instructions on the homework exercise on knowledge representation. The goal is to provide a knowledge model to describe information related to an industrial environment made of machines, places, tools that evolve in time an space. The goal is provide enough knowledge in sufficiently precise way that an intelligence system can determine what action to perform given a specific goal, or analyse what happened before for better decision making. From fragmentary descriptions of events, it should be possible to reconstruct (at least in part) the evolution of the system and identify problematic situations, such as two robots follow overlapping trajectories that may collide, etc.

The delivery consists in providing a formal specification defining classes and properties with associated axioms, a documentation, and example data that instantiate the model.

## Use case
During the sessions, we often rely on the production line and facility of the IT'm Factory at the ground floor of Espace Fauriel. The facility is complex enough to illsutrate challenging situations of knowledge representation. These challenges, in turn, can be extrapolated to cover other facilities, real corporate industries. A formal description of a physical system can be the basis of a digital twin.

## Knowledge Model
The knowledge model in this exercise corresponds to the ontology or ontologies that define the generic classes and properties that characterise the domain of interest. It is very unlikely that you need to introduce instances at the level of the knowledge model. In your homework, instances should only exist to exemplify how to instantiate the classes and properties of your knowledge model.

## Modelling machines
A separate module that organise knowledge about machines must be produced. This module should provide terminologies that are common to all machine types, but can also provide a hierarchy of more or less specific machine types and their associated properties. Axioms and rules should be provided. The more generic the rules are, the more widely the knowledge model applies.

## Modelling functions
Machines and tools have functions that can be triggered. This could be part of the machine module or separated. A hierarchy of functions can be defined. We consider that a function is something that can be triggered to produce an action. A function is always present, while an action happens at a specific time, possibly from the punctual us of a function.

## Modelling places
A separate module of places must be provided. There are very general spatial relationships that can exist between places. The simplest of them is the “subpart” relation (e.g., Saint-Étienne is a subpart of département de la Loire). You have to introduce general spatial relations in this module.

Additionally, places can be organised in hierarchies. Such hierarchies may be industry-specific but can be very general too. For instance, we can distinguish warehouses from logistic platforms, as distinct subtypes of places.

As part of the ontology of places, there can be spatial relations according the the Region Connection Calculus, as provided in the RCC ontology.

## Modelling time
This includes modelling temporal entities (such as timepoints or time intervals) and their relation (before, after, etc.). This can use Allen’s temporal algebra

## Events and actions
This is the most interesting and complex part. Events occur at specific time points or during a period of time. We may not know the exact duration, starting time and ending time of an event, but we know when they occur with respect to another event (before, after, during, etc.). Events occur at places and involve characters.

Events and actions connect time, places, agents, and tools. Events can also be organised in hierarchies (e.g., production event, move events). Provide an event hierarchy as needed.

Actions can be thought of a specifial case of events, but they involve an actor, and usually have an impact on the environment. The consequences of actions are notably difficult to model. They relate to pre-conditions and post-conditions, which are challenging aspects of knowledge representation.

## Itineraries
For this exercise, we focus more precisely on itineraries. They relate spatial and temporal dimensions, and may also connect to the actor following the itinerary, the actions performed along the way, and event that may have happenned.

For this module, we would like to have rules that detect (deductively) overlapping itineraries, or itineraries that cross each other.

## Instructions
Your work will be delivered by teams of two students. You will deliver several files: ontology files in Turtle that correspond to the modules mentioned above (machines, events, etc.); the documentation that goes with it, preferably in HTML but possibly in PDF or (worse) MS Word or OpenOffice writer; and a separate Turtle file that shows a concrete example of data instantiating and illustrating all parts of your model.

## The ontology file
The ontology should provide classes and properties related to the different aspects of plot descriptions.

## Competency questions
Using your ontology, it should be possible to answer the following competency questions:

What are the available tools in a specific place P?
What sequence of places did a moving entity visit during a specific move event e?
Organise your ontology well
Separate concerns as much as possible. This can be apparent by documenting different aspects of your knowledge model in different sections.

Add rich axioms
The extensiveness of the coverage is not essential in this work. We will value much more a small ontology with few classes and properties but rich and complex rules. Identify interesting knowledge that constrain how your ontology terms could be interpreted.

## The documentation
The documentation must contain natural language labels for all the terms defined in the ontology, and a textual description of what the terms mean (you can use the properties rdfs:label and rdfs:comment for each term you introduce). The documentation must contain examples of usage of the terms you introduce. Additionally, any amount of details about the design choices can be given in the introduction of the documentation. The way AI tools were used can also add from the point of view of assessing your work.

## The instance file
A Turtle file with instances that illustrate all the things from your model must be provided.

For this, you will extend the example file given during the course.

## Delivery
Deadline for delivery: December 10th, 2026

The ideal way to deliver your work is by using a Git repository. It is also advisable to use Git to collaborate on the files, if you are familiar with it. Otherwise, use a file hosting service. Send us the link by email before the deadline. Make sure that files delivered by way of a link to the Web are kept available for long enough.

last modified 2026/10/04 16:42:42 by Antoine Zimmermann.
