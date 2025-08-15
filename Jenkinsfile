pipeline {
  agent any
  tools {
    gradle 'gradle'
  }
  stages {
    stage("run frontend") {
      steps {
        echo 'executing yarn ...'
        nodejs('nodeJS') {
          sh 'yarn install'
        }
      }
    }
   stage("run backend") {
     steps {
       echo 'executing gradle ...'
       withGradle(){
         sh './gradlew -v'
       } 
   }
    }
  }
}
