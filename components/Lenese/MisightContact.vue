<script setup lang="ts">
const { t } = useLang()
</script>
<template>
  <div class="MisightContact">
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
              <img
                src="https://static.cmereye.com/imgs/2023/04/ddf7c34280464074.png"
              />
              <div>
                角膜矯形術（Ortho-K，俗稱OK鏡）是一項非手術矯正視力方法，透過配戴特製的高透氧度硬性隱形眼鏡（角膜矯形鏡），以壓力慢慢改變角膜弧度，使角膜中央部分變得平坦，令外界光線重新聚焦到視網膜上，看見清晰的影像。由於角膜富有彈性，弧度改善並不持久，不能將近視徹底根治。一旦停戴，清晰視覺效果將會在數天內消失。因此需長期及定時在晚間戴上角膜矯形鏡（OK鏡），以維持清晰視覺的效果。
              </div>
            </div>
            <div>
              <img
                src="https://static.cmereye.com/imgs/2023/04/3f9eeb7638bff548.png"
              />
            </div>
            <div>
              <div>
                另外，角膜形狀改變後，眼球聚焦事物時，中心影像會被聚焦在視網膜上，周邊影像則會被聚焦在視網膜的較前方，產生「周邊離焦」，有效預防眼軸變長，從而減慢近視及散光加深速度。
              </div>
              <img
                src="https://static.cmereye.com/imgs/2023/04/ed71182adfdc3daf.png"
              />
            </div>
          </div>
        </div>
        <div>服务内容</div>
        <div>角膜畸形术疗程</div>
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
  }
}
</style>
