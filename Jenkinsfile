pipeline {
    agent any

    parameters {

        string(name:'MODELNAME',defaultValue:'silly')
    }


    stages {
        stage('Getting models') {
            steps {
                // Get some code from a GitHub repository
                git branch: 'main', url: 'https://github.com/FrancescoDiSalesGithub/ai-models'

                       catchError(buildResult: 'SUCCESS', stageResult: 'FAILURE') {
            sh 'exit 1'
            }
                    dir("${params.MODELNAME}") {

                    sh "ls -l"
                  }
                
              


              
            }

        }
    }
}
