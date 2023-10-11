import groovy.json.JsonSlurperClassic

def jsonParse(def json){
  new groovy.json.JsonSlupperClassic().parseText(json)
}
pipeline {
  agent { label 'master' }
  environment {
    appName = 'Variable'
  }
  stages{
    stage("Paso 1"){
      steps{
        script {
          sh "echo 'Hola'"
        }
      }
    }  
  }
  post {
    always {
        deleteDir()
        sh "echo 'Fase always'"
    }
    success {
      sh "echo 'Fase success'"      
    }
    failure { 
      sh "echo 'Fase failure'"
    }
  }
}
