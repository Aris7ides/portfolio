<template>
  <div>
    <UPageHero
      title="José Aristides Amarista Marrón"
      description="Ingeniero de Software"
      :links="[{
        label: 'Contactar',
        to: 'https://www.linkedin.com/in/jose-aristides-amarista-marron-99b018246/',
        target: '_blank',
        icon: 'i-simple-icons-linkedin',
        size: 'xl',
        color: 'neutral',
        variant: 'subtle'
      }]"
    />

    <UPageLogos
      title="Frontend"
      :items="[
        'logos-javascript',
        'logos-typescript-icon',
        'logos-vue',
        'logos-nuxt-icon',
        'logos-react',
        'logos-nextjs-icon',
      ]"
    />

    <UPageLogos
      title="Backend"
      :items="[
        'logos-php',
        'logos-laravel',
        'logos-symfony',
        'logos-nodejs',
        'logos-mysql',
        'logos-postgresql',
        'logos-python',
        'logos-django-icon',
        'logos-git',
      ]"
    />
  <UPageSection
    id="proyects"
    title="Algunos de mis proyectos"
    description=""
  >
    <UBlogPosts>
      <UBlogPost
        v-for="(post, index) in posts"
        :key="index"
        v-bind="post"
      />
    </UBlogPosts>
  </UPageSection>

    <UPageSection>
      <UPageCTA
        title="Ready to build your next Nuxt app?"
        description="Join thousands of developers building with Nuxt and Nuxt UI. Get this template and start shipping today."
        variant="subtle"
        :links="[{
          label: 'Start building',
          to: 'https://ui4.nuxt.com/docs/getting-started/installation/nuxt',
          target: '_blank',
          trailingIcon: 'i-lucide-arrow-right',
          color: 'neutral'
        }, {
          label: 'View on GitHub',
          to: 'https://github.com/nuxt-ui-templates/starter',
          target: '_blank',
          icon: 'i-simple-icons-github',
          color: 'neutral',
          variant: 'outline'
        }]"
      />
    </UPageSection>
  </div>
</template>

<script setup>
const posts = ref([
  {
    title: 'Actaldia',
    description: 'Plataforma para gestionar reuniones y conovocar asistentes.',
    image: '/actaldia1.png',
    to:"https://actaldia.com/admin/",
    target:"_blank",
    badge: {
      label: 'Desarrollo total',
      color: 'success'
    },
    authors: [
      {
        name: 'VueJs',
        avatar: {
          icon: 'logos-vue',
          alt: 'VueJs'
        },
      },
      {
        name: 'TypeScript',
        avatar: {
          icon: 'logos-typescript-icon',
          alt: 'TypeScript'
        },
      },
      {
        name: 'PHP',
        avatar: {
          icon: 'logos-php',
          alt: 'PHP'
        },
      },
      {
        name: 'Laravel',
        avatar: {
          icon: 'logos-laravel',
          alt: 'Laravel'
        },
      },
    ]
  },
  {
    title: 'Sistema de Almacén',
    description: 'Plataforma web para la gestión de artículos, compras, ventas, stock, albaranes, devoluciones y demás.',
    image: '/almacen1.png',
    to:"https://macau.servicios-empresa.com",
    target:"_blank",
    badge: {
      label: 'Desarrollo total',
      color: 'success'
    },
    authors: [
      {
        name: 'VueJs',
        avatar: {
          icon: 'logos-vue',
          alt: 'VueJs'
        },
      },
      {
        name: 'TypeScript',
        avatar: {
          icon: 'logos-typescript-icon',
          alt: 'TypeScript'
        },
      },
      {
        name: 'ASP',
        avatar: {
          icon: 'vscode-icons:file-type-asp',
          alt: 'ASP'
        },
      },
    ]
  },
  {
    title: 'Servicio de Verifactu',
    description: 'Servicio web para el envio de facturas a hacienda cumpliendo con la ley del verifactu.',
    image: '/verifactu_logo.jpg',
    badge: {
      label: 'Desarrollo total',
      color: 'success'
    },
    authors: [
      {
        name: 'C#',
        avatar: {
          icon: 'logos-c-sharp',
          alt: 'C#'
        },
      },
      {
        name: '.NET',
        avatar: {
          icon: 'logos-dotnet',
          alt: '.NET'
        },
      },
    ]
  },
  {
    title: 'eFacturando',
    description: 'Plataforma web para gestionar facturas enlazado al verifactu.',
    image: '/efacturando1.jpg',
    to:"https://efacturando.es",
    target:"_blank",
    badge: {
      label: 'Desarrollo parcial',
      color: 'info'
    },
    authors: [
      {
        name: 'VueJs',
        avatar: {
          icon: 'logos-vue',
          alt: 'VueJs'
        },
      },
      {
        name: 'JavaScript',
        avatar: {
          icon: 'logos-javascript',
          alt: 'JavaScript'
        },
      },
      {
        name: 'ASP',
        avatar: {
          icon: 'vscode-icons:file-type-asp',
          alt: 'ASP'
        },
      },
    ]
  },
  {
    title: 'TransFlowIA',
    description: 'Plataforma web para la gestión de ordenes de transporte usando IA.',
    image: '/transflow1.jpg',
    to:"https://transporte.servicios-empresa.com",
    target:"_blank",
    badge: {
      label: 'Desarrollo total',
      color: 'success'
    },
    authors: [
      {
        name: 'VueJs',
        avatar: {
          icon: 'logos-vue',
          alt: 'VueJs'
        },
      },
      {
        name: 'JavaScript',
        avatar: {
          icon: 'logos-javascript',
          alt: 'JavaScript'
        },
      },
      {
        name: 'ASP',
        avatar: {
          icon: 'vscode-icons:file-type-asp',
          alt: 'ASP'
        },
      },
      {
        name: 'ChatGPT',
        avatar: {
          icon: 'hugeicons:chat-gpt',
          alt: 'ChatGPT'
        },
      },
    ]
  },
  {
    title: 'Sistema de TPV',
    description: 'Aplicación de TPV enlazada a almacén para gestión de productos y stock. Desarrollada con Delphi 12.',
    image: '/tpv1.jpg',
    badge: {
      label: 'Desarrollo total',
      color: 'success'
    },
    authors: [
      {
        avatar: {
          icon: 'vscode-icons:file-type-asp',
          alt: 'ASP'
        },
      },
    ]
  },
  {
    title: 'Plataforma Ever-si',
    description: 'Gestor documental web para la seguridad industrial.',
    image: '/eversi1.png',
    to:"https://ever-si.es/",
    target:"_blank",
    badge: {
      label: 'Desarrollo parcial',
      color: 'info'
    },
    authors: [
      {
        name: 'PHP',
        avatar: {
          icon: 'logos-php',
          alt: 'PHP'
        },
      },
      {
        name: 'Symfony',
        avatar: {
          icon: 'logos-symfony',
          alt: 'Symfony'
        },
      },
      {
        name: 'MySQL',
        avatar: {
          icon: 'logos-mysql',
          alt: 'MySQL'
        },
      }
    ]
  },
])
</script>