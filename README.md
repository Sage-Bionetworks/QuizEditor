### Used to edit the Synapse Certification Quiz (based on the effective Quiz schema).

_ Based on https://github.com/jdorn/json-editor _  

Steps:
1.  Clone this repo.
2.  Start a web server 
  `python -m SimpleHTTPServer 8000`
3.  Go to the main page.
  `http://localhost:8000`
4.  Follow instructions (to load/edit/generate quiz)
5.  Send a developer the output json.  

The developer can then deploy the quiz by (after backing it up) updating the contents of `certifiedUsersTestDefault_vX.json` file in the AWS S3 bucket.