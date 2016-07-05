### Used to edit the Synapse Certification Quiz (based on the effective Quiz schema).

_Based on https://github.com/jdorn/json-editor_  

### Steps:
1.  Clone this repo.
2.  Start a web server 
  `python -m SimpleHTTPServer 8000`
3.  Go to the main page.
  `http://localhost:8000`
4.  Follow instructions (to load/edit/generate quiz)
5.  Send a developer the output json.  

The developer can then deploy the quiz (after backing it up) by updating the contents of `certifiedUsersTestDefault_vX.json` file in the AWS S3 bucket.

### Screenshot:
<img width="1124" alt="screen shot 2016-07-05 at 12 47 27 pm" src="https://cloud.githubusercontent.com/assets/1864447/16597672/04fbc416-42af-11e6-8bfa-d4ffb3cfbddc.png">
