<link href="./../styles.css" rel="stylesheet"></link>
Week 01 : Goal-oriented Requirements Engineering

# Goal-oriented Requirements Engineering
Used to define the context in which an application works
- Time
- Place
- Information
- Operations
- Stakeholders

So it creates a foundation and common understanding of how the system (should) work.

**Goals**:
* Use of goals as a starting point to identify, elicit, document, specify and analyze requirements
* Goals are objectives that the system aims to achieve
* Goals are meant to specify why a requirement is needed, which tasks are required to reach it, and which ones may hamper its achievement

hence, it covers the collumn for the motivational viewpoint and the row for the contextual perspective in the Zachmann Framework.

## Elements for modelling

* Participanpants

| Types | Describtion | I-star symbol | Archimate symbol |
| ----- | ----------- | ------------- | ---------------- |
| Actor/Stakeholder | The role of an individual, team or organisation (or classes thereof) that represents their interest in the outcome of the application | ![i-star actor](./images/req_engineering_elements/i-star/actor.png) | ![archimate stakeholder](./images/req_engineering_elements/archimate/stakeholder.png)
| Agent             | A business entity that is capable of performing a set of behaviours. | ![i-star agent](./images/req_engineering_elements/i-star/agent.png) | ![archimate business actor](./images/req_engineering_elements/archimate/business_actor.png)
| Role              | The responsibility for performing specific behaviour, or the part one plays in a particular action or event.  | ![i-star role](./images/req_engineering_elements/i-star/role.png) | ![archimate business role](./images/req_engineering_elements/archimate/business_role.png)

| Types | Describtion | I-star symbol | Archimate symbol |
| ----- | ----------- | ------------- | ---------------- |
| Goal      | An intent, direction or desired end state for an organisation and its stakeholders. | ![i-star goal](./images/req_engineering_elements/i-star/goal.png) | ![archimate goal](./images/req_engineering_elements/archimate/goal.png)
| Quality   | A criteria that must be met by the architecture. | ![i-star quality](./images/req_engineering_elements/i-star/quality.png) | ![achimate requirement](./images/req_engineering_elements/archimate/requirement.png)
| Task      | An/a set of action(s) to achive something | ![i-star task](./images/req_engineering_elements/i-star/task.png) | ![archimate business process](./images/req_engineering_elements/archimate/business_process.png)
| Resource  | A object concept | ![i-star resource](./images/req_engineering_elements/i-star/resource.png) | ![archimate business obejct](./images/req_engineering_elements/archimate/business_object.png)

| Relations | Description | I-star Symbol | Archimate Symbol |
| --------- | ----------- | ------------- | ---------------- |
| Specialisation | a is a A | ITU $-ISA\rightarrow$ Uni | ITU <span>&#8702;</span> Uni
| Assignment | a plays the role of an A | Bab $-Plays\rightarrow$ MSc Student | Bab $\boldsymbol{\cdot}\rightarrow$ MSc Student
| Composition | a is part of/cannot exist without A | topping $-Is\_part\_of\rightarrow$ pizza | topping <span>&#8212;<span style="display: inline-block; transform: rotate(90deg);">&#9830;</span></span> Pizza

| Associating elements to participants | |
|-----------------|-|
| I-star | Archimate |
| ![image_w200_h180](./images/req_engineering_elements/i-star/assosiation.png) | ![image_w200_h180](./images/req_engineering_elements/archimate/association.png)  |

## Goal Refinement

| Type | I-star | Archimate |
| ---- | ------ | --------- |
| Decomposition | ![image_w200_h180](./images/req_engineering_elements/i-star/goal_decomposition.png) | ![image_w200_h180](./images/req_engineering_elements/archimate/goal_decomposition.png) |
| Specialization | ![image_w200_h180](./images/req_engineering_elements/i-star/goal_specialization.png) | ![image_w200_h180](./images/req_engineering_elements/archimate/goal_specialization.png)
| Realization(inclusive)  | ![image_w200_h180](./images/req_engineering_elements/i-star/goal_realization.png) | ![image_w200_h180](./images/req_engineering_elements/archimate/goal_realization.png)


## Task Refinement
| Type | I-star | Archimate |
| ---- | ------ | --------- |
| Task Decomposition | ![image_w200_h180](./images/req_engineering_elements/i-star/task_decomposition.png) | ![image_w200_h180](./images/req_engineering_elements/archimate/task_decomposition.png)
| Task Specialization | ![image_w200_h180](./images/req_engineering_elements/i-star/task_specialization.png) | ![image_w200_h180](./images/req_engineering_elements/archimate/task_specialization.png)

## Resources for task execution
| I-star | Archimate |
| ------ | --------- |
| ![i-star: access relation](./images/req_engineering_elements/i-star/access_relation.png) | ![archimate: access relation](./images/req_engineering_elements/archimate/access_relation.png)

## Contribution links
| I-star Type | Archimate Type | I-star | Archimate |
| ----------- | -------------- | ------ | --------- |
| Make | Influence Relation | ![i-star make relation](./images/req_engineering_elements/i-star/contribution_link_make.png) | ![archimate positive influence relation](./images/req_engineering_elements/archimate/contribution_link_influence_relation_positive.png)
| Help | Influence Relation | ![i-star help relation](./images/req_engineering_elements/i-star/contribution_link_help.png) | ![archimate positive influence relation](./images/req_engineering_elements/archimate/contribution_link_influence_relation_positive.png)
| Hurt | Influence Relation | ![i-star hurt relation](./images/req_engineering_elements/i-star/contribution_link_hurt.png) | ![archimate negative influence relation](./images/req_engineering_elements/archimate/contribution_link_influence_relation_negative.png)
| Break| Influence Relation | ![i-star break relation](./images/req_engineering_elements/i-star/contribution_link_break.png) | ![archimate negative influence relation](./images/req_engineering_elements/archimate/contribution_link_influence_relation_negative.png)


# Archimate-exclusive intentional elements
| Type | Description | Symbol |
| ---- | ----------- | ------ |
| Driver | An external or internal condition that motivates an organisation to define its goals and implement the changes necessary to achieve them. | ![archimate driver](./images/req_engineering_elements/archimate/driver.png)
| Assesment | The result of an analysis of the state of affairs of the enterprise with respect to some driver. | ![archimate assesment](./images/req_engineering_elements/archimate/assesment.png)
| Constraint | A factor that prevents or obstructs the realisation of goals. | ![arcimate constraint](./images/req_engineering_elements/archimate/conatraint.png)
| Priciple | A qualitative statement of intent that should be met by the architecture | ![archimate priciple](./images/req_engineering_elements/archimate/principle.png)

**Example**:\
![ArchiMate-exclusive intentional elements example](./images/req_engineering_elements/archimate/archiMate-exclusive_intentional_elements_example.png)

# I-star-exclusive social dependencies
![I-star-exclusive social dependencies](./images/req_engineering_elements/i-star/I-star-exclusive_social_dependencies.png)

**Example**:\
![i-star extended example](./images/req_engineering_elements/i-star/i-star_example.png)

## Reasoning

| Type | Symbol |
| ---- | ------ |
| Denied | ![I-star reasoning denied](./images/req_engineering_elements/i-star/reasoning_denied.png)
| Partially denied |
| Partially satisfied |
| Satisfied | 

### Forward analysis (AND-Decomposition)

### Forward analysis (OR-Decomposition)
