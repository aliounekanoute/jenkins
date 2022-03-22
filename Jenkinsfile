pipeline {
    stages {
        stage('clone') {
            steps {
                sh "rm -rf jenkins"
                sh "git clone https://github.com/aliounekanoute/jenkins.git"
            }
        }
        stage('build') {
            steps {
                sh "cd jenkins/jenkins-app && mvn clean package"
            }
        }
        stage('run') {
            steps {
                sh "java -jar /var/jenkins_home/workspace/MyFirstPipeline/jenkins/jenkins-app/target/jenkins-app-1.0-SNAPSHOT.jar"
            }
        }
    }
}
