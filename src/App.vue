<script setup>
import { onBeforeUnmount, onMounted, ref } from 'vue'

const activeImage = ref(null)
const stats = [
  { value: '3+', label: '年开发经验' },
  { value: '8', label: '项目案例' },
  { value: 'H5 / iPad / 小程序 / App', label: '多端适配' },
  { value: 'Vue 3 + Spring Cloud', label: '全栈开发' }
]

const skillGroups = [
  {
    title: '前端框架',
    content: 'Vue 2 / Vue 3、TypeScript、React、React Hooks、Vuex / Pinia'
  },
  {
    title: '可视化能力',
    content: 'Three.js、Canvas、ECharts、复杂大屏与异形屏适配'
  },
  {
    title: '多端开发',
    content: '原生小程序、UniApp、Vant、H5、iPad、App'
  },
  {
    title: '工程与体验',
    content: 'Vite、Webpack、性能优化、i18n、复杂交互与键盘操作'
  },
  {
    title: '后端与数据',
    content: 'Spring Boot、MyBatis Plus、Redis、MySQL、Oracle、PostgreSQL'
  },
  {
    title: '部署与 AI',
    content: 'Docker、Linux、Nginx、LLM API、SSE、Agent、RAG、MCP'
  }
]

const openImage = (src, alt) => {
  activeImage.value = { src, alt }
}

const closeImage = () => {
  activeImage.value = null
}

const handleKeydown = (event) => {
  if (event.key === 'Escape') closeImage()
}

onMounted(() => window.addEventListener('keydown', handleKeydown))
onBeforeUnmount(() => window.removeEventListener('keydown', handleKeydown))

const projects = [
  {
    id: '01',
    title: '城市之窗地标媒体智能操作系统',
    tag: 'V3-大屏',
    summary:
      '面向城市地标媒体的内容投放与播控协作平台，聚焦大屏运营、排期调度与现场展示联动。',
    accent: 'right',
    cover: '/projects/V3-大屏/微信图片_20260817190515.jpg',
    gallery: [
      '/projects/V3-大屏/微信图片_20260817190515.jpg',
      '/projects/V3-大屏/微信图片_20260817190521.jpg',
      '/projects/V3-大屏/微信图片_20260817190535.jpg',
      '/projects/V3-大屏/微信图片_20260817190538.jpg'
    ]
  },
  {
    id: '02',
    title: '城市媒体运营管理平台 V3',
    tag: 'V3',
    summary:
      '覆盖资源管理、内容配置、排期调度和终端联动的运营平台，适合复杂屏媒业务的统一管理。',
    accent: 'left',
    cover: '/projects/V3/微信图片_20260816233257.png',
    gallery: [
      '/projects/V3/微信图片_20260816233257.png',
      '/projects/V3/微信图片_20260816233320.png',
      '/projects/V3/微信图片_20260816233354.png',
      '/projects/V3/微信图片_20260816233405.png',
      '/projects/V3/微信图片_20260816233439.png',
      '/projects/V3/微信图片_20260816233454.png',
      '/projects/V3/微信图片_20260816233514.png',
      '/projects/V3/微信图片_20260816233533.png',
      '/projects/V3/微信图片_20260816233625.png'
    ]
  },
  {
    id: '03',
    title: '花旗3D空间展示系统',
    tag: '花旗',
    summary:
      '沉浸式空间浏览与服务信息展示系统，预览播放效果。',
    accent: 'right',
    cover: '/projects/花旗/微信图片_20260814184322.png',
    gallery: [
      '/projects/花旗/微信图片_20260814184322.png',
      '/projects/花旗/微信图片_20260814184415.png',
      '/projects/花旗/微信图片_20260814184444.png',
      '/projects/花旗/微信图片_20260814184632.png'
    ]
  },
  {
    id: '04',
    title: '高端餐饮空间浏览系统',
    tag: 'hello!上海',
    summary:
      '围绕城市节庆活动打造的视觉专题页，适合品牌宣传、节日活动联动与多内容入口整合。',
    accent: 'left',
    cover: '/projects/hello!上海/微信图片_20260814184542.png',
    gallery: [
      '/projects/hello!上海/微信图片_20260814184542.png',
      '/projects/hello!上海/微信图片_20260814184555.png'
    ]
  },
  {
    id: '05',
    title: '监控中心可视化联动平台',
    tag: '监控中心',
    summary:
      '整合监控画面、状态面板与现场联动能力，适合运营监看、状态巡检和应急指挥场景。',
    accent: 'right',
    cover: '/projects/监控中心/微信图片_20260814183136.png',
    gallery: [
      '/projects/监控中心/微信图片_20260814183136.png',
      '/projects/监控中心/微信图片_20260814183152.png',
      '/projects/监控中心/微信图片_20260814183305.png',
      '/projects/监控中心/微信图片_20260814183347.png',
      '/projects/监控中心/微信图片_20260814183400.png',
      '/projects/监控中心/微信图片_20260814183427.png',
      '/projects/监控中心/微信图片_20260901162537.jpg'
    ]
  },
  {
    id: '06',
    title: '多端展示与内容播发界面',
    tag: '展示',
    summary:
      '用于现场展示和终端播发的界面方案，强调内容直达、视觉统一和终端操作便捷性。',
    accent: 'left',
    cover: '/projects/展示/微信图片_20260814184911.png',
    gallery: [
      '/projects/展示/微信图片_20260814184911.png',
      '/projects/展示/微信图片_20260814184932.png'
    ]
  },
  {
    id: '07',
    title: '业务报价与方案配置系统',
    tag: '报价单',
    summary:
      '面向方案整理与价格配置的业务页面，便于快速组合内容项并输出清晰的交付结构。',
    accent: 'right',
    cover: '/projects/报价单/微信图片_20260814184717.png',
    gallery: [
      '/projects/报价单/微信图片_20260814184717.png',
      '/projects/报价单/微信图片_20260814184747.png',
      '/projects/报价单/微信图片_20260814184802.png',
      '/projects/报价单/微信图片_20260814184815.png'
    ]
  },
  {
    id: '08',
    title: '城市之窗客户服务小程序',
    tag: '小程序',
    summary:
      '面向城市地标媒体客户的移动服务平台，集项目进度、上屏节目验收、播出排期与拍摄交付于一体，便于随时查看项目状态与展示效果。',
    accent: 'left',
    portrait: true,
    cover: '/projects/小程序/微信图片_20260907120920.jpg',
    gallery: [
      '/projects/小程序/微信图片_20260907120920.jpg',
      '/projects/小程序/微信图片_20260907120818.jpg',
      '/projects/小程序/微信图片_20260907120836.jpg',
      '/projects/小程序/微信图片_20260907120841.jpg',
      '/projects/小程序/微信图片_20260907120847.jpg',
      '/projects/小程序/微信图片_20260907120852.jpg',
      '/projects/小程序/微信图片_20260907120856.jpg',
      '/projects/小程序/微信图片_20260907120900.jpg',
      '/projects/小程序/微信图片_20260907120903.jpg'
    ]
  }
]

</script>

<template>
  <div class="page-shell">
    <header class="topbar">
      <div class="brand">作品集</div>
      <nav class="nav">
        <a href="#home">首页</a>
        <a href="#projects">项目展示</a>
        <a href="#stack">技术栈</a>
        <a href="#about">关于我</a>
        <a href="#contact">联系我</a>
      </nav>
    </header>

    <main>
      <section id="home" class="hero section">
        <div class="hero-copy">
          <p class="eyebrow">你好，我是骆树仁</p>
          <h1>专注于城市媒体与数据可视化系统开发</h1>
          <p class="hero-text">
            以 Vue 3 为核心，覆盖城市大屏、运营后台、专题展示与多终端适配，
            将复杂业务整理成稳定、清晰且可持续维护的产品体验。
          </p>

          <div class="stats">
            <div v-for="item in stats" :key="item.label" class="stat">
              <strong>{{ item.value }}</strong>
              <span>{{ item.label }}</span>
            </div>
          </div>

        </div>

        <div class="hero-visual" aria-hidden="true">
          <div class="skyline-card">
            <img class="skyline-image" src="/shanghai-skyline.png" alt="" fetchpriority="high" />
          </div>
        </div>
      </section>

      <section id="projects" class="projects section">
        <div class="section-heading">
          <h2>项目展示</h2>
        </div>

        <article
          v-for="project in projects"
          :key="project.id"
          class="project-card"
          :class="[`accent-${project.accent}`, { 'project-portrait': project.portrait }]"
        >
          <div class="project-copy">
            <p class="project-id">{{ project.id }}</p>
            <h3>{{ project.title }}</h3>
            <span class="project-tag">{{ project.tag }}</span>
            <p class="project-summary">{{ project.summary }}</p>
          </div>

          <div class="project-media">
            <button
              class="image-button project-cover-button"
              type="button"
              :aria-label="`放大查看 ${project.title}`"
              @click="openImage(project.cover, project.title)"
            >
              <img
                v-if="project.portrait"
                class="portrait-backdrop"
                :src="project.cover"
                alt=""
                aria-hidden="true"
              />
              <img class="project-cover" :src="project.cover" :alt="project.title" />
              <span class="image-hint">点击放大</span>
            </button>
            <div class="project-gallery">
              <button
                v-for="image in project.gallery.slice(1)"
                :key="image"
                class="image-button gallery-image-button"
                type="button"
                :aria-label="`放大查看 ${project.title} 截图`"
                @click="openImage(image, `${project.title} 截图`)"
              >
                <img
                  v-if="project.portrait"
                  class="portrait-backdrop"
                  :src="image"
                  alt=""
                  aria-hidden="true"
                />
                <img
                :src="image"
                :alt="`${project.title} 截图`"
                />
                <span class="image-hint">点击放大</span>
              </button>
            </div>
          </div>
        </article>
      </section>

      <section id="stack" class="stack section">
        <div class="section-heading left">
          <h2>技术栈</h2>
          <p>覆盖复杂业务、大屏可视化、多端开发、工程化与基础全栈协作能力。</p>
        </div>
        <div class="stack-grid">
          <article v-for="skill in skillGroups" :key="skill.title" class="skill-card">
            <h3>{{ skill.title }}</h3>
            <p>{{ skill.content }}</p>
          </article>
        </div>
      </section>
    </main>

    <footer id="contact" class="footer">
      <div>
        <p class="footer-label">邮箱</p>
        <p>stundast@gmail.com</p>
      </div>
      <div>
        <p class="footer-label">电话</p>
        <p>+86 17824929582</p>
      </div>
      <div id="about">
        <p class="footer-label">定位</p>
        <p>中国 · 上海</p>
      </div>
      <div class="footer-copy">© 2026 作品集，保留所有权利。</div>
    </footer>

    <Teleport to="body">
      <div
        v-if="activeImage"
        class="image-modal"
        role="dialog"
        aria-modal="true"
        :aria-label="activeImage.alt"
        @click.self="closeImage"
      >
        <button class="modal-close" type="button" aria-label="关闭图片预览" @click="closeImage">
          关闭
        </button>
        <img :src="activeImage.src" :alt="activeImage.alt" />
      </div>
    </Teleport>
  </div>
</template>
