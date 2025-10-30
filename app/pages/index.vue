<template>
  <div>
    <UPageHero
      title="José Aristides Amarista Marrón"
      headline="Ingeniero de Software"
      description="Desarrollador Full Stack con experiencia en múltiples tecnologías y frameworks. Apasionado por crear soluciones eficientes y escalables."
      :links="[
        {
          label: 'joseamaristam@gmail.com',
          to: '',
          trailingIcon: 'i-lucide-copy',
          size: 'xl',
          color: 'neutral',
          variant: 'subtle',
          onClick: copyText,
          class: 'cursor-pointer'
        },
        {
          to: 'https://www.linkedin.com/in/jose-aristides-amarista-marron-99b018246/',
          target: '_blank',
          icon: 'i-simple-icons-linkedin',
          size: 'xl',
          color: 'neutral',
          variant: 'subtle'
        },
      ]"
    />

    <USeparator />

    <UPageSection
      id="proyects"
      title="Mis proyectos"
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

    <USeparator />

    <UPageSection
      id="proyects"
      title="Tecnologías"
    >
      <UPageLogos
        :ui="{logos: 'm-0'}"
        :items="[
          'logos-javascript',
          'logos-typescript-icon',
          'logos-vue',
          'logos-react',
        ]"
      />
      <UPageLogos
        :ui="{logos: 'm-0'}"
        :items="[
          'logos-nuxt-icon',
          'logos-nextjs-icon',
          'logos-laravel',
          'logos-symfony',
        ]"
      />
      <UPageLogos
        :ui="{logos: 'm-0'}"
        :items="[
          'logos-php',
          'logos-nodejs',
          'logos-python',
          'logos-fastapi-icon',
        ]"
      />
      <UPageLogos
        :ui="{logos: 'm-0'}"
        :items="[
          'logos-tailwindcss-icon',
          'logos-postgresql',
          'logos-mysql',
          'logos-git',
        ]"
      />
    </UPageSection>
  </div>
</template>

<script setup>
const copyText = async() => {
  await navigator.clipboard.writeText('joseamaristam@gmail.com')
};

const posts = ref([
  {
    title: 'Lector y Firma de PDFs',
    description: 'Aplicación móvil para firmar electrónicamente documentos PDF desde el dispositivo.',
    image: '/pdf1.png',
    to:"/proyects/movil-pdf-sing",
    badge: {
      label: 'Aplicación movil',
      color: 'info'
    },
    authors: [
      {
        name: 'NodeJS',
        avatar: {
          icon: 'logos-nodejs',
          alt: 'NodeJS'
        },
      },
      {
        name: 'React Native',
        avatar: {
          icon: 'logos-react',
          alt: 'React Native'
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
        name: 'SQLite',
        avatar: {
          icon: 'logos-sqlite',
          alt: 'SQLite'
        },
      },
    ]
  },
  {
    title: 'Control de Almacén',
    description: 'Crea y gestiona artículos, proveedores y clientes, gestiona albaranes y controla el stock.',
    image: '/almacen1.png',
    to:"/proyects/web-almacen",
    badge: {
      label: 'Aplicación web',
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
        name: 'TypeScript',
        avatar: {
          icon: 'logos-typescript-icon',
          alt: 'TypeScript'
        },
      },
      {
        name: 'Python',
        avatar: {
          icon: 'logos-python',
          alt: 'Python'
        },
      },
      {
        name: 'FastAPI',
        avatar: {
          icon: 'logos-fastapi-icon',
          alt: 'FastAPI'
        },
      },
    ]
  },
  {
    title: 'TPV',
    description: 'En conjunto con la aplicación de control de almacén, un sistema de TPV para gestionar ventas e imprimir tickets.',
    image: '/tpv1.jpg',
    to:"/proyects/desktop-tpv",
    badge: {
      label: 'Aplicación de escritorio',
      color: 'info'
    },
    authors: [
      {
        avatar: {
          icon: 'logos-vue',
          alt: 'VueJs'
        },
      },
      {
        avatar: {
          icon: 'logos-tauri',
          alt: 'Tauri'
        },
      },
      {
        avatar: {
          icon: 'logos-rust',
          alt: 'Rust'
        },
      },
    ]
  },
  {
    title: 'Gestor de Reuniones',
    description: 'Crea reuniones, envía invitaciones, realiza votaciones y obtén un resumen.',
    image: '/actaldia1.png',
    to:"/proyects/web-reuniones",
    badge: {
      label: 'Aplicación web',
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
    title: 'Gestor de Ordenes IA',
    description: 'Administra de ordenes, premisas y clientes para una empresa de transporte de contenedores.',
    image: '/transflow1.jpg',
    to:"/proyects/web-ordenes-ia",
    badge: {
      label: 'Aplicación web',
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
    title: 'Servicio Verifactu',
    description: 'API RESTful para la gestión de facturas electrónicas según la normativa española.',
    image: '/verifactu_logo.jpg',
    to:'/proyects/api-verifactu',
    badge: {
      label: 'API RESTful',
      color: 'info'
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
    title: 'Administración de Facturas',
    description: 'Plataforma web para gestionar facturas enlazado al verifactu.',
    image: '/efacturando1.jpg',
    to:"/proyects/web-facturas",
    badge: {
      label: 'Aplicación web',
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
    title: 'Plataforma Ever-si',
    description: 'Gestor documental para el mantenimiento de instalaciones segun normativa vigente.',
    image: '/eversi1.png',
    to:"/proyects/web-ever-si",
    badge: {
      label: 'Aplicación web',
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