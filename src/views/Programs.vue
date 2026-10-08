<script> 
const programs = [
  {
    code: 'BSIT',
    name: 'Bachelor of Science in Information Technology',
    logo: asset('program-bsit.png'),
    description:
      'Designed to bridge computer science and management information systems, with focus on infrastructure, systems administration, networking, databases, information security, and technology support.',
    highlights: ['Network architecture', 'Systems administration', 'Information security'],
  },
  {
    code: 'BSCS',
    name: 'Bachelor of Science in Computer Science',
    logo: asset('program-bscs.png'),
    description:
      'Built for students who want to study computing in depth through algorithms, software design, computer systems, theory, and new developments in computing.',
    highlights: ['Algorithms', 'Software development', 'Computing theory'],
  },
  {
    code: 'BSDMIA',
    name: 'Bachelor of Science in Digital Media and Interactive Arts',
    logo: asset('program-bsdmia.png'),
    description:
      'Focused on creativity, applied arts, and digital media technologies for animation, video editing, 3D modeling, photography, graphic design, game design, and interactive experiences.',
    highlights: ['Digital storytelling', 'Interactive design', 'Creative production'],
  },
  {
    code: 'BLIS',
    name: 'Bachelor of Library and Information Science',
    logo: asset('program-blis.png'),
    description:
      'A four-year program that prepares students to develop, deploy, organize, and manage information resources in print, non-print, electronic, and digital formats.',
    highlights: ['Information resources', 'Library systems', 'Digital collections'],
  },
]
import './styles.css'; 

</script>

<template>

    <section id="programs" class="program-section section-block">
      <div class="section-heading">
        <p class="eyebrow">Academic Programs</p>
        <h2>Programs Offered</h2>
        <p>
          Four CCS degree programs serving software, infrastructure, digital
          media, and information science careers.
        </p>
      </div>

      <div class="program-grid">
        <article v-for="program in programs" :key="program.code" class="program-card">
          <div class="program-card-top">
            <img :src="program.logo" :alt="`${program.code} logo`" />
            <span>{{ program.code }}</span>
          </div>
          <h3>{{ program.name }}</h3>
          <p>{{ program.description }}</p>
          <ul>
            <li v-for="highlight in program.highlights" :key="highlight">
              {{ highlight }}
            </li>
          </ul>
        </article>
      </div>
    </section>

</template>

<style>


</style>