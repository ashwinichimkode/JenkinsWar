node{

   /*def tomcatWeb = 'D:\\Auto_deployment\\apache-tomcat-9.0.30\\apache-tomcat-9.0.30\\webapps'
   def tomcatBin = 'D:\\Auto_deployment\\apache-tomcat-9.0.30\\apache-tomcat-9.0.30\\bin'
   def tomcatStatus = ''*/
   stage('SCM Checkout'){
     git  'https://github.com/ashwinichimkode/JenkinsWar'
   }
   stage('Compile-Package-create-war-file'){
      // Get maven home path
      /*def mvnHome =  tool name: 'maven-3', type: 'maven'  */ 
    /*  bat "${mvnHome}/bin/mvn package"*/
      
     sh  "mvn clean install package"
      }
   
   stage("deploy"){
      sh "echo hi"
      
   /*sshagent(credentials: ['deploy-tomcat'], ignoreMissing: true) {
      
    sh "scp -o StrictHostKeyChecking=no /var/lib/jenkins/workspace/pipelinedeploytomcat/target/JenkinsWar.war ec2-user@
172.31.13.180:/opt/apache-tomcat-10.0.11/webapps"
}*/
   }
/*   stage ('Stop Tomcat Server') {
               bat ''' @ECHO OFF
               wmic process list brief | find /i "tomcat" > NUL
               IF ERRORLEVEL 1 (
                    echo  Stopped
               ) ELSE (
               echo running
                  "${tomcatBin}\\shutdown.bat"
                  sleep(time:10,unit:"SECONDS") 
               )
'''
   }*/
 /*  stage('Deploy to Tomcat'){
     bat "copy target\\JenkinsWar.war \"${tomcatWeb}\\JenkinsWar.war\""
   }
      stage ('Start Tomcat Server') {
         sleep(time:5,unit:"SECONDS") 
         bat "${tomcatBin}\\startup.bat"
         sleep(time:100,unit:"SECONDS")
   }*/
}
