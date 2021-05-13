pipeline {
    agent any
    parameters {
        string(name: 'Greeting', defaultValue: 'Hello', description: 'somethings')
    }
    stages {
        stage("Hello"){
            steps{
                sh "echo \"${params.Greeting} World\""
            
            }
        }
        stage("Script"){
            steps{
                timeout(time:1, unit:"MINUTES"){
                    sh '/var/jenkins_home/scripts/scriptsfile.sh'
                }
            }
            
        }
    }
}
