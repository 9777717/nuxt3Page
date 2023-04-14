<script lang="ts" setup>
import Title from '../Title'
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
  <Title :text_l="'服務'" :text_r="'內容'" />
  <div class="InspectionItem flex flex-col">
    <div class="flex flex-col serve">
      <div class="flex flex-row items-center justify-center">
        <div class="iconLogo">
          <img
            src="https://static.cmereye.com/imgs/2023/04/cc7c0c7aaf50c230.png"
            alt="服務一覽"
          />
        </div>
        <div class="iconText">服務一覽</div>
      </div>
      <div class="eyeBox flex flex-col">
        <div class="flex flex-wrap">
          <div v-for="eyeIcon in arrImage" :key="eyeIcon.img" class="eyeIcon">
            <div class="eyeImg">
              <img :src="eyeIcon.img" :alt="eyeIcon.text" />
            </div>
            <div class="eyeIext" v-html="eyeIcon.text"></div>
          </div>
        </div>
      </div>
    </div>
    <div class="flex flex-nowrap btn">
      <div class="eyeBnt1">
        長者醫療券計劃
        <div class="triangle"></div>
      </div>
      <div class="eyeBnt2">
        服務收費
        <div class="triangle1"></div>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
.InspectionItem {
  position: relative;
  text-align: center;
  background: #ffffff;
  padding: 18px 33px 69px 33px;
}
.serve {
  padding: 0 4.5px;
}

.iconLogo {
  margin-top: 10px;
  margin-right: 37px;
}

.iconText {
  position: relative;
  margin-left: 37px;
  padding: 0 10px;

  font-family: 'Noto Sans';
  font-style: normal;
  font-weight: 700;
  font-size: 40px;
  line-height: 34px;
  display: flex;
  align-items: center;
  text-align: center;
  letter-spacing: 0.1em;
  /* Turquoise */

  color: #00a4ce;
  border-bottom: 9px solid #ffee54;
}
.eyeBox {
  width: 839px;
  margin: 25px 0 69.5px 0;
}
.eyeIcon {
  display: flex;
  width: 156.44px;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  box-sizing: border-box;
  margin: 0px 4.5px 44.2px 4.5px;
}

.eyeImg {
  width: 100px;
  height: 100px;
}
.eyeIext {
  margin-top: 9px;
  height: 65.18px;
  font-family: 'Noto Sans CJK TC';
  font-style: normal;
  font-weight: 700;
  font-size: 20.858px;
  line-height: 31px;
  /* or 150% */

  text-align: center;

  /* Dark Grey */

  color: #3e5270;
}
.btn {
  margin: 33px 190px auto 190px;
}
.eyeBnt1 {
  cursor: pointer;
  height: 49px;
  width: 210px;
  background: #00a4ce;
  border-radius: 29px;
  font-family: 'Noto Sans CJK TC';
  font-style: normal;
  font-weight: 700;
  font-size: 20px;
  line-height: 40px;
  /* identical to box height, or 200% */

  display: flex;
  align-items: center;
  justify-content: space-evenly;
  /* Turquoise */

  color: #ffffff;
  margin-right: 74px;
}
.eyeBnt2 {
  cursor: pointer;
  width: 138px;
  height: 49px;
  background: #ffee54;
  border-radius: 29px;
  font-family: 'Noto Sans CJK TC';
  font-style: normal;
  font-weight: 700;
  font-size: 20px;
  line-height: 40px;
  /* identical to box height, or 200% */

  display: flex;
  align-items: center;
  justify-content: space-evenly;
  /* Turquoise */

  color: #00a4ce;
}
.triangle {
  width: 0;
  height: 0;
  border-left: 10px solid transparent;
  border-right: 10px solid transparent;
  border-bottom: 14px solid #ffffff;
  transform: matrix(0, -1, -1, 0, 0, 0);
}
.triangle1 {
  width: 0;
  height: 0;
  border-left: 10px solid transparent;
  border-right: 10px solid transparent;
  border-bottom: 14px solid #00a4ce;
  transform: matrix(0, -1, -1, 0, 0, 0);
}
</style>
