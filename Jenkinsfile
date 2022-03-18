pipeline {

  agent any
 
  stages {
    stage('Build') {
      steps {
            bat 'mvn -B -U -e -V clean -gs %M2SETTINGS% -DskipTests package'
      }
    }

    stage('Test') {
      steps {
        echo "Testing done successfully"
      }
    }

     stage('Deployment') {
   
      steps {
            bat 'mvn -U -V -e -B -gs %M2SETTINGS% -DskipTests-Pdev deploy -DmuleDeploy' 
      }
    }
   
  }
}