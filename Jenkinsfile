pipeline {
 agent any
	tools {
        maven 'maven' 
    }
	 stages {
    stage('Analysis') {
	 steps {
               echo 'maven compilation'
                sh 'mvn  clean install'
              
              
            }
	 }
	 
}
}
    
