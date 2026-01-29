pipeline {
    agent any

    parameters {

        string(name:'MODELNAME',defaultValue:'silly')
        choice(name:'SERVER',choices:["192.168.56.20"])
    }


    stages {
        

        stage('build ai'){
            steps{
                dockerNode('ollama/ollama') {
                         git branch: 'main', url: 'https://github.com/FrancescoDiSalesGithub/ai-models'
                         dir("${params.MODELNAME}"){
                          sh "ollama create ${params.MODELNAME} -f Modelfile"
                         }
                    }
            }
        }
    }
}
