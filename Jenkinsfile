node{
   stage('SCM Checkout'){
      git 'https://github.com/Rahulgautam12233/svn-repo'
   }
   stage('Compile-Package'){
      def mvnHOME=tool name: 'Maven-3', type: 'maven' 
      sh "${mvnHOME}/bin/mvn clean package"
   }
     stage('Deployment'){  
      sshagent(['Tomcat-dev']) {
      sh 'scp -o StrictHostKeyChecking=no target/*.jar root@192.168.11.133:/opt/apache-tomcat-7.0.73/webapps
}
   stage('Email Notification'){
      mail bcc: '', body: '''Hi Team,
      This is testing jenkins jobs.Please ignore it. 
      Thanks,
      Rahul Gautam''', cc: '', from: '', replyTo: '', subject: 'Jenkins Jobs', to: 'rahulgautam12233@gmail.com' 
   }
   stage('Slack notification'){
       slackSend baseUrl: 'https://hooks.slack.com/services/',
          channel: '#jenkinspipelinedemo', color: 'good',
          message: 'Welcome to slack!', teamDomain: 'gautamdevops', tokenCredentialId: 'slackdemo'  
   }
     
   
   
}
