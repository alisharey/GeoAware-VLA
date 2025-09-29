
<script setup lang="ts">
const logo = '/favicon.svg'
const title = "GeoAware‑VLA: Implicit Geometry Aware Vision‑Language‑Action Model"
const title_color = '#0b1220'
const title_supp = 'Project Page'
const title_supp_color = '#2b59ff'
const btn_color = '#2b59ff'

const authors = [{"name": "Ali Abouzeid", "homepage": "", "icon": "", "address_flag": ""}, {"name": "Malak Mansour", "homepage": "", "icon": "", "address_flag": ""}, {"name": "Zezhou Sun", "homepage": "", "icon": "", "address_flag": ""}, {"name": "Dezhen Song", "homepage": "", "icon": "", "address_flag": ""}]

const addresses = [
  // Example: { address_flag: '🇺🇸', name: 'Texas A&M University', icon: '', homepage: 'https://www.tamu.edu/' }
]

const emphases = [
  "Geometry-aware visual backbone improves viewpoint robustness",
  "Lightweight projection adapts features to policy decoder",
  "Stronger zero-shot generalization to unseen camera poses"
]

const buttons = [
  { disabled: false, name: 'Paper (arXiv)', component: () => window.open('https://arxiv.org/abs/2509.14117', '_blank') },
  { disabled: false, name: 'PDF', component: () => window.open('https://arxiv.org/pdf/2509.14117', '_blank') },
  { disabled: false, name: 'Code (GitHub)', component: () => window.open('https://github.com/your-username/geoaware-vla', '_blank') },
  // { disabled: false, name: 'Video', component: () => window.open('', '_blank') },
]
</script>

<template>
  <section class="hero">
    <div class="container">
      <div class="grid two" style="align-items:center;">
        <div>
          <img :src="logo" alt="logo" style="width:64px;height:64px;border-radius:12px;border:1px solid var(--border);" />
          <h1 class="title" :style="{ color: title_color }">{{ title }}</h1>
          <p class="subtitle" :style="{ color: title_supp_color }">{{ title_supp }}</p>
          <div style="display:flex;flex-wrap:wrap;gap:8px;margin:12px 0 6px;">
            <template v-for="a in authors" :key="a.name">
              <a v-if="a.homepage" class="chip" :href="a.homepage" target="_blank" rel="noreferrer">{{ a.name }}</a>
              <span v-else class="chip">{{ a.name }}</span>
            </template>
          </div>
          <div style="display:flex;flex-wrap:wrap;gap:10px;margin:14px 0 0;">
            <a v-for="b in buttons" :key="b.name" class="btn" href="#" @click.prevent="b.component()">{{ b.name }}</a>
          </div>
        </div>
        <div>
          <img src="/og.png" alt="teaser" style="width:100%;border-radius:16px;border:1px solid var(--border);" />
        </div>
      </div>
      <div class="card" style="margin-top:18px;">
        <ul class="grid auto" style="margin:0;padding:0;list-style:disc;padding-left:20px;">
          <li v-for="e in emphases" :key="e">{{ e }}</li>
        </ul>
      </div>
    </div>
  </section>
</template>

<style scoped>
.chip { background: var(--muted); border: 1px solid var(--border); padding: 6px 10px; border-radius: 999px; }
</style>
