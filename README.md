**UJIAN AKHIR SEMESTER KELOMPOK 3**

                                                           ANGGOTA KELOMPOK :
                                          - Angeline Romauli Sabatini         (2005551038)
                                          - Brian Jordan Wijaya               (2005551055)


                                                        LAPORAN PROJECT UAS PBA
                                                          QUESTION ANSWERING

**DESKRIPSI UMUM PROGRAM**

Project ini merupakan aplikasi yang berbasis question answering secara website. Program ini digunakan untuk mengetahui sesuatu dengan memberi pertanyaan pada kolom pertanyaan. Program ini dibangun dengan menggunakan language model dalam bahasa Python. Pada program in Idigunakan dataset SQuAD (The Standford Question Answering Dataset). Dataset merupakan suatu kumpulan data yang terstruktur yang mengandung informasi pada masa lalu untuk diolah menjadi informasi baru. Dataset terdiri dari berbagai variabel mengenai suatu topik tertentu.

**ARSITEKTUR PROGRAM**

Arsitektur program terbagi menjadi 3 bagian, yaitu bagian front-end, back-end, dan model.
1. Front -end, pada bagian front-end digunakan bahasa pemrograman Python. Bagian inilah yang akan menjadi design untuk platform question answering, di mana pada front-end terdapat kolom untuk penggguna mengisi pertanyaan yang akan diajukan. Setelah itu, program akan memberikan respon lalu program akan menampilkan predict jawaban yang berasal dari model python_model.bin.
2. Back-end, pada bagian back-end digunakan bahasa pemrograman python. Bagian ini digunakan untuk membentuk dan menjalankan front-end agar dapat memproses pertanyaan sehingga memberikan jawawaban yang sesuai dengan predict model.
3. Model, pada bagian ini digunakan untuk mengolah dataset agar dapat memberikan predict jawaban kepada backend. Setelah itu, back end akan memproses model dan akan disalurkan kepada front end. Lalu, front end akan menampilkan jawaban dan konteks.

**MODEL PROGRAM**
1. Dataset yang digunakan pada program ini adalah Standford Question Answering Dataset. Terdapat 98106 data pada dataset yang kami gunakan.
2. Algoritma Machine Learning yang digunakan untuk pembuatan question answering adalah BERT. Bidirectional Encoder Representations from Transformers (BERT) merupakan suatu algoritma yang diciptakan oleh Google untuk memahami konteks kata-kata dalam pencarian. BERT menggunakan teknik pre-processing berbasis jaringan saraf untuk perosesan bahasa alami atau dalam bahasa Inggrisnya adalah Natural Language Processing (NLP) yang bertujuan untuk memudahkan komputer dalam memahami bahasa. Cara kerja BERT berbasis neural network atau jaringan saraf tiruan dalam machine learning dan AI yang mencoba meniru system kerja otak manusia, sehingga mesin dapat belajar dan meningkatkan kemampuannya. BERT mampu melatih model bahasa berdasarkan seluaruh rangkaian katadalam kalimat atau query daripada pelatihan tradisional pada urutan kata yang diururtkan dari kiri ke kanan dan kanan ke kiri. Banyak macam pekerjaan dalam NLU yang dapat diselesaikan oleh BERT. Pekerjaan-pekerjaan itu antara lain adalah Question Answering (QA), sentiment analysis, machine translation, Named Entity Recognition (NER), dan lainnya. 
3. Tahapan preprocessing pada model ini adalah dengan menggunakan BertTokenizer dari library Transformers.
4. Pada program ini menggunakan pre-trained language model untuk melakukan training data. Proses training dari Pre-trained language model dimulai dengan input suatu kalimat. Setelah itu model akan dibangun berdasarkan input kalimat tersebut yang akan menghasilkan output tertentu. Setelah itu, model akan diperbaharui berdasarkan output yang dihasilkan.
5. Tahap evaluasi dilakukan untuk melihat apakah model sudah bekerja dengan baik. Tahap ini juga digunakan untuk mnegetahu prediksi hasil yang diperoleh.

**CARA MENGGUNAKAN PROGRAM**
Program dapat dijalankan dengan cara berikut ini.
1. Membuat akun ngrok agar mendapatkan authoken

3. Melakukan instalasi pyngrok
!pip install pyngrok

2. Melakukan konfigurasi ngrok
!ngrok config add-authtoken 2J2B6UsvY5OFddmqEixEKf0PXTi_68362FSDuEfupxpUYbATo

4.	Melakukan import ngrok
from pyngrok import ngrok
!pgrep streamlit

5.	Melakukan setup tunnel port streamlit
public_url = ngrok.connect(port='80')
public_url

6.	Melakukan run app.py pada url dengan port server 80
!streamlit run --server.port 80 app.py >/dev/null

7. Pada kode program public_url akan menghasilkan output link seperti http://a906-35-223-46-49.ngrok.io
8. Setelah meng-klik link, maka akan muncul web seperti dibawah ini
 
![WhatsApp Image 2022-12-18 at 8 42 18 PM](https://user-images.githubusercontent.com/81507442/208339099-e6fce77d-e028-4fec-80be-8c00096a4fd7.jpeg)
