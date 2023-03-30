# Postman
CI/CD Jenkins prerequisites:
  -Install Nodejs: https://nodejs.org/en
  -Install Java and set the Java path in System Environments Variables in your PC
  -Install Newman 
  -Install Jenkins
  
Cmd command to run Jenkins Localhost: 
  -java -jar jenkins.war --httpPort=8080

Jenkins - Settings/
 -Build Steps: in his step the user should write commands to be executed from the drop-down menu Execute Windows batch command type should be selected
 -Inportant: Junit Report will be available if the following commands are in one line
 
 newman run "Trello API.postman_collection.json" --environment "TestEnvironment.postman_environment.json" --disable-unicode --reporters cli,junit,html --reporter-junit-export "newman/report.xml"
 
 Post Buld Actions:
 - From drop-down menu select Publish JUnit test result report type of report
 - Add the in HML path in thuis step newman/report.xml
