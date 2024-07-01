pipeline {
    agent any
    
    tools {
        nodejs "nodejs"
    }
    
    stages {
        stage("Clone Repository"){
            steps {
                git url: "https://github.com/navi-da/gallery", branch: "master"
            }
        }
        
        stage("Install Dependencies"){
            steps {
                sh "npm install"
            }
        }

        stage("Test"){
            steps {
                sh "npm test"
            }
        }
    }
}