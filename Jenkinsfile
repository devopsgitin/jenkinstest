pipeline{
  agent any
  stages{
    stage("Check Build Number and Job Number"){
      steps{
        checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'gitkey', url: 'git@github.com:devopsgitin/jenkinstest.git']]])
        sh "bash test.sh"
      }
    }
  }
}
