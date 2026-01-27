pipeline {
    agent any



    stages {
        stage('Getting models') {
            steps {
                // Get some code from a GitHub repository
                git branch: 'main', url: 'https://github.com/FrancescoDiSalesGithub/ai-models-jenkins'
                  dir('silly') {

                    sh "ls -l"
                  }

              
            }

        }
    }
}
