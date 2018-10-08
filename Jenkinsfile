node{
   stage('SCM Checkout'){
      git 'https://github.com/Rahulgautam12233/svn-repo'
   }
   stage('Compile-Package'){
      def mvnHOME=tool name: 'Maven-3', type: 'maven' 
      sh "${mvnHOME}/bin/mvn clean package"
   }
}
