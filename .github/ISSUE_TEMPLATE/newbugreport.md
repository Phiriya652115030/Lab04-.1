---
name: NewBugReport
about: this is bug report
title: "[Bug]: "
labels: bug
assignees: ''

---

name: NewBugReport
description: File a bug report
title: "[Bug]: "
labels: ["bug", "triage"]
assignees: 
 - octocat
body:
 - type: markdown
   attributes:
     value: |
       Thanks for taking the time to fill out thing bug report!
 - type: input
   id: contact
   
   attributes:
     label: Contract Details
     description: Also tell us, what did you expect to happen?
     placeholder: ex. email@example.com
   validations:
     required: false
 - type: textarea
   id: what-happened
   attributes:
     label: What happened?
     description: Also tell us, what did you expect to happen?
     placeholder: Tell us what you see!
     value: "A bug happened!"
   validations:
     required: true
 - type: dropdown
   id: Version
   attributes:
     label: Version
     description: What version of our software are you running?
     options:
       - 1.0.2 (Default)
       - 1.0.3 (Edge)
     default: 0
   validations:
     required: true
 - type: dropdown
   id: browsers
   attributes:
     label: What browsers are you seeing the problem on?
     multiple: true
     options:
       - Firefox
       - Chrome
       - Safari
       - Microsoft Edge
 - type: textarea
   id: logs
   attributes:
     label: Relevant log output
     description: Please copy and paste any relevant log output. This will be automatically formatted into code, so no need for backtick.
     render: shell
 - type: checkboxes
   id: terms
   attributes:
     label: Code of Conduct
     description: By submitting this issue, you agree to follow our [Code of Conduct](htpps://example.com)
     options:
       - label: I agree to follow this project's Code of Conduct
         required: true
          
---
