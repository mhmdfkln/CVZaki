<template>
  <div class="cv">
    <header>
      <div class="header-left">
        <img :src="profileImage" alt="Profile Picture" class="profile-image" />
      </div>
      <div class="header-right">
        <h1>{{ name }}</h1>
        <p>{{ jobTitle }}</p>
        <p>{{ contactInfo }}</p>
      </div>
    </header>

    <section>
      <h2>Data Diri</h2>
      <ul>
        <li v-for="edu in datadiri" :key="edu.saya">
          <p>{{ edu.saya }}</p>
        </li>
      </ul>
    </section>

    <section>
      <h2>Pendidikan</h2>
      <ul>
        <li v-for="job in pendidikan" :key="job.dates">
          <h3>{{ job.sekolah }}</h3>
          <p>{{ job.dates }}</p>
        </li>
      </ul>
    </section>

    <section>
      <h2>Pengalaman Kepanitiaan</h2>
      <ul>
        <li v-for="org in pengalaman" :key="org.description">
          <p>{{ org.description }}</p>
        </li>
      </ul>
    </section>

    <section>
      <h2>Skills</h2>
      <ul>
        <li v-for="skill in keterampilan" :key="skill">{{ skill }}</li>
      </ul>
    </section>
  </div>
</template>

<script setup>
const name = 'Mohammad Fakhlan Zaki Harmawan';
const jobTitle = 'Web Developer';
const contactInfo = 'Email: mfzh87@gmail.com | Phone: +62 8572 1791 403';
const profileImage = 'fotoku.jpg'; // Ganti dengan jalur gambar yang sesuai

const datadiri = [
  {
    saya: 'Saya adalah seorang mahasiswa Universitas Brawijaya Fakultas Vokasi Jurusan Teknologi Informasi yang memiliki kemampuan dalam bidang Bisnis Digital'
  }
];

const pendidikan = [
  {
    sekolah: 'SMAN 4 PROBOLINGGO',
    dates: '(2020 - 2023)'
  },
  {
    sekolah: 'Universitas Brawijaya',
    dates: '(2023 - Sekarang)'
  }
];

const pengalaman = [
  {
    description: 'Panitia Kampung Budaya Universitas Brawijaya Tahun 2024',
  },
  {
    description: 'Panitia Ospek Jurusan Prodi Teknologi Informasi Tahun 2024',
  }
];

const keterampilan = [
  'Canva', 
  'Figma', 
  'Adobe Premiere', 
  'Corel Draw',
];
</script>

<style>
.cv {
  max-width: 800px;
  margin: auto;
  padding: 20px;
  background-color: #f9f9f9;
  border-radius: 8px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}

header {
  display: flex; /* Menjadikan header sebagai flexbox */
  align-items: center; /* Vertikal rata tengah */
  margin-bottom: 30px;
}

.header-left {
  margin-right: 20px; /* Jarak antara gambar dan teks */
}

.profile-image {
  width: 100px;
  height: 130px;
  border-radius: 0%; /* Gambar tetap persegi */
}

.header-right {
  flex-grow: 1; /* Memastikan konten kanan mengambil ruang yang tersisa */
}

h1 {
  font-size: 2.5em;
  margin: 0;
}

h2 {
  border-bottom: 2px solid #ccc;
  padding-bottom: 5px;
  margin-top: 20px;
  color: #333;
}

section {
  margin-bottom: 20px;
}

ul {
  list-style-type: none; /* Menghilangkan bullet points */
  padding: 0; /* Menghilangkan padding */
}

li {
  margin-bottom: 10px;
  padding: 10px;
  background-color: #fff; /* Warna latar belakang item daftar */
  border: 1px solid #ddd; /* Garis batas item daftar */
  border-radius: 5px; /* Sudut melingkar */
}

li h3 {
  margin: 0;
  color: #151515; /* Warna teks judul pekerjaan */
}

p {
  margin: 5px 0; /* Margin atas dan bawah */
  color: #555; /* Warna teks deskripsi */
}
</style>