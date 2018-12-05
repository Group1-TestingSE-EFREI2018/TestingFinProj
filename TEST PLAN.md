# TEST PLAN

Bohao LI, Yuyao WEI, Yijie XIAN

Group 1 for Testing Class, M2-SE 2019

## Identify

## Introduction

The purpose of the Plan

-   This document presents general assumptions to collection process. 
-   It describes division of collection into stages and processes and most important notions in collection. 
-   Some of system’s functionalities accessible from every process and activity are described.
-   ​	

## Test Items 

version numbers: v0.0.1

configuration requirements 

-   Litigation is a collection through Court orders and with the help of Law enforcement officers. It is out of the scope of the project. Ekip will handle automatically only Early and Advanced Collection.
-    Field Collection (Street Collection) is out of the scope of the project. Ekip will not support this process apart from the standard screens containing customer and contract information, standard Ekip notes and one custom report to be created in Business Objects.
-    Collection of assets is out of scope. No inventory of collected assets or no asset valuation will be supported by Ekip.
-   Collection will be performed on a contract level. In rare cases, when multiple contracts become due for one client, a manual workflow for multiple contracts maintenance will be triggered.
-    From geographical point of view, collection activities will be centrally managed. From the organization point of view there will be three collection teams - Early Collection, Advanced Collection and Specialized Collection (manual, more complex processes). In the beginning, the collectors will be part of other Back Office teams to secure productivity of users.
-   Initially POS loans and later also cash loan will be offered in Romania. It is assumed that both products will have the same collection strategy, but it will be possible to differentiate in the future between the two on any level of the strategy and assign appropriate decision to the contracts related to the product.
-   Sending SMS during Early Collection instead of letters will not be implemented due to a significantly high investment cost required to integrate SMS gateway (a device that enables sending SMS messages to the GSM telecommunications network). SMS gateway is not included in the Romanian technical architecture.
-   Standard Ekip does not support sending e-mail reminder letters, so this functionality will not be implemented.
-   The detailed approach to Romanian strategy will not be performed until July 1-st 2007. Until then we are going to assume that Romanian collection strategy will be similar to a simplified version of Zagiel’s strategy. The objective of the project is to define a simple strategy. KBC will be able to modify the strategy as business grows.

key delivery schedule issues

Litigation

After 180 days the contract will pass to manual litigation (execution) process. Litigation is out of the scope of the project and will not be supported by any specialized Ekip screens or workflows.

Specialized Collection

Specialized Collection is collection on contracts which have some specificity that requires undertaking manual collection decisions on them.

critical steps required before testing can begin: Early Collection

Early collection is performed in the beginning of collection processes:in the first 90 days of delinquency. It will consist of a phone, letter until the unpaids are paid by the customer or until an agreement is reached with the customer or until the contract will go into a higher stage of collection.

References to existing incident reports or enhancement requests 

In Ekip Types of notes are defined as a codification of 4 alphanumerics.

To Any type of note is attached a description that can be seen when the collection officer chooses a type of note from the list in order to input a note on a contract.

All types of notes for Collection will have their code beginning with “C”.

list of what is to be tested and what is not to be tested:

## Features To Be Tested

1.  Collection stage: It is a major conceptual subdivision of collection, determined by time or by the seriousness of the actions that are undertaken. Within a collection stage, many actions are undertaken but with a similar seriousness.
2.  Decision point: it is set-up in Ekip as a sector. In Ekip a sector is a test done on a criterion. If a criterion is true, then Ekip workflow performs a decision to execute one predefined activity. If the criterion is false – the other predefined activity.
3.  Criterion: A criterion is for example the search in the database for a contract to answer to such a question as “how many unpaids are existing on a contract?”
4.  Activities: Ekip sufficient set-up for the automation of a job. This means that an activity is able to work on its own. An activity runs a set of actions in the time, at the same time or one after the other or both. Activities are run on contract and to every activity is attached a user or a group of users that are only allowed to work on it.
5.  Warning: in Ekip it is a message sent to a specific screen for a user. Every user has a screen that manages the warnings agenda. The messages are sent to this screen with the id of the contract on which they were produced. A set-up determines the messages that will be sent to this screen. Normally, if a user receives a warning (alert) it means that something important is happening on the contract (or is not happening when it should be).

## Features Not To Be Tested

Regression testing version：

No previous version

The current version (v0.0.1)：

1.  Litigation is a collection through Court orders and with the help of Law enforcement officers and out of the scope of the Ekip project. Ekip only handles Early and Advanced Collection.
2.  The process out of standard screens containing customer and contact information, standard Ekip notes and the custom report to be created in Business Objects. 
3.  Field Collection (Street Collection) is out of the scope of the project and will not be tested.
4.  Collection of assets will not be tested. The Ekip do not support inventory of collected assets or asset valuation.
5.  Only in the Early Collection, the collectors own Back Office teams permission. The permission and messages and all Back Office related features would not be tested as a collector role in Advanced Collection.
6.  Initial POS loans and later also cash loan will be offered in Romania. Other initial loans will not be tested.
7.  Sending SMS during Early Collection instead of letters will not be implemented due to a significantly high investment cost required to integrate SMS gateway. All features which related to SMS will not be tested.
8.  The Standard Ekip does not support sending e-mail reminder letters and e-mail reminder will not be tested.
9.  The detailed approach to Romanian strategy will not be performed until July 1st -2007. Until then we are going to assume that the Romanian collection strategy will be similar to a simplified version of Zagiel’s strategy. Other strategies will not be tested in this version.
10.  The format of the contract is only support 

## Approach 

Tools: 

-   No Specific Tools Except Word 2000,Excel 2000 and Notepad (on corresponding Windows version).
-   Test case management SW: Zentao open source 10.5 stable version

Metrics: 

​      \- Progress metrics：

-   Test case coverage rate.
-   Test case execution rate.
-   Documents upload.
-   Daily upload.

​      \- Quality metrics:

​	-  Number of blocking defects

​	-  Number of major defects

​	-  Number of minor tests

Regression testing：

No previous version

Configuration:

-   Hardware: 

-   -   Thinkpad X1C 3th, Core i5, 4G-RAM, 256G
    -   ASUS G551GW, Core i5, 4G-RAM, 256G
    -   DELL 5490, Core i7, 4G-RAM,128G
    -   Server : Synology DS2415+ Serveur NAS pour 12 Disques Durs 3,5"/2,5" 2,4 GHz QuadCore 2 Go 4 LAN USB 3.0 Noir

​      \-  Software:

① Operation System: Windows 98/XP/VISTA/win 7/win8

② Ekip

③ Database:PL/SQL

④ Server/Client

⑤ Web

Meetings: 

-   Project Creation Meeting ( Test manager ).
-   Explanation of the requirements framework Meeting (Test manager).
-   Test task assignation and The Explanation of the test plan and schedule Meeting.
-   Daily Morning Meeting.
-   Selecting Test Cases Meeting.
-   Current Version Acceptance Meeting (Test manager).

## Item Pass/Fail Criteria

At the Unit test

 \- All test cases completed.

 \- No Major defect and Serious defect.

 \- The Ordinary defect must be controlled within 10%.

 \- Code coverage tool indicates all code covered.

At the Integration test 

 \- All test cases completed.

 \-  No Major defect and Serious defect.

 \- The Ordinary defect must be controlled within 30%.

At Smoking test

Initialization

At 100% coverage test

 \- All test cases completed.

 \- No Major defect and Serious defect.

 \- The Ordinary defect must be controlled within 30%.

 \- Low impact defect would be passed in this version.

At Acceptance test

-   Operational Test: 

For each release,

-   2% blocking defects
-   3% major defects
-   5% minor defects

 	   - The Ordinary defect must be controlled within 30%.

​      \-     User Acceptance test: user satisfaction level is Acceptance.

Suspension Criteria and Resumption Requirements
· Unavailability of external dependent systems during execution.
· When a defect is introduced that cannot allow any further testing.
· Critical path deadline is missed so that the client will not accept delivery even if all testing is completed.


Test Deliverables 
· Test plan
· Test design specifications.
· Test case specifications
· Test procedure specifications
· Test item transmittal reports
· Test logs
· Test Incident Reports
· Test Summary reports

Test Task
· Test plan
· Test design specifications
· Test case specifications
· Test procedure specifications
· Test item transmittal reports
· Test logs
· Test Incident Reports
· Test Summary reports

## Environmental Needs

(1) Hardware:

-   -   Thinkpad X1C 3th, Core i5, 4G-RAM, 256G
    -   ASUS G551GW, Core i5, 4G-RAM, 256G
    -   DELL 5490, Core i7, 4G-RAM,128G
    -   Synology DS2415+ Serveur NAS pour 12 Disques Durs 3,5"/2,5" 2,4 GHz QuadCore 2 Go 4 LAN USB 3.0 Noir

(2) Software:

① Operation System: Windows 98/XP/VISTA/win 7/win8

② Ekip

③ Database:PL/SQL

④ Server/Client

⑤ Web

## Responsibilities

·  Setting risks - Test Manager.

·  Selecting features to be tested and not tested - Test Manager.

·  Setting overall strategy for this level of the plan - Test Manager and System  Architect Manager.

·  Ensuring all required elements are in place for testing - Test manager.

·  Providing for resolution of scheduling conflicts, especially if testing is done on the

production system - Test manager.

·  User Operation Engineer provides the required training.

·  Test manager makes the critical go/no-go decisions for items not covered in the test plans.

·  Test manager and test group leader deliver each item in the test items section.

## Staffing and Training Needs 

(1) Input the document into the Ekip and know about the 

① Note type code

② Note type name

③ Description

## Schedule

​	Write test plan & assign tasks (test manager) - Half a day

​	Write test cases (3 testers) - 1 week

​           Select test cases (test manager and 3 testers) - Half a day

​	Test case execution (3 testers) - 1 week

​	Quality report (test manager) - Half a day

## Risks and Contingencies

·  Lack of personnel resources when testing is to begin.

·  Lack of availability of required hardware, software, data or tools.

·  Late delivery of the software, hardware or tools.

·  Delays in training on the application and/or tools.

·  Changes to the original requirements or designs.

·  Specify what will be done for various events:

·  Requirements definition will be complete by January 1, 2007, and if the

requirements change after that date the following actions will be taken.

 	· Customer must pay extra fine for 0.05% in total cost per day

​	· All Schedule will delay on corresponding.

·  The number of tests performed will be reduced.

·  The number of acceptable defects will be increased.

·  These two items could lower the overall quality of the delivered product.

·  Resources will be added to the test team.

·  The test team will work overtime.

·  This could affect team morale.

·  The scope of the plan may be changed.

·  There may be some optimization of resources. This should be avoided if possible

for obvious reasons.

## Approvals

Project Manager will approvals the process as complete and allow the project to process to the next level while the Test manager will approve him the test progress report and quality report.