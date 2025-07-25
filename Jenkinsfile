node{                        // all the code and script that going to be configured  
    git branch: 'main', url: 'https://github.com/testofgit2/simple-java-app.git'                       // for scripted pipeline you must define all expersion since he won't do anything more than what you asks for 
        // this is the git repository that we are going to use
    // Now you should specify the build steps    
    stage('build'){
        try{      // try catch block to handle errors   
        sh'echo "building the application"' // sh means that we are going to run a shell command
           }
        catch (Exception e) {
            sh'echo "Build failed"'
            throw e // if the build fails, we throw an exception
        }
    }

    stage('test'){
        try{
            if (env.BRANCE_NAME == 'feat')   // check if the branch name is feat
            
            sh'echo "running tests"'
            else
            sh'echo "No tests to run"'
        }
        

}
}
