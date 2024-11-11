pipeline {
    agent any

    tools {
        maven 'Maven 3.9.9'  
        jdk 'JDK21'    
    }

    stages {
        stage('Clone Repository') {
            steps {
                git url: 'https://github.com/Varadnir/jenkins.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }

        stage('Run Application') {
            steps {
                sh 'java -jar src/index.jsp'
            }
        }
    }
}
