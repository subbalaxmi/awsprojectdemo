pipeline {
    agent any
    tools {
       maven 'mav'
    }

    stages {
		
        stage ('Build Stage') {

            steps {
			dir("/var/lib/jenkins/workspace/jenkinspipeline/mavewebappdemo"){
			sh 'mvn clean install'
            }
            }
        }

        
		stage ('Deployment Stage') {

            steps {
                
                    sh 'cp /var/lib/jenkins/workspace/jenkinspipeline/mavewebappdemo/target/mavewebappdemo.war /opt/apache-tomcat-8.5.37/webapps '
              
            }
        }


        
    }
}
