pipeline {
    agent {
        label 'agent-jenkins-01'
    }

    stages {
        stage('Kesatu') {
            steps {
                echo 'Proses ke-1 mulai'
                sh '''
                nil1=5
                nil2=3
                hasil=$((nil1*nil2))
                echo "Hasil perhitungan: $nil1 x $nil2 = $hasil"
                '''
                echo 'Proses ke-1 selesai'
            }
        }
        
        stage('Kedua') {
            steps {
                echo 'Proses ke-2 mulai'
                sh '''
                nil1=5
                nil2=3
                hasil=$((nil1+nil2))
                echo "Hasil Proses ke-2: $hasil"
                '''
                echo 'Proses ke-2 selesai'
            }
        }
    }
}
