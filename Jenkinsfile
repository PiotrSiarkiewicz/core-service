pipeline {
    agent any
    parameters {
        string(name: 'Greeting', defaultValue: 'Hello', description: 'somethings')
    }
    stages {
        stage("Hello2"){
            steps{
                sh "echo \"${params.Greeting} World\""
            
            }
        }
        stage("Script2"){
            steps{
                timeout(time:2, unit:"MINUTES"){
                    sh '/var/jenkins_home/scripts/scriptsfile.sh'
                }
            }
        }
        stage("Script2"){
            steps{
                timeout(time:1, unit:"MINUTES"){
                    echo "done"
                }
            }
            
        }
    }
}
