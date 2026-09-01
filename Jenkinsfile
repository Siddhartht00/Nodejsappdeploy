

pipeline {
    agent any

    stages {

        stage('Install Dependencies') {
            steps {
                bat '''
                    set "PATH=C:\\Program Files\\nodejs;%PATH%"
                    node -v
                    npm -v
                    npm install
                '''
            }
        }

        stage('Deploy') {
            steps {
                bat '''
                    set "PATH=C:\\Program Files\\nodejs;%PATH%"
                    start "" /B cmd /c "npm start > app.log 2>&1"
                '''
            }
        }
    }
}
