
pipeline{

    stage 'Dev'
    node ('docker-cloud') {
        checkout scm
        mvn 'clean package'
        dir('target') {stash name: 'war', includes: 'x.war'}
    }
}
