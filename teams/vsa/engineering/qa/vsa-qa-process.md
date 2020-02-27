# VSA-QA Process

\[Based on [template process](https://github.com/department-of-veterans-affairs/va.gov-team/blob/44fb872c0a945ca8ffa85c360d7e09956b979b3f/platform/quality-assurance/process.md) by VSP Product Support team Sr. QA Specialist Peter Hill]

This VSA-QA Process is currently a subset of the base-process as defined by VSP Product Support.

## Process Flow

![VSA-QA Process Flowchart][flowchart]

## Process Steps

The required steps of the VSA-QA Process are as follows:

### 1. VSA Product Team gives advance notice

During new product/feature's **Build phase** (minimum **2-3 Sprints before** manual UI testing on Staging is needed), **VSA Product Manager** adds **vsa-qa** label to product/feature **Epic**.  This makes the Epic visible on VSA-QA's ZenHub board, and provides enough lead time for VSA-QA to understand product/feature, develop Test Plan, and create test-cases.

### 2. VSA-QA understands product/feature

With help from **VSA Product Team** subject matter experts (SMEs), **VSA-QA** establishes understanding of new product/feature \[VSA-QA currently handles only manual UI testing on Staging.]

### 3. VSA-QA opens Test Plan ticket

**VSA-QA Engineer** opens [Test Plan ticket][test-plan-tic]\* \[use the VSA QA Test Plan Issue Template]:

* Assign to appopriate QA Engineer
* Add **vsa-qa** label
* Attach to Epic
* Add link to Pre-Launch Checklist \(or ensure Epic ticket has this link) \[See [Product Development Checklist](https://github.com/department-of-veterans-affairs/va.gov-team/blob/d210639376918e687efdeda9445199985783c487/platform/working-with-vsp/onboarding/Product%20Development%20Checklist.md) for checlist guidelines]

### 4. VSA Product Team & VSA-QA build Test Plan

As Build phase progresses, **VSA Product Team & VSA-QA** collaborate to ensure that Test Plan includes documentation of (or links to):

* Product/feature Epic
* Product outline
* UX Design wireframes & comps
* User stories/scenarios/flows
* Staging test-accounts


### 5. VSA Product Team & VSA-QA develop test-cases

As Build Phase progresses, VSA Designers, Engineers, & VSA-QA develop manual UI test-cases:

* **VSA-QA** creates manual UI test cases:
  * **VSA Product Team** (PM and/or UX Design/Research) helps ensure all testable user scenarios/flows are covered.
  * **VSA Engineers** help ensure the steps in each test-case.

### 6. VSA-QA conducts testing\*\*
* **Build Phase**:
  * **Front-End (and/or Full-Stack) Developers** should already have created & run local unit-/e2e-tests during Build Phase.  These tests are also automatically run when Pull Requests (PRs) are opened, and merges are disabled until they all have passed.
* **Validate Phase** (once changes are deployed to Staging):
  * A11y Specialist performs accessibility tests.\*\*
  * VSA-QA performs manual tests\*\*.
  * Log defects.
  * Re-iterate as needed/desired, until all acceptance-critical bugfixes are validated.

### 7. Engineers & VSA-QA report test results

* Submit results to the VSP Product Support Team by sharing them in #vsp-product-support Slack channel. Either attach the documents to the channel, or provide shareable links to documents stored in the cloud.
* Expected deliverables include:
  * Test plan with test-results added/linked\*
  * QA Manual Testing Matrix\* \[[see sample](https://github.com/department-of-veterans-affairs/va.gov-team/blob/master/teams/vsa/engineering/qa/QA_Testing_Matrix_Template.xlsx)], to be linked/attached to Test Plan ticket.



## Notes

\* Test-plan-ticket details/references will be copied into an official Test Plan in our online TestRail test case management system (TCMS).  VSA Product Teams will share a common TestRail user-account to access & review the online Test Plan and its associated Test Runs/Cases.

\*\* Some QA and A11y testing tasks/subtasks may be assigned to Product Team members.  We currently have only 1 shared QA-resource and 1 shared A11y resource supporting all 8 VSA Product Teams, and anticipate availability challenges until staffing increases.

\*\*\* Re. manual UI testing on Staging by VSA-QA, a change's test-readiness depends upon Staging test-accounts and relevant test-data availability behind Staging API-endpoints.


[flowchart]: images/vsa-qa-process-flow.png
[test-plan-tic]: https://github.com/department-of-veterans-affairs/va.gov-team/issues/new?&template=vsa-qa-test-plan.md