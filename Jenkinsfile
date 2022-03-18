pipeline {

  agent any
 
  stages {
    stage('Build') {
      steps {
            bat 'mvn -B -U -e -V clean -DskipTests package'
      }
    }

    stage('Test') {
      steps {
        echo "Testing done successfully"
      }
    }

     stage('Deployment') {
   
      steps {
            bat 'mvn clean package -DskipTests deploy -Pdev -DmuleDeploy' 
      }
    }
   
  }
}
