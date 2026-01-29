pipeline {
    agent any

    parameters {

        string(name:'MODELNAME',defaultValue:'silly')
        choice(name:'SERVER',choices:["192.168.56.20"])
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
