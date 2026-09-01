pipeline {
    agent any

    stages {

        stage('Install Dependencies') {
            steps {
                bat '''
                    set "PATH=C:\\Program Files\\nodejs;%PATH%"

                    echo Checking Node.js...
                    node -v

                    echo Checking npm...
                    npm -v

                    echo Installing dependencies...
                    npm install
                '''
            }
        }

        stage('Deploy') {
            steps {
                bat '''
                    set "PATH=C:\\Program Files\\nodejs;%PATH%"

                    echo Starting Node.js application...

                    start "" /B cmd /c "npm start > app.log 2>&1"

                    timeout /t 5 /nobreak > nul

                    echo Application deployed successfully!
                '''
            }
        }
    }
}
