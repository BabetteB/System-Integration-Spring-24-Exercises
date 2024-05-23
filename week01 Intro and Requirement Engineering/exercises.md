# Week 01 Exercises

## Exercise 01 Speedy

Speedy is an international delivery company that needs to refocus on which markets it should operate. Indeed, Speedy lacks a clear understanding on which markets are the most profitable. Thus, to address this issue, Speedy’s top management aims at improving their governance. To achieve this, the top management requires sales reports containing timely information. Thus, the top management decided to build a new reporting system to automatically produce such reports. After inspecting the sales reports, the top management may also need to query the existing ERP system to get detailed sales and HR information.
Prepare an ArchiMate and an I-star model that captures the formalizes Speedy’s new architecture.

- Can you model all the elements and relations described in this exercise with both languages? 
- If not, which elements can be captured only in ArchiMate? Which ones in I-star?

Goal/driver: Find which markets are profitable
Actor with actions: Top Management, (new) reporting system, ERP system
Sub-goal: Improve governance
Task: require, build, auto preduce reports, inspecting, query
Resourses: sales reports (containing timely info), detailed sales info, detailed HR info

### Solution

![](./exercise%20files/ex01_speedy_archi.png)
![](./exercise%20files/ex01_speedy_istar.png)

In I-star it was very difficult to find a way to assosiate many of the resources and also assert what are goals, subgoals/drivers etc. Most of all what was difficult was that you are unable to draw relations between elements that are not within the same stakeholder which decouples the model but makes it less flexible.
In archimate there are more elements and lables to put and because it is similar to UML diagrams it was easier for me at least to understand and model them. The most limiting part I could find for Archimate is that it is slighty more difficult to assosiate actors with their actions and components, moreover it is very flexible so there is a higher risk of making syntactic errors.

## Exercise 02 IC
IC is an insurance company which wants to offer a new insurance service for small assets (<2000$) managed completely online for reliable
customers.\
To achieve this, a customer who wants their assets to be insured has to
provide its credentials and photo of the asset and its details (serial number, purchase date) to IC. To ensure that the customer is reliable and the asset inexpensive, IC will then check the customers credentials and past history and estimate the asset’s price.\
Prepare an ArchiMate and an I-star model that captures the formalizes IC’s
requirements.

- Can you model all the elements and relations described in this exercise
with both languages? If not, which elements can be captured only in
ArchiMate? Which ones in I-star?

### Solution

![](./exercise%20files/ex02_ic_archi.png)
![](./exercise%20files/ex02_ic_istar.png)

In Istar again it is not possible to break down resourses e.g. the asset cannot be specified to have serial number and other credentials, moreover you can not model the assesment criteria for a task - i put the requirement of the asset to be a quality, howevere I think it is better described as a requirement which I've made it in the archi model.

## Exercise 03 University travel reimbursement

This I-star model represents a university travel reimbursement system.
Prepare an ArchiMate model representing the same system
- Can you model all the elements and relations in this I-star model?
- If not, which elements and relations cannot be modeled?

![](./exercise%20files/ex03_travel_archi.png)

In Archimate you cannot specialize a goal with a task e.g. with *Request prepared* you cannot specialize with *fill form on paper* and *fill form online*. To work around this I made a task *fill in form* that realizes the goal but the task is specialized with *on paper* or *online*.

Another componen that can't be modeled are the make, break, hurt, help relationships - here I just used an infuence relationship with lables ++, --, -, +.

It isn't possible to group the component within the actor - instead for some of the actors, I just nested their actions in a group.

MoreOver I cannot use specialization where goal needs to be realised through one task or another, here I used the realization relation for OR relations and if multiple tasks needs to be met for a goal to be obtained, I created a new task that is decompositioned into multiple tasks that then realizes the goal.