<script setup lang="ts">
import { Html } from '~~/.nuxt/components'

const { t } = useLang()
const leneseServe = [
  {
    img: 'https://static.cmereye.com/imgs/2023/04/c408bd080f987af5.png',
    text: t('components.lenese.eye_examination'),
    id: 1,
  },
  {
    img: 'https://static.cmereye.com/imgs/2023/04/a5071d2e7ac66690.png',
    text: t('components.lenese.eye_suitability'),
    id: 2,
  },
  {
    img: 'https://static.cmereye.com/imgs/2023/04/92fe9f61d9dc577f.png',
    text: t('components.lenese.eye_teaching'),
    id: 3,
  },
  {
    img: 'https://static.cmereye.com/imgs/2023/04/fd21acfcea3f880c.png',
    text: t('components.lenese.eye_customized'),
    id: 4,
  },
  {
    img: 'https://static.cmereye.com/imgs/2023/04/9f809e92cc0a72eb.png',
    text: t('components.lenese.eye_necessary'),
    id: 5,
  },
  {
    img: 'https://static.cmereye.com/imgs/2023/04/51674a0ee668a28e.png',
    text: t('components.lenese.eye_products'),
    id: 6,
  },
]
const courseOftreatment = [
  {
    img: 'https://static.cmereye.com/imgs/2023/04/c408bd080f987af5.png',
    text: '綜合眼睛檢查<br />+ 鏡片試配<br />+ 鏡片訂製',
  },
  {
    img: 'https://static.cmereye.com/imgs/2023/04/92fe9f61d9dc577f.png',
    text: '學習戴上、摘下和護理隱形眼鏡的方法',
  },
  {
    img: 'https://static.cmereye.com/imgs/2023/04/87c78c54f6ab1ee5.png',
    text: '取鏡片並在<br />當晚開始使用',
  },
  {
    img: 'https://static.cmereye.com/imgs/2023/04/9f809e92cc0a72eb.png',
    text: '按時覆診',
  },
  {
    img: 'https://static.cmereye.com/imgs/2023/04/fd21acfcea3f880c.png',
    text: '需更換全新鏡片',
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
        <!-- 设计原理 -->
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
        <!-- 服务内容 -->
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
        <!-- 角膜畸形术疗程 -->
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
              <div v-for="ortArr in courseOftreatment" :key="ortArr.img">
                <div><img :src="ortArr.img" alt="" /></div>
                <div v-html="ortArr.text"></div>
              </div>
            </div>
          </div>
        </div>
        <!-- 達致效果 -->
        <div>
          <div>
            <PageTitle :text_l="'達致'" :text_r="'效果'" />
          </div>
          <div>
            <div>
              <div>
                <img
                  src="https://static.cmereye.com/imgs/2023/04/f557602124a10cbb.png"
                  alt=""
                />
              </div>
              <div>
                <div>
                  <div>✓短暫減低近視及散光</div>
                  <div>日間不需配戴近視眼鏡或隱形眼鏡。</div>
                </div>
                <div>
                  <div>✓控制近視及散光加深速度</div>
                  <div>
                    根據本地大學的研究結果顯示，配戴角膜矯形鏡片（OK鏡）的兒童眼軸增長幅度是沒有配戴的兒童的四至六成；近視加深速度亦比配戴普通眼鏡的兒童平均減慢一倍。
                  </div>
                </div>
              </div>
            </div>
            <div>
              <div>
                <div>優點</div>
                <div>
                  <p>日間摘除鏡片後便能整天保持良好視力</p>
                  <p>近視加深速度減慢一倍</p>
                  <p>使用後約一星期已有顯著效果</p>
                  <p>避免日間配戴隱形眼鏡引起的問題，例如眼乾</p>
                  <p>可隨時停止療程，角膜亦會在數周後回復原狀</p>
                </div>
              </div>
              <div>
                <div>達致效果</div>
                <div>
                  <p>6歲或以上</p>
                  <p>近視度數少於500</p>
                  <p>散光度數少於100</p>
                  <p>近視持續加深者</p>
                  <p>不喜歡戴眼鏡人士</p>
                  <p>熱愛運動人士</p>
                </div>
              </div>
            </div>
          </div>
        </div>
        <!-- 真實案例分享 -->
        <div>
          <div class="iconHeader">
            <div>
              <span>真實案例</span>
            </div>
            <div>分享</div>
          </div>
          <div></div>
        </div>
        <!-- 配戴時間及方法 -->
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

    // 以下是是设计原理的样式布局
    & > div:nth-child(1) > div:nth-child(1) {
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

    // 角膜畸形术疗程
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

      // 疗程流程→
      & > div:nth-child(2) {
        background: #fff;
        margin-bottom: 87px;
        border-radius: 5px;
        box-shadow: 4px 4px 4px rgba(0, 0, 0, 0.1);

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

        & > div:nth-child(2) {
          display: flex;
          flex-direction: row;
          padding: 27px 12px 24px 30px;

          & > div {
            width: 152px;
            margin: auto;
            display: flex;
            flex-direction: column;
            align-items: center;

            & > div:nth-child(1) {
              width: 100px;
              height: 100px;

              & > img {
                width: 100%;
                height: 100%;
              }
            }

            & > div:nth-child(2) {
              margin-top: 14px;
              font-family: 'Noto Sans CJK TC';
              font-style: normal;
              font-weight: 700;
              font-size: 20.858px;
              line-height: 31px;
              /* or 150% */

              text-align: center;

              /* Dark Grey */

              color: #3e5270;
              height: 96px;
            }
          }

          & > div:nth-child(3) {
            & > div:nth-child(1) {
              padding: 17px;
            }
          }

          & > div:nth-child(1) {
            & > div:nth-child(2) {
              width: 127px;
            }
          }
        }
      }
    }

    & > div:nth-child(1) > div:nth-child(4) {
      & > div:nth-child(2) {
        background: #fff;
        padding: 54px 77px 49px 76px;
        margin-bottom: 87px;
        border-radius: 5px;
        box-shadow: 4px 4px 4px rgba(0, 0, 0, 0.1);

        & > div:nth-child(1) {
          display: flex;

          & > div:nth-child(1) {
            width: 308px;
            height: 308px;
            margin-right: 55px;

            & > img {
              width: 100%;
            }
          }

          & > div:nth-child(2) {
            width: 368px;
            font-family: 'Noto Sans CJK TC';
            font-style: normal;
            font-weight: 500;
            font-size: 16px;
            line-height: 32px;
            text-align: justify;
            letter-spacing: 0.1em;

            /* Dark Grey */

            color: #3e5270;

            & > div:nth-child(1) {
              margin-bottom: 77px;
            }

            & > div > div:nth-child(1) {
              font-size: 24px;
              line-height: 36px;
              font-weight: 700;
            }
          }
        }

        & > div:nth-child(2) {
          margin-top: 51px;
          display: flex;
          flex-direction: row;
          justify-content: space-between;

          & > div {
            display: flex;
            flex-direction: row;

            & > div:nth-child(1) {
              background: #00a4ce;
              font-family: 'Noto Sans CJK TC';
              font-style: normal;
              font-weight: 700;
              font-size: 16px;
              line-height: 24px;
              /* identical to box height, or 150% */

              display: flex;
              align-items: center;

              /* 白色 */

              color: #ffffff;
            }
          }

          & > div:nth-child(1) {
            & > div:nth-child(1) {
              width: 45px;
              height: 33px;
              padding: 6px;
              margin-right: 7px;
            }

            & > div:nth-child(2) {
              width: 348px;
              color: #3e5270;

              & > p::before {
                content: '';
                display: inline-block;
                width: 5px;
                height: 5px;
                background-color: #3e5270;
                border-radius: 100%;
                margin: 3px 10px;
              }

              & > p {
                font-family: 'Noto Sans CJK TC';
                font-style: normal;
                font-weight: 700;
                font-size: 16px;
                line-height: 24px;
                color: #3e5270;
              }
            }
          }

          & > div:nth-child(2) {
            & > div:nth-child(1) {
              width: 78px;
              height: 33px;
              padding: 6px;
              margin-right: 7px;
            }

            & > div:nth-child(2) {
              width: 153px;
              color: #3e5270;

              & > p::before {
                content: '';
                display: inline-block;
                width: 5px;
                height: 5px;
                background-color: #3e5270;
                border-radius: 100%;
                margin: 3px 10px;
              }

              & > p {
                font-family: 'Noto Sans CJK TC';
                font-style: normal;
                font-weight: 700;
                font-size: 16px;
                line-height: 24px;
                color: #3e5270;
              }
            }
          }
        }
      }
    }

    & > div:nth-child(1) > div:nth-child(5) {
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
        width: 178px;
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
        margin-bottom: 87px;
        border-radius: 5px;
        box-shadow: 4px 4px 4px rgba(0, 0, 0, 0.1);
      }
    }
  }
}
</style>
