<script setup lang="ts">
import { Html } from '~~/.nuxt/components'

const { t } = useLang()
const leneseServe = [
  {
    img: 'https://static.cmereye.com/imgs/2023/04/92fe9f61d9dc577f.png',
    text: t('components.lenese.eye_examination'),
    id: 1,
  },
  {
    img: 'https://static.cmereye.com/imgs/2023/04/c408bd080f987af5.png',
    text: t('components.lenese.eye_suitability'),
    id: 2,
  },
  {
    img: 'https://static.cmereye.com/imgs/2023/04/a5071d2e7ac66690.png',
    text: t('components.lenese.eye_teaching'),
    id: 3,
  },
  {
    img: 'https://static.cmereye.com/imgs/2023/04/9f809e92cc0a72eb.png',
    text: t('components.lenese.eye_customized'),
    id: 4,
  },
  {
    img: 'https://static.cmereye.com/imgs/2023/04/fd21acfcea3f880c.png',
    text: t('components.lenese.eye_necessary'),
    id: 5,
  },
  {
    img: 'https://static.cmereye.com/imgs/2023/04/51674a0ee668a28e.png',
    text: t('components.lenese.eye_products'),
    id: 6,
  },
]
</script>
<template>
  <div class="OrthoKContact">
    <div class="miCoypright">
      <div></div>
      <div>
        <img
          src="https://static.cmereye.com/imgs/2023/04/b5f32d00179371e8.png"
        />
      </div>
      <div>
        <p>硬性隱形眼鏡</p>
        <p>Ortho-K</p>
      </div>
    </div>
    <!-- <PageRhomboidTop
      :style-rhom="{
        top: '650px',
        height: '342px',
        transform: 'skewY(348deg)',
        background: '#fff',
      }"
    /> -->
    <div class="navLenese">
      <div>
        <div>
          <div>
            <PageTitle
              :text_l="t('components.lenese.design')"
              :text_r="t('components.lenese.theory')"
            />
          </div>
          <div>
            <div>
              <div>
                <img
                  src="https://static.cmereye.com/imgs/2023/04/ddf7c34280464074.png"
                />
              </div>
              <div>
                {{ t('components.lenese.detail') }}
              </div>
            </div>
            <div>
              <img
                src="https://static.cmereye.com/imgs/2023/04/3f9eeb7638bff548.png"
              />
            </div>
            <div>
              <div>{{ t('components.lenese.detail_img_int') }}</div>
              <div>
                <img
                  src="https://static.cmereye.com/imgs/2023/04/ed71182adfdc3daf.png"
                />
              </div>
            </div>
          </div>
        </div>

        <div>
          <div>
            <PageTitle
              :text_l="t('components.lenese.serve_lenese')"
              :text_r="t('components.lenese.matter_lenese')"
            />
          </div>
          <div>
            <div>
              <div v-for="arr in leneseServe" :key="arr.id">
                <img :src="arr.img" />
                <div>{{ arr.text }}</div>
              </div>
            </div>
            <div>
              *本中心的角膜矯形鏡驗配服務已包括
              <div>1次綜合眼睛檢查及1年內覆診之費用。</div>
            </div>
          </div>
        </div>
        <div>
          <div class="iconHeader">
            <div>
              <span>角膜畸形术</span>
            </div>
            <div>疗程</div>
          </div>
          <div>
            <div>
              <div>1-4星期</div>
              <div>取鏡</div>
              <div>配戴後第1/7/ 14/30/90/180日</div>
              <div>一年後</div>
            </div>
            <div>
              <div>
                <div>
                  <img
                    src="https://static.cmereye.com/imgs/2023/04/92fe9f61d9dc577f.png"
                    alt=""
                  />
                </div>
                <div>綜合眼睛檢查 + 鏡片試配 + 鏡片訂製</div>
              </div>
              <div>
                <div>
                  <img
                    src="https://static.cmereye.com/imgs/2023/04/92fe9f61d9dc577f.png"
                    alt=""
                  />
                </div>
                <div>綜合眼睛檢查 + 鏡片試配 + 鏡片訂製</div>
              </div>
              <div>
                <div>
                  <img
                    src="https://static.cmereye.com/imgs/2023/04/92fe9f61d9dc577f.png"
                    alt=""
                  />
                </div>
                <div>綜合眼睛檢查 + 鏡片試配 + 鏡片訂製</div>
              </div>
              <div>
                <div>
                  <img
                    src="https://static.cmereye.com/imgs/2023/04/92fe9f61d9dc577f.png"
                    alt=""
                  />
                </div>
                <div>綜合眼睛檢查 + 鏡片試配 + 鏡片訂製</div>
              </div>
              <div>
                <div>
                  <img
                    src="https://static.cmereye.com/imgs/2023/04/92fe9f61d9dc577f.png"
                    alt=""
                  />
                </div>
                <div>綜合眼睛檢查 + 鏡片試配 + 鏡片訂製</div>
              </div>
            </div>
          </div>
        </div>
        <div>達致效果</div>
        <div>真實案例分享</div>
        <div>配戴時間及方法</div>
      </div>
      <div></div>
    </div>
  </div>
</template>

<style scoped lang="scss">
@media (min-width: 768px) {
  .OrthoKContact {
    position: relative;
  }

  .miCoypright {
    position: relative;

    & > div:nth-child(3) {
      position: absolute;
      top: 244px;
      left: 190px;

      font-family: 'Noto Sans CJK TC';
      font-style: normal;
      font-weight: 700;
      font-size: 120px;
      line-height: 116%;
      /* or 139px */

      display: flex;
      align-items: flex-start;
      flex-direction: column;
      letter-spacing: 0.1em;

      /* Turquoise */

      color: #00a4ce;
    }
  }

  .navLenese {
    width: 884px;
    margin: 0 auto;
    position: relative;

    & > div:nth-child(1) > div:nth-child(1) {
      // 以下是是设计原理的样式布局
      & > :nth-child(2) {
        background: #fff;
        padding: 37px 31px;
        box-shadow: 4px 4px 4px rgba(0, 0, 0, 0.1);
        border-radius: 5px;

        & > div:nth-child(1) {
          display: flex;

          & > div:nth-child(1) {
            width: 436px;
            height: 436px;

            & > img {
              width: 100%;
            }
          }

          & > div:nth-child(2) {
            width: 345px;
            padding-left: 72px;

            font-family: 'Noto Sans CJK TC';
            font-style: normal;
            font-weight: 500;
            font-size: 16px;
            line-height: 32px;
            /* or 200% */

            text-align: justify;

            /* Dark Grey */

            color: #3e5270;
          }
        }

        & > div:nth-child(2) {
          padding-top: 26px;
          padding-bottom: 47px;
        }

        & > div:nth-child(3) {
          display: flex;

          & > div:nth-child(1) {
            width: 440px;
            padding-top: 4px;
            padding-right: 32px;
            padding-left: 29px;

            font-family: 'Noto Sans CJK TC';
            font-style: normal;
            font-weight: 500;
            font-size: 16px;
            line-height: 32px;
            /* or 200% */

            text-align: justify;

            /* Dark Grey */

            color: #3e5270;
          }

          & > div:nth-child(2) {
            width: 331px;
            height: 271px;

            & > img {
              width: 100%;
            }
          }
        }
      }
    }

    //  以下是服务内容样式布局
    & > div:nth-child(1) > div:nth-child(2) {
      & > div:nth-child(2) {
        background: #fff;
        padding: 30px;
        margin-bottom: 87px;
        box-shadow: 4px 4px 4px rgba(0, 0, 0, 0.1);
        border-radius: 5px;

        & > div:nth-child(1) {
          display: flex;
          flex-wrap: wrap;
          justify-content: center;

          & > div {
            width: 176px;
            margin: 28px 17px;
            display: flex;
            flex-direction: column;
            align-items: center;

            & > div:nth-child(2) {
              font-family: 'Noto Sans CJK TC';
              font-style: normal;
              font-weight: 700;
              font-size: 20.858px;
              line-height: 31px;
              text-align: center;

              color: #3e5270;
            }
          }
        }

        & > div:nth-child(2) {
          display: flex;
          justify-content: center;
          font-family: 'Noto Sans CJK TC';
          font-style: normal;
          font-weight: 500;
          font-size: 16px;
          line-height: 32px;
          /* or 200% */

          text-align: center;
          color: #3e5270;

          & > div {
            color: #00a4ce;
          }
        }
      }
    }

    & > div:nth-child(1) > div:nth-child(3) {
      .iconHeader {
        margin: 83px auto 43px auto;
        /* PC-Title */

        font-family: 'Noto Sans';
        font-style: normal;
        font-weight: 700;
        font-size: 40px;
        line-height: 54px;
        display: flex;
        align-items: center;
        justify-content: center;
        text-align: center;
        letter-spacing: 0.1em;

        /* 白色 */

        color: #3e5270;
      }

      .iconHeader > div:nth-child(1) {
        position: relative;
        width: 224px;
        height: 48px;
        background: #00a4ce;
        box-sizing: border-box;
        margin-top: 5px;
      }

      .iconHeader > div:nth-child(1) > span {
        color: #ffffff;
        position: absolute;
        left: 2px;
        bottom: 0px;
      }

      & > div:nth-child(2) {
        background: #fff;

        & > div:nth-child(1) {
          height: 99px;
          display: flex;
          background: #fff8b9;

          font-family: 'Noto Sans CJK TC';
          font-style: normal;
          font-weight: 700;
          font-size: 24px;
          line-height: 36px;
          letter-spacing: 0.1em;
          text-align: center;

          color: #00a4ce;

          & > div {
            flex: 1;
            display: flex;
            justify-content: center;
            align-items: center;
          }

          & > div:nth-child(1) {
            flex: 2;
          }

          & > div:nth-child(2) {
            background: #ffee54;
          }

          & > div:nth-child(3) {
            background: #6ebcd2;
            font-size: 21px;
            line-height: 30px;
            color: #ffffff;
            letter-spacing: 0;
          }

          & > div:nth-child(4) {
            background: #00a4ce;
            color: #fff;
          }
        }
      }
    }
  }
}
</style>
