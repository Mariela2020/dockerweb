import groovy.json.JsonSlurperClassic

def jsonParse(def json){
    new groovy.json.JsonSlurperClassic().parseText(json)
}
pipeline {
    agent{ label 'master'    }
    environment {
        appName = 'variable'
    }
    stages {
    
    stage("Paso 1"){

        steps{
            script{
                bat "echo 'Hola Mundo'"
            }
        }
    }
}
post {
    always{
        deleteDir()
        bat "echo 'fase always'"
        }
    success{
        bat "echo 'fase success'"
    }    
    failure{
        bat "echo 'fase failure'"
    }
}

}