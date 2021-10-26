pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Build Stage'
            }
        }
        stage("Test"){
            steps{
                sh '''
                   echo "show the current path with command pwd:"
                   pwd
                '''
            }
        }
        stage("Finished"){
            steps{
                echo "finished"
            }
        }
    }
    post{
        always {
            echo "it will run always"
        }
        failure {
            echo " it will run when failure happen"
        }
        unstable {
            echo "it will run when the run is marked as unstable"
        }
        changed {
            echo "it will run when the state of pipeline is changed"
        }
        aborted {
            echo " it will run when the pipeline is aborted"
        }
    }
}
