pipeline{
  agent any
  stages {
      stage('Build'){
          steps{
              sh '/Users/c2o/Documents/apache-maven-3.5.4/bin/mvn clean package'
          }
          post{
              success{
                echo 'Now archiving ...'
                archiveArtifacts artifacts: '**/*.war'
              }
          }
      }
  }
}
