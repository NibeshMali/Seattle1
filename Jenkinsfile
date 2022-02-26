pipeline {

  agent any

   parameters {
     string(name: 'version',
            defaultValue: 'seattle1.1',
            description: 'Seattle Project')
   }

   stages{
      stage('Checkout')
              steps {

                checkout([$class: 'GitSCM', branches: [[name: '*/seattle1.1']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/NibeshMali/Seattle1.git']]])              
              }
      stage('Build')
        steps{
          script{
             mvn -f //location of pom.xml file

          }
      }
   }
}
