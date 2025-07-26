pipeline {
agent {
  label 'aws-agent'
} // Runs on any available Jenkins agent

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'mvn clean package'
                    // Add your build commands here
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo 'Testing...'
                    // Add your test commands here
                }
            }
        }
    }
post {
    success {
        slackSend(
            channel: '#jenkins-ci',
            message: "✅ Build succeeded: ${env.JOB_NAME} #${env.BUILD_NUMBER} (<${env.BUILD_URL}|Open>)",
            teamDomain: 'lamona-group',
            tokenCredentialId: 'jenkins-slack'
        )
    }
    failure {
        slackSend(
            channel: '#jenkins-ci',
            message: "❌ Build failed: ${env.JOB_NAME} #${env.BUILD_NUMBER} (<${env.BUILD_URL}|Open>)",
            teamDomain: 'lamona-group',
            tokenCredentialId: 'jenkins-slack'
        )
    }
}
}
