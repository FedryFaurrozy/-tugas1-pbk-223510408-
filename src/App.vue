<template>
  <div>
    <header class="navbar navbar-expand-lg navbar-dark bg-" style="padding-top: 30px; padding-bottom: 30px; padding-left: 20px; padding-right: 20px;">
      <div class="container-fluid">
        <!-- Icon di sebelah kiri -->
        <a class="navbar-brand" href="#">
          <img src="https://png.pngtree.com/png-clipart/20220604/original/pngtree-stick-play-station-illustration-png-image_7948317.png" alt="icon kucing" style="width: 50px; height: auto;">
        </a>
        <a class="navbar-brand" href="#">Curriculum Vitae</a>
        <!-- Navbar -->
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse justify-content-end" id="navbarNav">
          <ul class="navbar-nav">
            <li class="nav-item">
              <a class="nav-link" href="#" data-bs-toggle="modal" data-bs-target="#contactModal">Contact</a>
            </li>
          </ul>
        </div>
      </div>
    </header>

    <!-- Modal -->
    <div class="modal fade" id="contactModal" tabindex="-1" aria-labelledby="contactModalLabel" aria-hidden="true">
      <div class="modal-dialog">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title" id="contactModalLabel">Contact Information</h5>
            <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
          </div>
          <div class="modal-body">
            <p>Email: Ardian syahrul@gmail.com</p>
            <p>Phone: +62 87802463555</p>
          </div>
        </div>
      </div>
    </div>

    <div class="container">
      <div class="left">
        <img src="./assets/profile.png" alt="Profile Picture" class="boomerang">
      </div>

      <div class="right">
        <h1>{{ nama }}</h1>
        <h2>{{ npm }}</h2>
        <h3>{{ disukai }}</h3>
        <p>{{ bio }}</p>
        
        <!-- Ikon Instagram -->
        <a href="https://www.instagram.com/ardiansyahruljulian?igsh=OWhlYzF2M3NmazBh" target="_blank" class="icon instagram"><i class="fab fa-instagram"></i></a>
        <!-- Ikon GitHub -->
        <a href="https://github.com/ArdianSyahrulJS" target="_blank" class="icon github"><i class="fab fa-github"></i></a>
        <!--ikon reddit-->
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      nama: 'Hai, Ardian Syahrul Juliawan Suhendra',
      npm: "Npm : 223510408",
      disukai: 'gamer',
      bio: 'Saya berasal dari Kampar, Provinsi Riau, dan lahir pada tanggal 16 Desember 2003 di desa Pangkalan Baru. Pendidikan saya dimulai di SDN 002 Pangkalan Baru, kemudian melanjutkan ke SMPN 2 Siak Hulu, dan SMAN 1 Siak Hulu. Sekarang, saya sedang menempuh pendidikan tinggi di Universitas Islam Riau, Pekanbaru, Riau, dalam program studi S1 Teknik Informatika. Saya memiliki hobi bermain bola voli dan belum memiliki pengalaman kerja.',
    }
  }
}
</script>

<style scoped>
/* Animasi untuk gambar naik dan turun */
@keyframes boomerang {
  0% { transform: translateY(0); } /* Posisi awal (tidak berubah) */
  50% { transform: translateY(-20px); } /* Posisi naik */
  100% { transform: translateY(0); } /* Posisi turun ke posisi awal */
}

/* Mengatur tampilan gambar */
.boomerang {
  animation: boomerang 2s ease-in-out infinite; /* Terapkan animasi boomerang */
}
</style>