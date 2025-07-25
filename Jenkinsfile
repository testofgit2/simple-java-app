pipeline{
    agent any     // specify the agent to run the pipeline on
    

    stages {

        stage('Build') {
            steps{
                script {
                    echo 'Building...'
                    // Add your build commands here
                }
            }
    }

    stages('test') {
        steps {
            script {
                echo 'Testing...'
                // Add your test commands here
            }
        }
    }

}
}
