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

        stage('Ketiga') {
            steps {
                echo 'Proses ke-3 mulai'
                script {
                    int nil1 = 10;
                    int nil2 = 6;
                    int hasil = nil1 - nil2;
                    echo "Hasil Proses ke-3: ${hasil}"
                }                
                echo 'Proses ke-3 selesai'
            }
        }

        def keterangan = null;
        stage('Keempat') {
            steps {
                echo 'Proses ke-4 mulai'
                script {
                    int nil1 = 15;
                    int nil2 = 6;
                    int hasil = nil1 - nil2;
                    echo "Hasil Proses ke-3: ${hasil}"

                    if(hasil > 3){
                        keterangan = "AAAA";
                    } else {
                        keterangan = "BBBB";
                    }

                    echo "Label: ${keterangan}"
                }                
                echo 'Proses ke-3 selesai'
            }
        }
    }

    post {
        always {
            echo "Proses sudah selesai dilakukan"
        }

        success {
            echo "Semua proses berhasil dilakukan"
        }

        failure {
            echo "Proses yang dilakukan ada yang gagal"
        }

        aborted {
            echo "Proses yang dilakukan dibatalkan"
        }
    }
}
