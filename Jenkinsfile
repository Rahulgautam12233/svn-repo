node{
   stage('SCM Checkout'){
      git 'https://github.com/Rahulgautam12233/svn-repo'
   }
   stage('Compile-Package'){
       sh 'mvn clean package'
   }
}
