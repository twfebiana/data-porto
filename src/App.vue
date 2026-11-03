<template>
  <div class="min-h-screen bg-[#fbf8f1] text-[#2b2b2b] font-serif selection:bg-[#e2d5c3]">
    
    <!-- Top Navigation -->
    <nav class="border-b border-[#e2d5c3] sticky top-0 z-20 bg-[#fbf8f1]/90 backdrop-blur-sm">
      <div class="max-w-5xl mx-auto px-8 py-3 flex justify-between items-center text-xs tracking-widest uppercase font-semibold text-[#5c5c5c]">
        <span>Data Insight</span>
        <span>Analisis Penjualan Ritel</span>
      </div>
    </nav>

    <!-- Magazine Header -->
    <header class="bg-white pt-16 pb-12 border-b border-[#e2d5c3]">
      <div class="max-w-5xl mx-auto px-8">
        <h1 class="text-4xl md:text-6xl font-extrabold leading-tight mb-4 text-[#1a1a1a]">
          Analisis Penjualan Ritel 2003-2005.
        </h1>
        <h2 class="text-xl md:text-2xl text-[#5c5c5c] italic mb-6 border-l-4 border-[#dfcd93] pl-4">
          Melihat tren penjualan, pasar global, dan produk dengan kontribusi terbesar melalui data transaksi historis.
        </h2>
        <div class="bg-[#f9f6f0] inline-block px-4 py-2 text-xs font-mono text-[#5c5c5c] border border-[#e2d5c3] mb-8">
          Note: Dataset diperoleh dari program RevoU dan digunakan sebagai bahan studi kasus analisis data.
        </div>
        <div class="flex items-center gap-6 text-xs uppercase tracking-widest text-[#5c5c5c]">
          <span> Oleh Tri Wahyu Febiana </span>
        </div>
      </div>
    </header>

    <main class="w-full">
      
      <!-- Latar Belakang & Pertanyaan Penelitian -->
      <section class="w-full bg-[#f4efe6] py-16 border-b border-[#e2d5c3]">
        <div class="max-w-5xl mx-auto px-8 grid grid-cols-1 md:grid-cols-12 gap-12 items-center">
          <div class="md:col-span-7">
            <h3 class="text-xs font-bold uppercase tracking-widest text-[#5c5c5c] mb-2">Latar Belakang</h3>
            <h4 class="text-3xl font-bold mb-4">Mengapa Analisis Ini Diperlukan?</h4>
            <p class="text-sm leading-loose text-justify">
              Data penjualan dapat membantu perusahaan memahami perkembangan bisnis, mengenali pola belanja pelanggan, dan menentukan pasar yang perlu diperhatikan. Dalam analisis ini, data transaksi historis digunakan untuk melihat tren penjualan, kontribusi wilayah, serta kategori produk dan skala transaksi yang menghasilkan pendapatan terbesar.
            </p>
          </div>
          
          <div class="md:col-span-5 bg-white p-8 shadow-sm border border-[#e2d5c3]">
            <h4 class="text-lg font-bold mb-4 border-b border-[#d1c4b5] pb-2">Pertanyaan Penelitian</h4>
            <ul class="space-y-4">
              <li class="flex items-start gap-3">
                <span class="text-[#dfcd93] text-xl font-bold">1</span>
                <p class="text-sm font-medium leading-relaxed">Bagaimana perkembangan penjualan dari tahun ke tahun, dan pada bulan apa penjualan mencapai nilai tertinggi?</p>
              </li>
              <li class="flex items-start gap-3">
                <span class="text-[#dfcd93] text-xl font-bold">2</span>
                <p class="text-sm font-medium leading-relaxed">Negara mana yang memberikan kontribusi penjualan terbesar, khususnya untuk produk Classic Cars?

</p>
              </li>
              <li class="flex items-start gap-3">
                <span class="text-[#dfcd93] text-xl font-bold">3</span>
                <p class="text-sm font-medium leading-relaxed">Kategori produk dan skala transaksi mana yang memberikan kontribusi terbesar terhadap total penjualan?</p>
              </li>
            </ul>
          </div>
        </div>
      </section>

      <!-- Integritas Data -->
      <section class="w-full bg-white py-16 border-b border-[#e2d5c3]">
        <div class="max-w-5xl mx-auto px-8">
          <div class="text-center mb-10">
            <h3 class="text-xs font-bold uppercase tracking-widest text-[#5c5c5c] mb-2">Persiapan Data</h3>
            <h4 class="text-3xl font-bold mb-3">Memeriksa Kualitas Dataset</h4>
            <p class="text-sm leading-loose text-[#5c5c5c] max-w-2xl mx-auto">
              Sebelum melakukan analisis, dataset diperiksa untuk memastikan data dapat digunakan dan hasil analisis tidak dipengaruhi oleh masalah kualitas data.
            </p>
          </div>
          
          <div class="grid grid-cols-1 md:grid-cols-4 gap-6">
            <div class="bg-[#f9f6f0] p-6 border border-[#e2d5c3] flex flex-col justify-between">
              <div>
                <h5 class="font-bold text-sm mb-1">Jumlah Data</h5>
                <p class="text-3xl font-bold text-[#1a1a1a] mb-3">2.823</p>
              </div>
              <p class="text-xs leading-relaxed text-[#5c5c5c]">baris transaksi.</p>
            </div>
            <div class="bg-[#f9f6f0] p-6 border border-[#e2d5c3] flex flex-col justify-between">
              <div>
                <h5 class="font-bold text-sm mb-1">Data Duplikat</h5>
                <p class="text-3xl font-bold text-[#1a1a1a] mb-3">Nihil</p>
              </div>
              <p class="text-xs leading-relaxed text-[#5c5c5c]">Tidak ditemukan ID pesanan yang duplikat.</p>
            </div>
            <div class="bg-[#f9f6f0] p-6 border border-[#e2d5c3] flex flex-col justify-between">
              <div>
                <h5 class="font-bold text-sm mb-1">Missing Values</h5>
                <p class="text-3xl font-bold text-[#1a1a1a] mb-3">Aman</p>
              </div>
              <p class="text-xs leading-relaxed text-[#5c5c5c]"> Hanya ditemukan pada kolom alamat jalan.</p>
            </div>
            <div class="bg-[#f9f6f0] p-6 border border-[#e2d5c3] flex flex-col justify-between border-b-4 border-b-[#dfcd93]">
              <div>
                <h5 class="font-bold text-sm mb-1">Total Penjualan</h5>
                <p class="text-3xl font-bold text-[#1a1a1a] mb-3">$10 Juta</p>
              </div>
              <p class="text-xs leading-relaxed text-[#5c5c5c]">Akumulasi berdasarkan data transaksi yang tersedia.</p>
            </div>
          </div>
        </div>
      </section>

      <!-- Temuan 1: Tren Penjualan Tahunan dan Bulanan -->
      <section class="w-full bg-[#f4efe6] py-16 border-b border-[#e2d5c3]">
        <div class="max-w-5xl mx-auto px-8">
          <div class="mb-10 text-center">
            <h3 class="text-xs font-bold uppercase tracking-widest text-[#5c5c5c] mb-2">Temuan 1</h3>
            <h4 class="text-3xl font-bold mb-3">Tren Penjualan Tahunan dan Bulanan</h4>
            <p class="text-sm leading-loose text-[#5c5c5c] max-w-2xl mx-auto">
              Analisis dilakukan untuk melihat perkembangan penjualan setiap tahun dan mengidentifikasi bulan dengan penjualan tertinggi.
            </p>
          </div>

          <div class="grid grid-cols-1 md:grid-cols-2 gap-10">
            <!-- Yearly Box -->
            <div class="bg-white p-6 shadow-sm border border-[#e2d5c3]">
              <h5 class="font-bold mb-4 border-b border-[#d1c4b5] pb-2 text-center">Penjualan Tahunan</h5>
              <div class="w-full mb-6"><canvas id="yearlyChart" class="w-full h-48"></canvas></div>
              <p class="text-sm leading-loose text-justify">
                <strong>Temuan 1A:</strong> Penjualan tahun <strong class="text-black">2004</strong> meningkat sekitar <mark class="bg-[#dfcd93]/60 px-1 font-bold text-black rounded">34%</mark> dibandingkan 2003. Penjualan 2005 terlihat lebih rendah karena data hanya tersedia hingga Mei.
              </p>
            </div>

            <!-- Monthly Box -->
            <div class="bg-white p-6 shadow-sm border border-[#e2d5c3]">
              <h5 class="font-bold mb-4 border-b border-[#d1c4b5] pb-2 text-center">Penjualan Bulanan (2004)</h5>
              <div class="w-full mb-6"><canvas id="monthlyChart" class="w-full h-48"></canvas></div>
              <p class="text-sm leading-loose text-justify">
                <strong>Temuan 1B:</strong> Penjualan tertinggi terjadi pada <strong class="text-black">November</strong>, mencapai <mark class="bg-[#dfcd93]/60 px-1 font-bold text-black rounded">$1.089.048</mark>. Nilai ini bahkan lebih tinggi dibandingkan total penjualan pada Januari hingga Maret.
              </p>
            </div>
          </div>
        </div>
      </section>

      <!-- Temuan 2: Penjualan Berdasarkan Negara -->
      <section class="w-full bg-white py-16 border-b border-[#e2d5c3]">
        <div class="max-w-5xl mx-auto px-8 grid grid-cols-1 md:grid-cols-12 gap-12 items-center">
          <div class="md:col-span-5">
            <h3 class="text-xs font-bold uppercase tracking-widest text-[#5c5c5c] mb-2">Temuan 2</h3>
            <h4 class="text-3xl font-bold mb-4">Pasar Utama Classic Cars</h4>
            <p class="text-sm leading-loose text-justify mb-6">
              Analisis berdasarkan negara digunakan untuk mengetahui pasar dengan kontribusi penjualan terbesar pada kategori Classic Cars.
            </p>
            <div class="bg-[#f9f6f0] p-5 border-l-4 border-[#dfcd93]">
              <p class="text-sm leading-loose text-justify">
                <strong>Temuan 2:</strong> <strong class="text-black">Amerika Serikat</strong> mencatat penjualan Classic Cars tertinggi, yaitu sekitar <mark class="bg-[#e2b4bd]/50 px-1 font-bold text-black rounded">$560.448</mark>. Nilai ini jauh lebih tinggi dibandingkan negara lain dalam lima pasar teratas.
              </p>
            </div>
          </div>
          <div class="md:col-span-7 bg-[#f9f6f0] p-6 shadow-sm border border-[#e2d5c3]">
            <canvas id="countryChart" class="w-full h-64"></canvas>
          </div>
        </div>
      </section>

      <!-- Temuan 3: Produk dan Skala Transaksi -->
      <section class="w-full bg-[#f4efe6] py-16 border-b border-[#e2d5c3]">
        <div class="max-w-5xl mx-auto px-8">
          <div class="text-center mb-10">
            <h3 class="text-xs font-bold uppercase tracking-widest text-[#5c5c5c] mb-2">Temuan 3</h3>
            <h4 class="text-3xl font-bold mb-3">Kontribusi Produk dan Skala Transaksi</h4>
            <p class="text-sm leading-loose text-[#5c5c5c] max-w-2xl mx-auto">
              Analisis ini melihat kategori produk dan skala transaksi yang memberikan kontribusi terbesar terhadap total penjualan.
            </p>
          </div>

          <div class="grid grid-cols-1 md:grid-cols-2 gap-12">
            <!-- Box for Product -->
            <div class="bg-white p-6 shadow-sm border border-[#e2d5c3]">
              <h5 class="font-bold text-center mb-4 border-b border-[#d1c4b5] pb-2">Kontribusi Penjualan Produk</h5>
              <div class="w-full flex justify-center mb-6">
                <div class="h-48 w-full"><canvas id="productChart"></canvas></div>
              </div>
              <p class="text-sm leading-loose text-center">
                <strong>Temuan 3A:</strong> Kategori <strong class="text-black font-bold">Classic Cars</strong> memberikan kontribusi terbesar, yaitu sekitar <mark class="bg-[#dfcd93]/60 px-1 font-bold text-black rounded">38%</mark> dari total penjualan.
              </p>
            </div>

            <!-- Box for Deals -->
            <div class="bg-white p-6 shadow-sm border border-[#e2d5c3]">
              <h5 class="font-bold text-center mb-4 border-b border-[#d1c4b5] pb-2">Kontribusi Skala Transaksi</h5>
              <div class="w-full flex justify-center mb-6">
                <div class="h-48 w-full"><canvas id="dealChart"></canvas></div>
              </div>
              <p class="text-sm leading-loose text-center">
                <strong>Temuan 3B:</strong> Transaksi kategori <strong class="text-black">Medium</strong> menyumbang lebih dari <mark class="bg-[#dfcd93]/60 px-1 font-bold text-black rounded">60%</mark> dari total penjualan, menjadikannya skala transaksi dengan kontribusi terbesar.
              </p>
            </div>
          </div>
        </div>
      </section>

      <!-- Kesimpulan dan Rekomendasi -->
      
      <!-- Kesimpulan -->
      <section class="w-full bg-white py-16">
        <div class="max-w-4xl mx-auto px-8">
          <div class="bg-[#2b2b2b] text-[#fbf8f1] p-10 rounded-sm shadow-xl border-t-4 border-[#dfcd93]">
            <h3 class="text-xs font-bold uppercase tracking-widest text-[#dfcd93] mb-2 text-center">Kesimpulan</h3>
            <h4 class="text-3xl font-bold mb-8 text-center border-b border-[#5c5c5c] pb-6">Ringkasan Hasil Analisis</h4>

            <div class="space-y-8">
              <div class="flex gap-4">
                <div class="text-[#dfcd93] font-bold text-2xl">01.</div>
                <div>
                  <h5 class="font-bold uppercase tracking-widest text-white mb-2">Tren Penjualan</h5>
                  <p class="text-sm leading-loose text-[#d4c5b9]">
                    Penjualan meningkat 34% pada 2004 dibandingkan 2003. Pada 2004, November menjadi bulan dengan penjualan tertinggi, mencapai $1.089.048. Sementara itu, nilai penjualan 2005 masih mencakup data hingga Mei.
                  </p>
                </div>
              </div>

              <div class="flex gap-4">
                <div class="text-[#dfcd93] font-bold text-2xl">02.</div>
                <div>
                  <h5 class="font-bold uppercase tracking-widest text-white mb-2">Pasar Classic Cars</h5>
                  <p class="text-sm leading-loose text-[#d4c5b9]">
                    Amerika Serikat mencatat nilai penjualan Classic Cars tertinggi sebesar $560.448, lebih tinggi dibandingkan negara lain dalam lima pasar teratas yang dianalisis.
                  </p>
                </div>
              </div>

              <div class="flex gap-4">
                <div class="text-[#dfcd93] font-bold text-2xl">03.</div>
                <div>
                  <h5 class="font-bold uppercase tracking-widest text-white mb-2">Kontribusi Produk dan Deal Size</h5>
                  <p class="text-sm leading-loose text-[#d4c5b9]">
                    Classic Cars menjadi kategori produk dengan kontribusi penjualan terbesar, yakni 38%. Berdasarkan kategori deal size pada dataset, kategori Medium menyumbang nilai penjualan terbesar, yakni 60,7% dari total penjualan.
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>



    </main>

    <!-- Footer -->
    <footer class="border-t border-[#e2d5c3] bg-[#f4efe6]">
      <div class="max-w-5xl mx-auto px-8 py-10 text-center text-[#5c5c5c] text-xs font-semibold tracking-widest uppercase">
        <p>© 2026 Analitik Data Ritel</p>
      </div>
    </footer>
  </div>
</template>

<script setup>
import { onMounted } from 'vue'
import Chart from 'chart.js/auto'

onMounted(() => {
  // Styling Global Chart.js untuk tema Serif Majalah
  Chart.defaults.font.family = "'Georgia', 'Times New Roman', serif";
  Chart.defaults.color = '#5c5c5c';
  Chart.defaults.scale.grid.color = 'rgba(209, 196, 181, 0.4)';
  Chart.defaults.plugins.tooltip.backgroundColor = '#2b2b2b';
  Chart.defaults.plugins.tooltip.titleColor = '#fbf8f1';
  Chart.defaults.plugins.tooltip.bodyColor = '#fbf8f1';
  Chart.defaults.plugins.tooltip.padding = 10;

  const pastelBlue = '#a9bcd0';
  const pastelSage = '#b2c2b0';
  const pastelRose = '#e2b4bd';
  const pastelSand = '#d4c5b9';
  const pastelMustard = '#dfcd93';

  // 1. Chart Tren Tahunan
  const ctxYearly = document.getElementById('yearlyChart');
  new Chart(ctxYearly, {
    type: 'bar',
    data: {
      labels: ['2003', '2004', '2005'],
      datasets: [{
        label: 'Total Penjualan (USD)',
        data: [3516979, 4724162, 1791486],
        backgroundColor: [pastelSand, pastelBlue, pastelSand],
        borderRadius: 2,
      }]
    },
    options: {
      responsive: true,
      maintainAspectRatio: false,
      plugins: { legend: { display: false } },
      scales: {
        y: { beginAtZero: true, border: {display: false}, ticks: { callback: (value) => '$' + (value/1000000).toFixed(1) + 'M' } },
        x: { grid: { display: false }, border: {display: false} }
      }
    }
  });

  // 2. Chart Dinamika Bulanan 2004
  const ctxMonthly = document.getElementById('monthlyChart');
  new Chart(ctxMonthly, {
    type: 'line',
    data: {
      labels: ['Jan', 'Feb', 'Mar', 'Apr', 'Mei', 'Jun', 'Jul', 'Agt', 'Sep', 'Okt', 'Nov', 'Des'],
      datasets: [{
        label: 'Pendapatan 2004',
        data: [316577, 311419, 205733, 206148, 273438, 286674, 327144, 461501, 320750, 552924, 1089048, 372802],
        borderColor: pastelSage,
        backgroundColor: 'rgba(178, 194, 176, 0.2)',
        borderWidth: 3,
        fill: true,
        tension: 0.4,
        pointBackgroundColor: '#2b2b2b'
      }]
    },
    options: {
      responsive: true,
      maintainAspectRatio: false,
      plugins: { legend: { display: false } },
      scales: {
        y: { beginAtZero: true, border: {display: false}, ticks: { callback: (value) => '$' + (value/1000).toFixed(0) + 'K' } },
        x: { grid: { display: false }, border: {display: false} }
      }
    }
  });

  // 3. Chart Negara (USA)
  const ctxCountry = document.getElementById('countryChart');
  new Chart(ctxCountry, {
    type: 'bar',
    data: {
      labels: ['USA', 'Spanyol', 'Prancis', 'Swiss', 'Jerman'],
      datasets: [{
        label: 'Classic Cars (USD)',
        data: [560448, 209568, 184361, 117713, 92821],
        backgroundColor: [pastelRose, pastelSand, pastelSand, pastelSand, pastelSand],
        borderRadius: 2,
      }]
    },
    options: {
      indexAxis: 'y',
      responsive: true,
      maintainAspectRatio: false,
      plugins: { legend: { display: false } },
      scales: {
        x: { border: {display: false}, ticks: { callback: (value) => '$' + (value/1000).toFixed(0) + 'K' } },
        y: { grid: { display: false }, border: {display: false} }
      }
    }
  });

  // 4. Chart Portofolio Produk
  const ctxProduct = document.getElementById('productChart');
  new Chart(ctxProduct, {
    type: 'doughnut',
    data: {
      labels: ['Classic Cars', 'Vintage', 'Lainnya'],
      datasets: [{
        data: [38, 21, 41],
        backgroundColor: [pastelBlue, pastelSage, pastelSand],
        borderColor: '#ffffff',
        borderWidth: 2,
      }]
    },
    options: {
      responsive: true,
      maintainAspectRatio: false,
      cutout: '65%',
      plugins: { legend: { position: 'bottom' } }
    }
  });

  // 5. Chart Deal Size
  const ctxDeal = document.getElementById('dealChart');
  new Chart(ctxDeal, {
    type: 'pie',
    data: {
      labels: ['Medium', 'Small', 'Large'],
      datasets: [{
        data: [6087432, 2643077, 1302119],
        backgroundColor: [pastelMustard, pastelRose, pastelSand],
        borderColor: '#ffffff',
        borderWidth: 2,
      }]
    },
    options: {
      responsive: true,
      maintainAspectRatio: false,
      plugins: { legend: { position: 'bottom' } }
    }
  });
})
</script>