pipeline {
    agent any

    stages {

        stage('Create build output') {
            steps {
                script {
                    sh "mkdir -p output"
                    writeFile file: "output/usefulfile.txt", text: "This file is useful, need to archive it."
                    writeFile file: "output/uselessfile.md", text: "This file is useless, no need to archive it."
                }
            }
        }

        stage('Archive build output') {
            steps {
                archiveArtifacts artifacts: 'output/*.txt', excludes: 'output/*.md', followSymlinks: false
            }
        }

        stage('Interactive input') {
            steps {
                input message: 'Do you want to continue the pipeline?', ok: 'Yes, continue'
            }
        }
    }
}

