pipeline {
    agent any
   
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/Jasmine-tech17/Jenkins-Task2'
            }
        }
       
        stage('Run Script') {
            steps {
                sh 'chmod +x script.sh'
                sh './script.sh'
            }
        }
    }
   
    post {
        always {
            mail to: 'jasminechaudhary1997@gmail.com',
                 subject: "Jenkins Build Notification",
                 body: "The build has been triggered and executed successfully!"
        }
    }
}
