pipeline{
    agent any

    parameters{
        string(name: "Username", defaultValue: "Vinutha", description: "enter your name here")
        text(name: "Details", defaultValue: "", description: "enter user details here")
        booleanParam(name: "Toggle", defaultValue: true, description: "toggle values")
        choice(name: "Choice", choice:["one", "two", "three"], description: "select a value from below")
        password(name: "Password", defaultValue: "secret", description: "enter your password")
    }

    stages{
        stage ('build'){
            steps{
                echo "$Username"
                echo "$Details"
                echo "$Toggle"
                echo "$Choice"
                echo "$Password"
            }
        }
    }
}