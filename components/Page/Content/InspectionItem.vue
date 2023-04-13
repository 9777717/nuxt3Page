<script lang="ts" setup>
const { t } = useLang()
const arrImage = [
  {
    img: 'https://static.cmereye.com/imgs/2023/04/71b19643e3209ba5.png',
    text: t('pages.content.eyeIcon.eyeIcon1'),
  },
  {
    img: 'https://static.cmereye.com/imgs/2023/04/d329cb6cd08f49d4.png',
    text: t('pages.content.eyeIcon.eyeIcon2'),
  },
  {
    img: 'https://static.cmereye.com/imgs/2023/04/278a5de117f37ad5.png',
    text: t('pages.content.eyeIcon.eyeIcon3'),
  },
  {
    img: 'https://static.cmereye.com/imgs/2023/04/cfe8014055ea02da.png',
    text: t('pages.content.eyeIcon.eyeIcon4'),
  },
  {
    img: 'https://static.cmereye.com/imgs/2023/04/09408dbefdf1a8e6.png',
    text: t('pages.content.eyeIcon.eyeIcon5'),
  },
  {
    img: 'https://static.cmereye.com/imgs/2023/04/9f7172126a9be8e3.png',
    text: t('pages.content.eyeIcon.eyeIcon6'),
  },
  {
    img: 'https://static.cmereye.com/imgs/2023/04/33b7b64df01a7d84.png',
    text: t('pages.content.eyeIcon.eyeIcon7'),
  },
  {
    img: 'https://static.cmereye.com/imgs/2023/04/a405e259c1065863.png',
    text: t('pages.content.eyeIcon.eyeIcon8'),
  },
  {
    img: 'https://static.cmereye.com/imgs/2023/04/e99f917128ce1c6b.png',
    text: t('pages.content.eyeIcon.eyeIcon9'),
  },
  {
    img: 'https://static.cmereye.com/imgs/2023/04/35b9db375c594820.png',
    text: t('pages.content.eyeIcon.eyeIcon10'),
  },
  {
    img: 'https://static.cmereye.com/imgs/2023/04/5bf0d34bd7c13a9b.png',
    text: t('pages.content.eyeIcon.eyeIcon11'),
  },
  {
    img: 'https://static.cmereye.com/imgs/2023/04/d372622bf5eeeb97.png',
    text: t('pages.content.eyeIcon.eyeIcon12'),
  },
  {
    img: 'https://static.cmereye.com/imgs/2023/04/a22ce7e89c6bdf02.png',
    text: t('pages.content.eyeIcon.eyeIcon13'),
  },
  {
    img: 'https://static.cmereye.com/imgs/2023/04/a2a5118cac7cfa1f.png',
    text: t('pages.content.eyeIcon.eyeIcon14'),
  },
  {
    img: 'https://static.cmereye.com/imgs/2023/04/b1045c9cf8593872.png',
    text: t('pages.content.eyeIcon.eyeIcon15'),
  },
  {
    img: 'https://static.cmereye.com/imgs/2023/04/83b3e0b57c7d0df6.png',
    text: t('pages.content.eyeIcon.eyeIcon16'),
  },
  {
    img: 'https://static.cmereye.com/imgs/2023/04/3c9ed8915d4f300b.png',
    text: t('pages.content.eyeIcon.eyeIcon17'),
  },
  {
    img: 'https://static.cmereye.com/imgs/2023/04/b0206c64258f646a.png',
    text: t('pages.content.eyeIcon.eyeIcon18'),
  },
  {
    img: 'https://static.cmereye.com/imgs/2023/04/1aa3b128f172141c.png',
    text: t('pages.content.eyeIcon.eyeIcon19'),
  },
]
</script>
<template>
  <div class="InspectionItem">
    <div>服務內容</div>
    <div>
      <div>
        <div>
          <img
            src="https://static.cmereye.com/imgs/2023/04/cc7c0c7aaf50c230.png"
            alt="服務一覽"
          />
        </div>
        <div>服務一覽</div>
      </div>
      <div>
        <div>
          <div v-for="eyeIcon in arrImage" :key="eyeIcon.img">
            <img :src="eyeIcon.img" :alt="eyeIcon.text" />
            <div>
              {{ eyeIcon.text }}
            </div>
          </div>
        </div>
        <div>
          <el-button>長者醫療券計劃</el-button>
          <el-button>服務收費</el-button>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss"></style>
