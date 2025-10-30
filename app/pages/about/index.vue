<template>
  <UContainer>
    <UPageHero
        title="José Aristides Amarista Marrón"
        headline="Ingeniero de Software"
        description="Desarrollador Full Stack con experiencia en múltiples tecnologías y frameworks. Apasionado por crear soluciones eficientes y escalables."
        :links="[
          {
            label: 'CV',
            to: '',
            trailingIcon: 'vscode-icons-file-type-pdf2',
            size: 'xl',
            color: 'error',
            variant: 'solid',
            class: 'cursor-pointer'
          },
        ]"
      />
  
      <USeparator />
      
      <UPageSection title="Experiencia">
        <UTimeline :items="items" />
      </UPageSection>

      <USeparator />
      
      <UPageSection title="Formación">
        <UTimeline :items="items" />
      </UPageSection>

      <USeparator />
      
      <UPageSection title="Cursos y Certificaciones">
        <UTimeline :items="items" />
      </UPageSection>

      <USeparator />
      
      <UPageSection title="Experiencia">
        <UTimeline :items="items" />
      </UPageSection>

      <USeparator />
      
      <UPageSection title="Otra cosa">
        <UTimeline :items="items" />
      </UPageSection>
  </UContainer>
</template>

<script setup lang="ts">
const items = ref([
  {
    date: 'Mar 15, 2025',
    title: 'Project Kickoff',
    description: 'Kicked off the project with team alignment. Set up project milestones and allocated resources.',
    icon: 'i-lucide-rocket'
  },
  {
    date: 'Mar 22 2025',
    title: 'Design Phase',
    description: 'User research and design workshops. Created wireframes and prototypes for user testing.',
    icon: 'i-lucide-palette'
  },
  {
    date: 'Mar 29 2025',
    title: 'Development Sprint',
    description: 'Frontend and backend development. Implemented core features and integrated with APIs.',
    icon: 'i-lucide-code'
  },
  {
    date: 'Apr 5 2025',
    title: 'Testing & Deployment',
    description: 'QA testing and performance optimization. Deployed the application to production.',
    icon: 'i-lucide-check-circle'
  }
])
</script>