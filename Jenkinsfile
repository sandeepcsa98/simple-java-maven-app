pipeline{
  agent {
    docker {
      image 'maven:3-alpine'
      args '-v /usr/local/bin/docker:/root/.m2'
    }
  }
  stages {
    stage('Build'){
      steps{
        sh 'mvn -B -DskipTests clean package'
      }
     }
    stage('Test'){
      steps{
        sh 'mvn test'
      }
      
  }
 
  }
}
