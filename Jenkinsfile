pipeline {
    agent any

    tools {
        maven  'Apache Maven 3.9.1'
    }

    stages {
        stage('git clone') {
            steps {
                git branch: 'main', credentialsId: 'github', url: 'https://github.com/nirmalaputra/demoproject.git'
				
            }
		}
		stage ('Maven Clean')
		{
		  steps {
		    sh 'mvn clean'
		  }
		}
		stage ('Maven Test')
		{
		  steps {
		    sh 'mvn test'
		  }
		}
		stage ('Maven Compile')
		{
		  steps {
		    sh 'mvn compile'
		  }
		}
		stage ('Maven Package')
		{
		  steps {
		    sh 'mvn package'
		  }
		}
		stage ('Maven Deploy')
		{
		  steps {
		    sh 'mvn deploy'
		  }
		}
		
		
    }
}
