===== Put vs Patch =====

PUT is similar to POST in that it can create resources, but it does so when there is a defined URL wherein
PUT replaces the entire resource if it exists or creates new if it does not exist. Provide all field in json body

Unlike PUT Request, PATCH does partial update e.g. Fields that need to be updated by the client,
only that field is updated without modifying the other field. Provide all/only updated field in json body 

Newman is a CLI (Command-line interface) tool which allows you to run a Postman collection directly from the command line.

====== For Newman report ====== 


1. Download and install Node.js (LTS) and set a path of node.js and bin folder

Environment setup of Nodejs ---->
Go to this PC and right click >> "Advanced system settings" >> "Environment Variables" >> New (System Variables) >> 

Variable name: NODE_HOME   
Variable value: Nodejs path (C:\Program Files\nodejs)
click "OK"

Find variable's "Path" and select & click "Edit" then "New" and paste "bin" path (C:\Program Files\nodejs\node_modules\npm\bin)

2. Install Newman by cmd:

---> npm install -g newman //install

---> newman -v //check


3. html library install by cmd (for report generate):

---> npm install -g newman-reporter-html

---> npm install -g newman-reporter-htmlextrap

4. Run by cmd (go this export's folder and run by cmd):

---> newman run "collectionName.json" -e "environmentName.json"   //only report show

---> newman run "collectoName.json" - e "environmentName.json" -r cli,html  //html report

---> newman run "collectoName.json" - e "environmentName.json" -r cli,htmlextra  //html best report


