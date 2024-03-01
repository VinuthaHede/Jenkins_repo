pipeline{
    agent any

    parameters{
        string(name: "Username", defaultValue: "Vinutha", description: "enter your name here")
        text(name: "Details", defaultValue: "", description: "enter user details here")
        booleanParam(name: "Toggle", defaultValue: true, description: "toggle values")
        choice(name: "Choice", choices:["one", "two", "three"], description: "select a value from below")
        password(name: "Password", defaultValue: "secret", description: "enter your password")
    }

    environment{
        TEST="test value"
        TEST1="test value1"
        DEPLOY_TO="Testing"
    }

    stages{
        stage ('build'){
            steps{
                echo "$Username"
                echo "$Details"
                echo "$Toggle"
                echo "$Password"

                script{
                    echo "${params.Choice}"
                    echo "${env.DEPLOY_TO}"
                }
            }
        }

        stage('Parallel Execution'){
            parallel{
                stage('test1'){
                    steps{
                        echo "test1"
                        sh 'ls -lrt'
                    }
                }

                stage('test2'){
                    steps{
                        echo "test2"
                        sh 'ls -a'
                    }
                }
            }
        }
    }
}