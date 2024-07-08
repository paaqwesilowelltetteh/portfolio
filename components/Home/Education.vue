<template>
  <div>
    <h2 class="uppercase text-xs font-semibold text-gray-400 mb-6">
      EDUCATION
    </h2>
    <div class="space-y-4">
      <AppEducationCard v-for="education in educations" :key="education.id" :education="education" />
    </div>
    <div class="flex items-center justify-center mt-6 text-sm">
      <UButton label="Detailed Info on Education &rarr;" to="/projects" variant="link" color="gray" />
    </div>
  </div>
</template>

<script lang="ts" setup>

const rawEducations = ref([
  {
    id: 1,
    year: '2015 – 2019',
    name: 'Pentecost University',
    location: 'Sowutuom - Accra - Ghana',
    degree: 'Bachelor of Science in Information Technology',
    link: 'https://www.pentvars.edu.gh/',
    logo: 'https://z-p3-scontent.facc9-1.fna.fbcdn.net/v/t39.30808-6/419890346_758328679666087_8086500931978924664_n.jpg?_nc_cat=105&ccb=1-7&_nc_sid=6ee11a&_nc_ohc=eRr61y0YgKEQ7kNvgFrLTc0&_nc_ht=z-p3-scontent.facc9-1.fna&oh=00_AYDJ3wA8-97E3olqAkoExLmU9xdjzCwdcP2eyb0Avv9DSg&oe=6691FBB6',
    description: 'Studied courses such as Computer Programming in (C, Visual Basic, PHP, Java), Web Development, Computer Networking, etc.'
  },
  {
    id: 2,
    year: '2013 – 2015',
    name: 'NextGen IT solutions',
    location: 'Tema - Accra - Ghana',
    degree: 'Software/Hardware, Networking, Server configuration, etc.',
    link: '#',
    // logo: 'https://www.nextgenit.com/images/logo.png',
    description: 'Studied computer networking, server configuration, hardware, etc.'
  }
]);

const educations = computed(() => {
  return rawEducations.value.map(education => ({
    ...education,
    description: education.description.replace(/<br>/g, '\n')
  }));
});
</script>
