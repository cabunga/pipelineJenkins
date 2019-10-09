node {
   
   stage('Obtener Codigo') {
     
      git 'https://github.com/cabunga/pipelineJenkins.git'
      
   }
   stage('Compilacion') {
      sh label:'', script: 'chmod +x gradlew'
      sh label: '', script: './gradlew clean build'
   }
   stage('Pruebas') {
     
   }
    stage('sonarvm') {
    withSonarQubeEnv {
     sh label: '', script: './gradlew sonarqube'
   }
    waitForQualityGate false
   }
    stage('Despliegue Dllo') {
     
   }
}