pipeline{
  agent any
  stages {

    stage('Build'){
      steps{
        sh 'mvn clean package'
      }
      post{
        success{
          echo 'Now archiving ...'
          archiveArtifacts artifacts: ''**/*.war'
        }
      }
    }

    stage('Deploy'){
      steps{
        echo "Code Deployed."
      }
    }
  }

}
