<script setup lang="ts">
import type { NavigationMenuItem } from '@nuxt/ui'
import { useLogo } from '@/composables/useLogo';

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

const title = 'Jaamaristam'
const description = 'Portfolio by jaamaristam@gmail.com. Software Inginner.'

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
  label: 'Home',
  to: '/',
  active: route.path.toString() === '/'
}, {
  label: 'About',
  to: '/about',
  active: route.path.startsWith('/about')
}, {
  label: 'Proyects',
  to: '/proyects',
  active: route.path.startsWith('/proyects')
}])

const { logoUrl } = useLogo();
</script>

<template>
  <UApp>
    <div class="block lg:flex justify-center items-center">
      <div class="lg:max-w-4/5 xl:max-w-3/4">
        <UHeader>
          <template #left>
            <NuxtLink to="/">
              <img :src="logoUrl" class="w-auto h-12 shrink-0" />
            </NuxtLink>
          </template>
    
          <UNavigationMenu :items="items"/>
    
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
    
        <UMain>
          <NuxtPage />
        </UMain>
    
        <USeparator />
    
        <UFooter>
          <template #left>
            <p class="text-sm text-muted">
              Built by José Amarista • © {{ new Date().getFullYear() }}
            </p>
          </template>
    
          <template #right>
            <UButton
              to="https://www.linkedin.com/in/jose-aristides-amarista-marron-99b018246/"
              target="_blank"
              icon="i-simple-icons-linkedin"
              aria-label="GitHub"
              color="neutral"
              variant="ghost"
            />
          </template>
        </UFooter>
      </div>
    </div>
  </UApp>
</template>
