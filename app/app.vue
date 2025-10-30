<script setup lang="ts">
import type { NavigationMenuItem } from '@nuxt/ui'
import { useLogo } from '@/composables/useLogo';

const email = ref<string>('joseamaristam@gmail.com')

useHead({
  meta: [
    { name: 'viewport', content: 'width=device-width, initial-scale=1' }
  ],
  link: [
    { rel: 'icon', href: '/favicon.ico' }
  ],
  htmlAttrs: {
    lang: 'en'
  }
})

const title = 'José Amarista - Portfolio'
const description = 'Portfolio by José Amarista. Software Inginner.'

useSeoMeta({
  title,
  description,
  ogTitle: title,
  ogDescription: description,
  ogImage: 'https://ui4.nuxt.com/assets/templates/nuxt/starter-light.png',
  twitterImage: 'https://ui4.nuxt.com/assets/templates/nuxt/starter-light.png',
  twitterCard: 'summary_large_image'
})

const route = useRoute()

const items = computed<NavigationMenuItem[]>(() => [{
  label: 'Inicio',
  icon: 'i-heroicons-home-solid',
  to: '/',
  active: route.path.toString() === '/'
}, {
  label: 'Sobre mi',
  icon: 'i-heroicons-user-solid',
  to: '/about',
  active: route.path.startsWith('/about')
}, {
  label: 'Mis proyectos',
  icon: 'i-heroicons-briefcase-solid',
  to: '/#proyects',
  active: route.path.startsWith('/proyects')
}])

const { logoUrl } = useLogo();

const copyText = async() => {
  await navigator.clipboard.writeText(email.value)
};
</script>

<template>
  <UApp>
    <div class="block xl:flex justify-center items-center bg-gray-100 dark:bg-accented">
      <div class="xl:w-3/4">
        <UHeader
         :ui="{root: 'xl:rounded-full xl:border xl:mt-2'}">
          <template #left>
            <NuxtLink to="/" class="hover:scale-110">
              <img :src="logoUrl" class="w-auto h-12 shrink-0" />
            </NuxtLink>
          </template>
    
          <!-- Escritorio menu -->
          <UNavigationMenu :items="items"/>
          
          <!-- Mobile menu -->
          <template #body>
            <UNavigationMenu :items="items" orientation="vertical" class="-mx-2.5"/>
          </template>
    
          <template #right>
            <UColorModeButton />
    
            <UButton
              to="https://www.linkedin.com/in/jose-aristides-amarista-marron-99b018246/"
              target="_blank"
              icon="i-simple-icons-linkedin"
              aria-label="GitHub"
              color="neutral"
              variant="ghost"
            />
          </template>
        </UHeader>
    
        <UMain class="xl:border xl:rounded-4xl xl:border-muted xl:my-2 bg-white dark:bg-default">
          <div>
            <NuxtPage />
          </div>
        </UMain>
    
        <USeparator class="xl:hidden" />
    
        <UFooter
          :ui="{root: 'xl:rounded-full xl:border xl:border-muted xl:mb-2 bg-white dark:bg-default'}"
        >
          <template #left>
            <div>
              <p class="text-sm text-muted">
                Built by José Amarista • © {{ new Date().getFullYear() }}
              </p>
            </div>
          </template>

          <template #default>
            <div>
              <UButton
                :label="email"
                icon="i-lucide-copy"
                class="cursor-pointer"
                aria-label="Copy Email"
                color="neutral"
                variant="ghost"
                @click="copyText"
              />
            </div>
          </template>
    
          <template #right>
            <div>
              <UButton
                to="https://www.linkedin.com/in/jose-aristides-amarista-marron-99b018246/"
                target="_blank"
                icon="i-simple-icons-linkedin"
                aria-label="LinkedIn"
                color="neutral"
                variant="ghost"
              />
            </div>
          </template>
        </UFooter>
      </div>
    </div>
  </UApp>
</template>
