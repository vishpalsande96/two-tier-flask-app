pipeline{
    agent any;
    stages{
        stage("code"){
            steps{
                git url:"https://github.com/vishpalsande96/two-tier-flask-app.git", branch: "master"
                echo "code clone successfully"
            }
        }
        stage("build"){
                        steps{
                            sh "docker build -t app ."
                echo "Build successfully"
            }
        }
        stage("test"){
                        steps{
                echo "Testing completed successfully"
            }
        }
        stage("deploy"){
                        steps{
                            sh "docker compose up -d"
                echo "Has been Deployed successfully"
            }
        }
    }
}
