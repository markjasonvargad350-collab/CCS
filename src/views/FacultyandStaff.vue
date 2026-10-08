<script setup>
import '../styles.css'

const asset = (fileName) => `/assets/${fileName}`
const departments = [
  {
    name: 'College Administration',
    people: [
      {
        name: 'Ma. Christina A. Quijano',
        attainment: 'MSCS',
        role: 'Dean',
        image: asset('dean-quijano.png'),
      },
    ],
  },
  {
    name: 'Department Heads and Coordinators',
    people: [
      {
        name: 'Rea P. Balontong',
        attainment: 'MBA',
        role: 'Department Head, IT and IS',
        image: asset('balontong.jpg'),
      },
      {
        name: 'Marjee Rose B. Parreño',
        attainment: 'MSCS, MBA',
        role: 'Program Coordinator, BSCS, BSDMIA, and MSCS',
        image: asset('parreno.jpg'),
      },
      {
        name: 'Ana Mae B. Cantel',
        attainment: 'MLIS',
        role: 'Program Coordinator, BLIS and MLIS',
        image: asset('cantel.jpg'),
      },
      {
        name: 'Lennon D. Pajar',
        attainment: 'Not listed online',
        role: 'Computer Laboratory Coordinator',
        image: asset('pajar.jpg'),
      },
    ],
  },
  {
    name: 'BSIT and BSIS Program',
    people: [
      {
        name: 'Leo Paulo B. Beldia',
        attainment: 'Not listed online',
        role: 'Faculty',
        image: asset('beldia.jpg'),
      },
      {
        name: 'Lesley Joy L. Dignadice',
        attainment: 'MBA',
        role: 'Faculty',
        image: asset('dignadice.jpg'),
      },
      {
        name: 'Rodolfo C. Eregia, Jr.',
        attainment: 'Not listed online',
        role: 'Faculty',
        image: asset('eregia.jpg'),
      },
      {
        name: 'Donie S. Jardeleza',
        attainment: 'MSCS',
        role: 'Faculty',
        image: asset('jardeleza.jpg'),
      },
      {
        name: 'Antonio M. Montaño, Jr.',
        attainment: 'Not listed online',
        role: 'Faculty',
        image: asset('montano.jpg'),
      },
      {
        name: 'Rose Leah Joy A. Ojacastro',
        attainment: 'MSCS',
        role: 'Faculty',
        image: asset('ojacastro.jpg'),
      },
    ],
  },
  {
    name: 'BSCS, BSDMIA, and Graduate Computing Programs',
    people: [
      {
        name: 'Pedro Peter Rhys B. Cambronero',
        attainment: 'MSCS',
        role: 'BSCS Faculty',
        image: asset('cambronero.jpg'),
      },
      {
        name: 'Ma. Sheila C. Sapul',
        attainment: 'Ph. D.',
        role: 'BSCS Faculty',
        image: asset('sapul.jpg'),
      },
    ],
  },
  {
    name: 'Service and Support Staff',
    people: [
      {
        name: 'Chrislyn C. Castaño',
        attainment: 'Not listed online',
        role: 'Secretary',
        image: asset('castano.jpg'),
      },
      {
        name: 'A.M.P. Latter P. Taasan',
        attainment: 'Not listed online',
        role: 'Computer Laboratory Technician',
        image: asset('taasan.jpg'),
      },
      {
        name: 'Chriselda Elaine Ador',
        attainment: 'Not listed online',
        role: 'Guidance Counselor',
        image: asset('ador.jpg'),
      },
      {
        name: 'Donna May Rivera',
        attainment: 'Not listed online',
        role: 'Library Liaison Officer',
        image: asset('rivera.png'),
      },
    ],
  },
]

</script>

<template>
<section id="faculty" class="faculty-section section-block">
      <div class="section-heading">
        <p class="eyebrow">Mentors and Staff</p>
        <h2>Faculty and Staff</h2>
        <p>
          Personnel are grouped by their published CCS roles and program
          assignments. Educational attainment is shown when listed online.
        </p>
      </div>

      <div class="department-list">
        <section
          v-for="department in departments"
          :key="department.name"
          class="department-group"
          :aria-labelledby="department.name.replaceAll(' ', '-').toLowerCase()"
        >
          <h3 :id="department.name.replaceAll(' ', '-').toLowerCase()">
            {{ department.name }}
          </h3>
          <div class="people-grid">
            <article v-for="person in department.people" :key="person.name" class="person-card">
              <img :src="person.image" :alt="`${person.name} photo`" />
              <div>
                <h4>{{ person.name }}</h4>
                <p>{{ person.role }}</p>
                <span>Highest attainment: {{ person.attainment }}</span>
              </div>
            </article>
          </div>
        </section>
      </div>
    </section>

</template>

<style>

</style>