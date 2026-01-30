pipeline {
    agent any

    parameters {

        string(name:'MODELNAME',defaultValue:'silly')
    }


    stages {
        stage('Getting models') {
            steps {

                node('second'){
                // Get some code from a GitHub repository
                    git branch: 'main', url: 'https://github.com/FrancescoDiSalesGithub/ai-models'
                }

              
            }

        }

        stage('uploading to server'){
            steps{

                
                        node('second') {

                        dir("${params.MODELNAME}"){
                            
                        sh "ollama create ${params.MODELNAME} -f Modelfile"
                        }
                   }
                

            }
        }
    }
}
