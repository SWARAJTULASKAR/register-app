pipleline{
  agent{label 'Jenkins-Agent'}
  tools{
    jdk 'Java17'
    maven 'Maven3'
    
  }
  stages{
    stage("Cleanup Workspace"){
      steps{
        cleansWs()
      }
    }
      stage("Cleanup Workspace"){
      steps{
        git branch: 'main',credentialsId: 'github' ,url:'https://github.com/SWARAJTULASKAR/register-app.git'
      }
    }
    stage("Build Application"){
      steps{
        sh "mvn clean package"
      }
    }
    stage("Test Application"){
      steps{
        sh "mvn test"
      }
    }
    
  }
}
