node{
    // Ensure the desired
    def root = tool type: 'go' name: 'Go 1.15'

    // Export
    withEnv(["GOROOT=${root}","PATH+GO=${root}/bin"]){

        stage 'Checkout'
        git url: 'https://github.com/gde1indra/sample-go-jenkins.git'

        stage 'preTest'
        sh 'go version'

        stage 'Test'
        sh 'go test -cover'

        stage 'Build'
        sh 'go build'

        stage 'Deploy'
    }
}