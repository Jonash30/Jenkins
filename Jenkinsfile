pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                echo '[INFO] Cloning Repository'
                //sh 'git clone --depth 1 --single-branch https://github.com/Jonash30/Jenkins.git'
                sh 'ls website'
            }
        }
        stage('Provision AWS Instance') {
            steps {
                echo '[INFO] Deploying to AWS'
                // sh 'scp -r web_app user@ip_add:/var/www/html'
            }
        }
        stage('Deploy') {
            steps {
                echo '[INFO] Sending Notifications'
                // sh 'sh notif.sh'
            }
        }
        stage('Notification') {
            steps {
                echo '[INFO] Sending Notifications'
                slackSend channel: '#jenkins', message: 'Hello There', teamDomain: 'jenkinsteamco', color: '#439FE0'
                //cleanWs()
            }
        }
    }
}
