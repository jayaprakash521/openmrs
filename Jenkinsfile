node('Jaya') {
     stage('git') {
           git 'https://github.com/jayaprakash521/openmrs.git'
          }
     stage('build') {
          sh 'mvn clean package'
          }
     stage('archive artifacts') {
          archive 'webapp/target/*.war'
      	  } 
     stage('test results') {
          junit 'webapp/target/surefire-reports/*.xml'
         }
}
          
