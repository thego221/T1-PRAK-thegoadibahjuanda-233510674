<template>
  <div class="container">
    <div class="card">
      <!-- Kiri: Teks -->
      <div class="text-section">
        <p class="greeting">Halo</p>
        <h1 class="title">
          Saya <span class="highlight">Thego Adibah Juanda</span><br />
          <span class="subtitle">mahasiswa Informatika</span>
        </h1>
        <p class="paragraph">
          Selamat datang di portofolio saya! Saya adalah mahasiswa program studi Teknik Informatika yang saat ini sedang menempuh pendidikan di salah satu universitas di Indonesia.
        </p>
        <p class="paragraph">
          Saya memiliki minat besar dalam dunia teknologi, khususnya di bidang pengembangan perangkat lunak, jaringan komputer, serta analisis data. Saya selalu bersemangat untuk mempelajari hal-hal baru dan mengembangkan keterampilan saya dalam dunia informatika.
        </p>
        <p class="paragraph">
          Saat ini, saya sedang memperdalam ilmu <span class="bold">pemrograman</span> dan <span class="bold">pengolahan data</span> melalui platform
          <a href="#" class="link">Dicoding</a>, dan berharap dapat membangun berbagai proyek portofolio di masa depan sebagai bukti kemampuan saya.
        </p>
      </div>

      <!-- Kanan: Foto -->
      <div class="image-section">
        <img :src="profileImg" alt="Thego Adibah Juanda" class="profile-image" />
      </div>
    </div>
  </div>
</template>

<script>
import profileImg from './components/profile.jpg';

export default {
  name: 'App',
  data() {
    return {
      profileImg
    };
  }
};
</script>

<style scoped>
.container {
  min-height: 100vh;
  background-color: #f5f3ff;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 2rem;
}

.card {
  width: 100%;
  max-width: 1024px;
  background-color: #fff;
  border-radius: 1rem;
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
  padding: 2rem;
  display: flex;
  flex-direction: column;
  gap: 2rem;
}

@media (min-width: 768px) {
  .card {
    flex-direction: row;
    align-items: center;
  }
}

.text-section {
  flex: 1;
}

.greeting {
  color: #8b5cf6;
  font-weight: 600;
  font-size: 0.875rem;
  text-transform: uppercase;
  margin-bottom: 0.5rem;
}

.title {
  font-size: 2.25rem;
  font-weight: 700;
  color: #1f2937;
  margin-bottom: 1rem;
}

.highlight {
  color: #7c3aed;
}

.subtitle {
  font-weight: 500;
  color: #374151;
}

.paragraph {
  color: #4b5563;
  margin-top: 1rem;
  line-height: 1.6;
}

.bold {
  font-weight: 600;
}

.link {
  color: #2563eb;
  font-weight: 600;
  text-decoration: none;
}

.link:hover {
  text-decoration: underline;
}

.image-section {
  flex-shrink: 0;
  display: flex;
  justify-content: center;
}

.profile-image {
  width: 12rem;
  height: 12rem;
  object-fit: cover;
  border-radius: 9999px;
  filter: grayscale(100%);
}
</style>
