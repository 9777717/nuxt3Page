<script lang="ts" setup>
import { AppConfigInput } from '@nuxt/schema'

export interface IMenuItem {
  type: 'link' | 'button'
  text: string
  href?: any
  route?: any
}

const { t } = useLang()
const app = useAppConfig() as AppConfigInput
const menus = computed((): IMenuItem[] => [
  { type: 'link', text: t('pages.blank.nav'), route: { name: 'blank' } },
  { type: 'link', text: t('pages.test.nav'), route: { name: 'test' } },
  { type: 'link', text: t('pages.setting.nav'), route: { name: 'setting' } },
  // {
  //   type: 'button',
  //   text: t('pages.dashboard.nav'),
  //   route: { name: 'dashboard' },
  // },
])
</script>

<template>
  <BuilderNavbar>
    <template #menu>
      <div class="right_text">
        <div class="textWhats space-x-4 flex items-center">
          <div class="text_whats">
            <img
              src="https://static.cmereye.com/imgs/2023/04/bbd64119a071aecd.png"
              alt="WhatsApp"
            />
            <text class="text-base font-bold md:text-lg">WhatsApp</text>
            <!-- class="hover:no-underline hover:text-slate-900 hover:dark:text-white capitalize" -->
          </div>
          <div class="text_tel">
            <img
              src="https://static.cmereye.com/imgs/2023/04/56577123ca0c1773.png"
              alt="電話查詢"
            />
            <text>{{ t('pages.index.inquire') }}</text>
          </div>
        </div>
        <div class="img">
          <img
            src="https://static.cmereye.com/imgs/2023/04/92e29b10f3a22ee5.png"
          />
        </div>
        <!-- <LanguageSwitcher /> -->
        <!-- <ThemeSwitcher /> -->
      </div>
      <!-- <div class="flex space-x-4 border-l ml-6 pl-6 border-gray-900/10 dark:border-gray-50/[0.2]"> -->
      <!--- 语言翻译  --->
      <!-- <LanguageSwitcher /> -->
      <!--- 主题 --->
      <!-- <ThemeSwitcher /> -->
      <!-- </div> -->
    </template>
  </BuilderNavbar>
</template>

<style lang="scss" scoped>
.right_text {
  color: white;
  display: flex;
  height: 100%;
}

.right_text > div {
  display: flex;
  align-items: stretch;
}
.text_whats {
  font-family: 'Noto Sans CJK TC';
  font-style: normal;
  font-weight: 700;
  font-size: 16.1716px;
  line-height: 24px;
  display: flex;
  align-items: center;
  text-align: center;

  /* 白色 */

  color: #ffffff;
}
.text_whats > img {
  padding-right: 4px;
}

.textWhats > div {
  display: flex;
  align-items: center;
  flex-direction: row;
}
.text_tel > img {
  padding-right: 4px;
}
//
.text_tel {
  width: 150px;
  padding-left: 24px;
  padding-right: 29px;

  background: #ffee54;

  text {
    color: #00a4ce;
    font-family: 'Noto Sans CJK TC';
    font-style: normal;
    font-weight: 700;
    font-size: 16.1716px;
    line-height: 24px;
    display: flex;
    align-items: center;
    text-align: center;
  }
}

.right_text {
  .img {
    padding: 34px 26px 34px 27px;
    img {
      width: 22px;
      height: 18px;
    }
  }
}
</style>

<style lang="scss" scoped>
@media (max-width: 767px) {
  .right_text {
    .textWhats {
      display: none;
    }
    .img {
      padding: 12px 0;
      img {
        width: 22px;
        height: 18px;
      }
    }
  }
}
</style>
