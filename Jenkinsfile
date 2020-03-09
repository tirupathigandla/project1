node{
   stage('SCM Checkout'){
     git 'https://github.com/tirupathigandla/project1'
   }
   stage('Compile-Package'){
    sh 'mvn package'
   }
   stage('Deploy package'){
      deploy adapters: [tomcat9(credentialsId: 'tomcat', path: '', url: 'http://localhost:8081/')], contextPath: null, war: '**/*.war'
   }
}
