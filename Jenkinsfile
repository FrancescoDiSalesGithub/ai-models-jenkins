pipeline {
    agent any

    parameters {

        string(name:'MODELNAME',defaultValue:'silly')
        choice(name:'SERVER',choices:["192.168.56.20"])
    }


    stages {
        stage('Getting models') {
            steps {
                // Get some code from a GitHub repository
                git branch: 'main', url: 'https://github.com/FrancescoDiSalesGithub/ai-models'


              
            }

        }

        stage('uploading to server'){
            steps{
                echo "uploading to server ${params.SERVER}"
            }
        }
    }
}
