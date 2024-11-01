<h1 align="center"> NLP With HuggingFace Transformers </h1>
<p align="center"> Berisi tentang analisis pipeline dari HuggingFace Transformers untuk keperluan NLP (Natural Language Processing)</p>

<div align="center">

<img src="https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54">
<img src="https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white">

</div>

<h2 align="center"> Analisis NLP With HuggingFace Transformers </h2> 

- Zero-short-classcification merupakan jenis tugas NLP yang digunakan untuk mengklasifikasikan teks ke dalam kategori yang belum pernah dilatih secara eksplisit. Zero-short-clasification dalam jenis tugas NLP termasuk pada *Klasifikasi seluruh kalimat*. Hasilnya tergantung terhadap kalimat yang kita berikan, apabila kita memberikan candidates label yang katanya sama dengan apa yang terdapat pada kalimat maka nilai probabilitasnya akan semakin besar.

- Text generation digunakan untuk memuat model terlatih yang khusus dirancang agar dapat menghasilkan teks yang lebih mendetail dari text kalimat yang diberikan. Text generation dalam jenis tugas NLP termasuk pada  tugas untuk *membuat konten teks*. Apabila dalam code ditambah model="distilgpt2" maka hasilnya akan sesuai dengan model "distilgpt2" yang mana merupakan versi yang lebih kecil dan lebih cepat dari GPT-2 language model, yang didesain untuk text genaration yang lebih efisien Dalam kode diatas juga terdapat variasi lain yaitu menggunakan max_length=30, dan num_return_sequences=2. max_length=30 digunakan untuk membatasi teks yang hasilkan maksimum 30 kata sedangkan  num_return_sequences=2 digunakan untuk memerintahkan model agar mengahsilkan 2 rangkaian teks berbeda sebagai output.

- Fill-mask merupakan model yang digunakan untuk mengisi kata yang hilang dalam sebuah kalimat. Dalam tugas NLP fill-mask termasuk dalam membuat konten teks. Dalam kode diatas untuk mengsisi kata yang hilang menggunakan token <mask> dan top_k=2 digunakan untuk menentukan jumlah prediksi teratas yang akan ditampilkan, yaitu dua kata yang paling mungkin berdasarkan model.

- Ner tugas NLP yang bertujuan untuk mengenali entitas tertentu dalam teks. grouped_entities=Tru digunakan untuk memembantu jalur NER memberikan keluaran yang lebih terorganisasi dan koheren dengan mengelompokkan kata-kata terkait yang termasuk dalam entitas yang sama. apabila tidak menggunakan grouped_entities=True maka beberapa kata akan mengidentifikasinya dengan entitas yang terpisah. dalam kalimat yang terdapat pada code tersebut apabila tidak menggunakan grouped_entities=True maka seventeen akan menjadi entitas yang terpisah dengan seven dan teen. Ner dalam tugas NLP termasuk dalam kategori untuk *klasifikasi setiap kata*. Dalam kalimat tersebut entitas yang teridentifikasi adalah seventeen sebagai organtion dan Korea sebagai location.

- Question-answering digunakan untuk menjawab pertanyaan berdasarkan konteks teks yang diberikan. Model yang digunakan dalam code tersebut adalah distilbert-base-cased-distilled-squad, yang merupakan versi ringan dari model BERT yang dilatih menggunakan dataset SQuAD (Stanford Question Answering Dataset). Dalam jenis tugas NLP question-answering termasuk kedalam kategori yang digunakan untuk mengekstrak jawaban dari teks.

- Sentiment-analysis digunakan untuk  mendeteksi apakah teks yang diberikan mengandung sentimen positif atau negatif. Untuk tugas sentiment-analysis objek pipeline yang digunakan menggunakan classifier. Hasil dari klasfikasi pada kode diatas adalah positif karena terdapat kata excellent yang mengandung makna positif yang disertai dengan keyakinan model terhadap klasifikasi model. sentiment-analysis dalam tugas NLP termasuk dalam klasifikasi seluru kalimat.

- Summarizer digunakan untuk mereduksi teks menjadi versi yang lebih singkat tanpa kehilangan inti atau informasi penting. Output yang dihasilkan dalam kode tersebut akan diringkas menjadi beberapa kalimat yang mewakili informasi penting tanpa detail yang tidak relevan. Summarizer dalam tugas NLP termasuk dalam membuat kalimat baru dari teks masukan

- Translation digunakan untuk menerjemahkan bahasa dari teks yang kita berikan. Dalam tugas NLP translation termasuk sebagai tugas untuk membuat kalimat baru dari teks masukan. Dari kode di atas mengubah dari teks bahasa indonesia "Aku suka menonton drama china" menjadi bahasa prancis "J'adore regarder les drames chinois." untuk mengubah dari bahasa indonesia ke bahasa prancis menggunakan model="Helsinki-NLP/opus-mt-id-fr".

