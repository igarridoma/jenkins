import groovy.json.JsonSlurperClassic

def jsonParse(def json) {
    new groovy.json.JsonSlurperClassic().parseText(json)
}
pipeline {
  agent { label 'principal' }
  environment {
    appName = "variable" 
  }
  stages {

 stage("paso 1"){
     
      steps {
          script {			
           bat "echo 'hola mundoo'"
        }
      }
    }
  }
  post {
      always {          
          deleteDir()
           bat "echo 'fase always'"
      }
      success {
            bat "echo 'fase success'"
        }

      failure {
            bat "echo 'fase failure'"
      }
      
  }
}  

