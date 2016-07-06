### Used to create/edit a Synapse Quiz (using the effective Quiz schema)

_Based on https://github.com/jdorn/json-editor_  

### Steps:
1.  Clone this repo.
2.  Start a web server 
  `python -m SimpleHTTPServer 8000`
3.  Go to the main page.
  `http://localhost:8000`
4.  Follow instructions (to load/edit/generate quiz)
5.  Send a developer the output json.  

For the Certification Quiz, the developer can deploy the quiz json (after backing it up) by updating the contents of `certifiedUsersTestDefault_vX.json` file in the AWS S3 bucket.

### Screenshot:
<img width="1124" alt="screen shot 2016-07-05 at 12 47 27 pm" src="https://cloud.githubusercontent.com/assets/1864447/16597672/04fbc416-42af-11e6-8bfa-d4ffb3cfbddc.png">



##### (Developers only) How to update the underlying Quiz schema json file
1.  Go to the auto-generated Quiz.java file for the latest repo version.
2.  Copy the Quiz.EFFECTIVE_SCHEMA.  (remove the escape backslashes that are necessary in java, and pretty print)
3.  Copy the MultichoiceQuestion.EFFECTIVE_SCHEMA.  (again, remove the escape backslashes that are necessary in java, and pretty print)
4.  In the Quiz json, replace the Question interface definition with the concrete MultichoiceQuestion json.
The schema can now be used by this tool to create a MultichoiceQuestion quiz from scratch, or edit an existing Quiz (including the current Certified User Quiz).
