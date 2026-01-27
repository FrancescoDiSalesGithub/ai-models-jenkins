pipeline {
    agent any

    parameters {

        string(name:'MODELNAME')
    }


    stages {
        stage('Getting models') {
            steps {
                // Get some code from a GitHub repository
                git branch: 'main', url: 'https://github.com/FrancescoDiSalesGithub/ai-models'
                  dir("${params.MODELNAME}") {

                    sh "ls -l"
                  }

              
            }

        }
    }
}
