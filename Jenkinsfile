pipeline {
    agent any
    stages {
        stage('firstStage') {
            steps {
                echo "first-stage"
            }
        }
        stage('building jobs') {
            parallel {
                stage('office job') {
                    steps {
                        sh(script: "date -u")
                        build(job: "office")
                    }
                }
                stage('role job') {
                    steps {
                        sh(script: "date -u")
                        build(job: "role")
                    }
                }
               stage('person job') {
                    steps {
                        sh(script: "date -u")
                        build(job: "person")
                    }
                }
               stage('department job') {
                    steps {
                        sh(script: "date -u")
                        build(job: "department")
                    }
                } 
               stage('main job') {
                    steps {
                        sh(script: "date -u")
                        build(job: "main")
                    }
                }
            }
        }
    }
}
