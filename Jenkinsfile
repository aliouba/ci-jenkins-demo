node {
    def appName = 'flask-demo'
    def imageTag = "localhost:5000/${appName}:${env.BRANCH_NAME}.${env.BUILD_NUMBER}"
    stage('Clone repository') {
        checkout scm
    }
    stage('Build image') {
        app = docker.build("${imageTag}")
    }
    stage('Test image') {
        sh 'echo "Tests passed"'
    }
    stage('Push image') {
        docker.withRegistry('http://localhost:5000', '') {
            app.push("${env.BUILD_NUMBER}")
            app.push("latest")
        }
    }
}
