pipeline {
    agent any

    stages {

        stage('Install Dependencies') {
            steps {
                bat '''
                    set "PATH=C:\\Program Files\\nodejs;%PATH%"
                    echo Node version:
                    node -v

                    echo NPM version:
                    npm -v

                    echo Installing dependencies:
                    npm install
                '''
            }
        }

        stage('Deploy') {
            steps {
                bat '''
                    set "PATH=C:\\Program Files\\nodejs;%PATH%"
                    echo Starting application...
                    start "" /B cmd /c "npm start > app.log 2>&1"
                    echo Application deployed successfully!
                '''
            }
        }
    }
}
