node { 
    // Checkout the code from Git
    stage('Checkout') {
        git branch: 'main', url: 'https://github.com/testofgit2/simple-java-app.git'
    }

    // Build stage
    stage('Build') {
        try {
            sh 'echo "Building the application"'
        } catch (Exception e) {
            sh 'echo "Build failed"'
            throw e
        }
    }

    // Test stage
    stage('Test') {
        try {
            if (env.BRANCH_NAME == 'feat') {  // Corrected typo: BRANCE_NAME → BRANCH_NAME
                sh 'echo "Running tests"'
            } else {
                sh 'echo "No tests to run"'
            }
        } catch (Exception e) {
            sh 'echo "Test stage failed"'
            throw e
        }
    }
}
