pipeline {
	agent any 
	stages {
		stage (checkout){
			steps{git 'https://github.com/Rohit-457/pipeline-repo.git'}
		}
		stage (build){
			steps{sh 'mvn install'}
		}
		stage (Deploy){
			steps{sh 'cp target/pipeline-repo.war /home/rohit/Documents/devops/apache-tomcat-9.0.93/webapps'}
		}
	}
}
