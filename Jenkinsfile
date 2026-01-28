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

                script {

                      try {
                    dir("${params.MODELNAME}") {

                    sh "ls -l"
                  }
                }
                catch(Exception e){
                    echo "${e.getMessage()}"
                }
                    
                }
              


              
            }

        }
    }
}
