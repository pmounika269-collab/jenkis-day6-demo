// pipeline {
//     agent any

//     stages {
//         stage('Day 11 Test') {
//             steps {
//                 echo 'Hello from Jenkinsfile'
//                 sh 'whoami'
//                 sh 'pwd'
//             }
//         }
//     }
// }
pipeline {
    agent any

    parameters {
        string(name: 'APP_NAME', defaultValue: 'myapp', description: 'Application name')
        choice(name: 'ENV_NAME', choices: ['dev', 'qa', 'prod'], description: 'Environment')
    }

    stages {
        stage('Show Parameters') {
            steps {
                echo "App Name from params: ${params.APP_NAME}"
                echo "Environment from params: ${params.ENV_NAME}"
            }
        }
    }
}
