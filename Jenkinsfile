pipeline{
    agent { label 'dev' }
    stages{
        stage('code'){
            steps{
                git url:'https://github.com/dhiyani12/react-django-demo-app.git', branch: 'master'
            }
        }
        stage('build'){
            steps{
              sh 'docker build . -t django-todo-app'
            }
        }
        stage('deploy'){
            steps{
              sh 'docker run -d -p 8001:8001 django-todo-app'
}
}
}
}
