# JavaCodeGuidelines
A code review checklist for Java/Android projects.


# Java

#### General
- Does the project pass all tests on the CI server?
- Is there any repetition in the code which can be avoided?
- Have the toString/equals/hashcode methods been implemented on model classes?

#### Stylistic
- Are there any excessively long lines (>120 chars)?
- Are there any excessively large methods/classes?
- Could any of the methods/classes/variables have a more appropriate name?
- Is the code formatted similarly to the rest of the project?
- Are there enough comments?

#### Error Handling
- Are stream resources closed?
- Are all exceptions handled?
- Does the code check for null references and handle them appropriately?
- Are method parameters validated if the code relies on assumptions (e.g. non-null, between 0-100)?

#### Mutability
- Is the accessibility level (public/protected/package/private) appropriate for all fields/methods/classes?
- Can it be final?
- Can the method return an empty List rather than null?

# Android
- Are listeners/receivers deregistered in the appropriate lifecycle method?
- Are there any references to views/activities/fragments/inner classes/async tasks which might leak memory?
- Do any long operations (disk io/network) run on a background thread?
- Are there any potential performance issues (e.g. unnecessary parent views, not using ViewHolder pattern)?
- Are user input fields validated?
- Does it use ButterKnife/latest technologies?
