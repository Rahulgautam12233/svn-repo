node{
   stage('SCM Checkout'){
      git 'https://github.com/Rahulgautam12233/svn-repo'
   }
   stage('Compile-Package'){
      def mvnHOME=tool name: 'Maven-3', type: 'maven' 
      sh "${mvnHOME}/bin/mvn clean package"
   }
   stage('Email Notification'){
      mail bcc: '', body: '''Hi Team,
      This is testing jenkins jobs.Please ignore it. 
      Thanks,
      Rahul Gautam''', cc: '', from: '', replyTo: '', subject: 'Jenkins Jobs', to: 'rahulgautam12233@gmail.com' 
  
   }
}
