node{
    // Ensure the desired
    def root = "/usr/local/go/bin/go"

    stage 'Checkout'
    git url: 'https://github.com/gde1indra/sample-go-jenkins.git'

    stage 'preTest'
    sh "${root} version"

    stage 'Test'
    sh '${root} test ./... -cover'

    stage 'Build'
    sh "${root} build ./..."

    stage 'Deploy'
}