<script setup>
import '../styles.css'

const asset = (fileName) => `/assets/${fileName}`
const partners = [
  { name: 'Oracle Academy', logo: asset('partner-oracle.png') },
  { name: 'Cisco Networking Academy', logo: asset('partner-cisco.png') },
  { name: 'Acer Academy', logo: asset('partner-acer.jpg') },
  { name: 'Huawei ICT Academy', logo: asset('partner-huawei.jpg') },
  { name: 'iNAL', logo: asset('partner-inal.png') },
  { name: 'GoveSmart', logo: asset('partner-govesmart.jpg') },
  { name: 'Mayad Studios', logo: asset('partner-mayad.png') },
  { name: 'LasorTech', logo: asset('partner-lasortech.jpg') },
  { name: 'Startup Project', logo: asset('partner-startup.jpg') },
]

</script>

<template>
<section id="partners" class="partner-section section-block">
      <div class="section-heading">
        <p class="eyebrow">Connect</p>
        <h2>Partnerships and Memberships</h2>
        <p>
          CCS builds industry and academic connections through technology
          academies, creative partners, and innovation networks.
        </p>
      </div>

      <div class="partner-grid">
        <article v-for="partner in partners" :key="partner.name" class="partner-card">
          <img :src="partner.logo" :alt="`${partner.name} logo`" />
          <span>{{ partner.name }}</span>
        </article>
      </div>
    </section>

</template>

<style>

</style>