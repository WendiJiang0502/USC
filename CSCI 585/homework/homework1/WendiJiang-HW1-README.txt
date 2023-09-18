Assumptions:
- Assume each employee's test result leads to different contact tracing records, even they are in the same meeting. 
- Assume the contact tracing record for each employee is the general version of all their meetings conbined in one record.
Diagram Design:
- Employees as an entity would have a primary key of employee ID, smartphone number and email address.
- Employees and Registration System (M:1) There is only one registration system, and multiple employees would register through that system.
- Employees and Phone App (M:1) There is only one phone app, and multiple employees would download that app; And phone app notifies multiply employees who share the same meeting record with the employee who test postive.
- Employees and Symptom (1:M) Since one employee can shows 0 or multiple symptoms including fever(which tests by the ramdom scan) and self-report symptoms.
- Company and Scan (1:M) The company can randomly scan the employee's temperature, 0 or multiple employees.
- Scan and Symptom (1:1) One scan could only show one or zero symptom because scan can only show the high temperature symptom.
- Symptoms and COVID test (M:1) One or multiple symptoms can lead to test that employee for COVID.
- Employee and test result(1:M) One employee could have zero or many test resluts because they might never show any symptoms or get the random test or they could have many tests.
- COVID test and test result(1:1) One COVID test can only have one test result.
- Phone App and Symptoms(1:M) Employees can self-report zero or multiple symptoms through the phone app.
- Phone App and Test results(1:M) Employees can self-reprt zero or multiple test results through their phone app.
- Test result and Contact Tracing record(1:1) If the result is positive, then there is one record for that employee and if the result is negative, then there is no contact tracing record activated.
- Meeting and Phone App(M:1) Multiple meetings can be record through the phone app.
- Phone app and Quarantine Status(1:M) Since the employee needs to update their status to the company daily, so there are multiple status reports to the company through the phone app.
- Test results and Quarantine Status(1:M) The test result could decides if the employee needs to self-quarantine, if they are tested postive, they need to report multiple quarantine status.
- Employee and Quarantine Status(1:M) One employee could have zero or multiple quarantine status reported.
