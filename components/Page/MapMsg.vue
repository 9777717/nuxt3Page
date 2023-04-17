<script lang="ts" setup>
const { t } = useLang()
</script>
<template>
  <div class="map h-180">
    <div
      class="map_header flex flex-row flex-nowrap justify-center items-center h-20"
    >
      <Anchor class="map_font mx-8">{{ t('footer.map.mapIsLand') }}</Anchor>
      <span>|</span>
      <Anchor class="map_font mx-8">{{ t('footer.map.Kowloon') }}</Anchor>
      <span>|</span>
      <Anchor class="map_font mx-8">{{ t('footer.map.Territories') }}</Anchor>
    </div>
    <div class="m-6">
      <div class="flex flex-row justify-center">
        <Anchor class="map_footer">{{ t('footer.map.YalanMong') }}</Anchor>
        <span>|</span>
        <Anchor class="map_footer">{{ t('footer.map.MongKok') }}</Anchor>
      </div>
      <div
        class="rectangle container mx-auto flex flex-nowrap box-border justify-between pr-7 pb-10.5 pl-8 pt-13"
      >
        <div>
          <div class="title-font pb-2">旺角雅蘭</div>
          <div class="font-h5 pb-5">希瑪眼科視光中心</div>
          <div class="flex items-center pb-5">
            <svg
              width="24"
              height="21"
              viewBox="0 0 24 21"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M22.3043 11.7961C23.0016 11.7961 23.6168 11.2219 23.6168 10.4795C23.6578 10.1104 23.4937 9.78223 23.1656 9.49512L21 7.58789V2.625C21 1.89902 20.4135 1.3125 19.6875 1.3125H18.375C17.649 1.3125 17.0625 1.89902 17.0625 2.625V4.13027L12.6943 0.287109C12.4482 0.0820312 12.1201 0 11.833 0C11.5459 0 11.2178 0.0410156 10.9307 0.328125L0.410156 9.49512C0.123047 9.78223 0 10.1104 0 10.4795C0 11.2178 0.574219 11.7961 1.3125 11.7961H2.625V14.6549C2.6209 14.6918 2.6209 14.7287 2.6209 14.7697V19.3594C2.6209 20.2658 3.35508 21 4.26152 21H4.91777C4.96699 21 5.01621 20.9959 5.06543 20.9918C5.12695 20.9959 5.18848 21 5.25 21H7.54688C8.45332 21 9.1875 20.2658 9.1875 19.3594V15.75C9.1875 15.024 9.77402 14.4375 10.5 14.4375H13.125C13.851 14.4375 14.4375 15.024 14.4375 15.75V19.3594C14.4375 20.2658 15.1717 21 16.0781 21H18.3955C18.4529 21 18.5104 21 18.5678 20.9959C18.6129 21 18.658 21 18.7031 21H19.3594C20.2658 21 21 20.2658 21 19.3594V18.6949C21.0123 18.5883 21.0205 18.4775 21.0205 18.3627L20.9918 11.792H22.3043V11.7961Z"
                fill="#3E5270"
              />
            </svg>
            <div class="mapFont pl-2.5">彌敦道625及639號雅蘭中心一期1202室</div>
          </div>
          <div class="flex items-center pb-5">
            <svg
              width="20"
              height="20"
              viewBox="0 0 20 20"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M13.2477 14.11L14.9277 12.43C15.154 12.2066 15.4403 12.0536 15.7518 11.9897C16.0634 11.9258 16.3867 11.9537 16.6827 12.07L18.7302 12.8875C19.0293 13.0089 19.2858 13.2162 19.4673 13.4831C19.6488 13.75 19.7473 14.0647 19.7502 14.3875V18.1375C19.7485 18.3571 19.7023 18.5741 19.6145 18.7753C19.5267 18.9766 19.3991 19.158 19.2393 19.3087C19.0796 19.4594 18.891 19.5761 18.6849 19.652C18.4788 19.7278 18.2595 19.7612 18.0402 19.75C3.69272 18.8575 0.797722 6.70753 0.250222 2.05753C0.224807 1.82918 0.248028 1.59804 0.318359 1.37931C0.388689 1.16058 0.504534 0.959225 0.658273 0.788483C0.812012 0.61774 1.00016 0.481484 1.21034 0.388679C1.42052 0.295873 1.64797 0.248621 1.87772 0.250031H5.50022C5.82348 0.250987 6.13906 0.348631 6.40637 0.530403C6.67368 0.712174 6.8805 0.96976 7.00022 1.27003L7.81772 3.31753C7.93791 3.61233 7.96858 3.93601 7.90588 4.24814C7.84319 4.56027 7.68992 4.847 7.46522 5.07253L5.78522 6.75253C5.78522 6.75253 6.75272 13.3 13.2477 14.11Z"
                fill="#3E5270"
              />
            </svg>
            <div class="mapFont pl-2.5">
              <a href="tel:+852 3892 5089">+852 3892 5089</a>
            </div>
          </div>
          <div class="flex items-center pb-5">
            <svg
              width="24"
              height="24"
              viewBox="0 0 24 24"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <g clip-path="url(#clip0_2958_6021)">
                <path
                  d="M21.5531 4.00019C21.4622 3.99082 21.3706 3.99082 21.2798 4.00019H2.6131C2.49346 4.00203 2.37462 4.01997 2.25977 4.05352L11.8931 13.6469L21.5531 4.00019Z"
                  fill="#3E5270"
                />
                <path
                  d="M22.5404 4.92676L12.8338 14.5934C12.584 14.8418 12.246 14.9811 11.8938 14.9811C11.5415 14.9811 11.2036 14.8418 10.9538 14.5934L1.33378 5.00009C1.3042 5.10878 1.28852 5.22079 1.28711 5.33342V18.6668C1.28711 19.0204 1.42759 19.3595 1.67763 19.6096C1.92768 19.8596 2.26682 20.0001 2.62044 20.0001H21.2871C21.6407 20.0001 21.9799 19.8596 22.2299 19.6096C22.48 19.3595 22.6204 19.0204 22.6204 18.6668V5.33342C22.6151 5.19453 22.5881 5.05731 22.5404 4.92676ZM3.53378 18.6668H2.60711V17.7134L7.45378 12.9068L8.39378 13.8468L3.53378 18.6668ZM21.2738 18.6668H20.3404L15.4804 13.8468L16.4204 12.9068L21.2671 17.7134L21.2738 18.6668Z"
                  fill="#3E5270"
                />
              </g>
              <defs>
                <clipPath id="clip0_2958_6021">
                  <rect width="24" height="24" fill="white" />
                </clipPath>
              </defs>
            </svg>
            <div class="mapFont pl-2.5">
              <a href="mailto:booking@hkcmer.com">booking@hkcmer.com</a>
            </div>
          </div>
          <div class="flex pb-5 items-start">
            <svg
              class="mt-2"
              width="18"
              height="20"
              viewBox="0 0 18 20"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M14 0C13.45 0 13 0.45 13 1V2H5V1C5 0.45 4.55 0 4 0C3.45 0 3 0.45 3 1V2H2C0.89 2 0.00999999 2.9 0.00999999 4L0 18C0 18.5304 0.210714 19.0391 0.585786 19.4142C0.960859 19.7893 1.46957 20 2 20H16C17.1 20 18 19.1 18 18V4C18 2.9 17.1 2 16 2H15V1C15 0.45 14.55 0 14 0ZM16 18H2V8H16V18ZM8 11C8 10.45 8.45 10 9 10C9.55 10 10 10.45 10 11C10 11.55 9.55 12 9 12C8.45 12 8 11.55 8 11ZM4 11C4 10.45 4.45 10 5 10C5.55 10 6 10.45 6 11C6 11.55 5.55 12 5 12C4.45 12 4 11.55 4 11ZM12 11C12 10.45 12.45 10 13 10C13.55 10 14 10.45 14 11C14 11.55 13.55 12 13 12C12.45 12 12 11.55 12 11ZM8 15C8 14.45 8.45 14 9 14C9.55 14 10 14.45 10 15C10 15.55 9.55 16 9 16C8.45 16 8 15.55 8 15ZM4 15C4 14.45 4.45 14 5 14C5.55 14 6 14.45 6 15C6 15.55 5.55 16 5 16C4.45 16 4 15.55 4 15ZM12 15C12 14.45 12.45 14 13 14C13.55 14 14 14.45 14 15C14 15.55 13.55 16 13 16C12.45 16 12 15.55 12 15Z"
                fill="#3E5270"
              />
            </svg>
            <div class="flex flex-col flex-nowrap items-start mapFont pl-2.5">
              <p>星期一至五：10:00 – 13:30 / 14:30 – 18:30</p>
              <p class="mt-1">星期六：09:30 –17:00</p>
              <p class="mt-1">(星期日及公眾假期休息)</p>
            </div>
          </div>
          <div class="flex items-center pb-5">
            <svg
              width="18"
              height="20"
              viewBox="0 0 18 20"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M14.9401 14.7468C16.5156 13.1705 17.4007 11.033 17.4007 8.80439C17.4007 6.57574 16.5156 4.4383 14.9401 2.86199C14.1603 2.0816 13.2343 1.46253 12.2151 1.04016C11.1958 0.617788 10.1034 0.400391 9.00013 0.400391C7.89687 0.400391 6.80441 0.617788 5.7852 1.04016C4.76599 1.46253 3.83999 2.0816 3.06013 2.86199C1.48464 4.4383 0.599609 6.57574 0.599609 8.80439C0.599609 11.033 1.48464 13.1705 3.06013 14.7468L4.88533 16.5456L7.33693 18.9276L7.49653 19.0692C8.42653 19.8228 9.78853 19.7748 10.6645 18.9276L13.5865 16.0836L14.9401 14.7468ZM9.00013 12.4008C8.04535 12.4008 7.12968 12.0215 6.45455 11.3464C5.77942 10.6712 5.40013 9.75557 5.40013 8.80079C5.40013 7.84601 5.77942 6.93034 6.45455 6.25521C7.12968 5.58008 8.04535 5.20079 9.00013 5.20079C9.95491 5.20079 10.8706 5.58008 11.5457 6.25521C12.2208 6.93034 12.6001 7.84601 12.6001 8.80079C12.6001 9.75557 12.2208 10.6712 11.5457 11.3464C10.8706 12.0215 9.95491 12.4008 9.00013 12.4008Z"
                fill="#3E5270"
              />
            </svg>
            <div class="mapFont pl-2.5">旺角站E1出口</div>
          </div>
        </div>
        <div class="pt-30">
          <iframe
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d29531.42797392747!2d114.14283751814892!3d22.29962865616729!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x340401ae16f16839%3A0x3942ab0fd827016f!2z5biM55Gq55y856eR6KaW5YWJ5Lit5b-DIC0g5pe66KeS!5e0!3m2!1szh-CN!2ssg!4v1681190999916!5m2!1szh-CN!2ssg"
            width="375"
            height="268"
            class="iframeSm"
            style="border: 0"
            allowfullscreen="true"
            loading="lazy"
            referrerpolicy="no-referrer-when-downgrade"
          ></iframe>
        </div>
      </div>
    </div>
  </div>
  <PageSmfooter />
</template>

<style scoped lang="scss">
@media (min-width: 768px) {
  .map {
    background: #f2fcff;
  }

  .map_header {
    background: #aad4e5;
  }

  .map_font {
    font-family: 'ABeeZee';
    font-style: normal;
    font-weight: 400;
    font-size: 25px;
    line-height: 30px;
    /* identical to box height */

    display: flex;
    align-items: center;

    /* White */

    color: #ffffff;
  }

  .map_font:active {
    color: #3e5270;
  }

  .map_font:link {
    color: #3e5270;
  }

  .map_header > span {
    font-size: 40px;
    font-weight: 100;
    color: #ffffff;
  }

  .map_footer {
    font-family: 'ABeeZee';
    font-style: normal;
    font-weight: 400;
    font-size: 25px;
    line-height: 30px;
    display: flex;
    align-items: center;

    color: #a9a9a9;
  }

  .map_footer:active {
    color: #00a4ce;
  }

  .map_footer:link {
    color: #00a4ce;
  }
  .map_footer:hover {
    color: #00a4ce;
  }
  .map_footer + span {
    font-size: 40px;
    font-weight: 200;
    color: #a9a9a9;
    margin: 0 2.8rem;
  }

  .rectangle {
    height: 493px;
    width: 884px;
    background: #ffffff;
  }
  .title-font {
    /* PC-Title */

    font-family: 'Noto Sans';
    font-style: normal;
    font-weight: 700;
    font-size: 40px;
    line-height: 54px;
    letter-spacing: 0.1em;

    /* Dark Grey */

    color: #3e5270;
  }
  .font-h5 {
    font-family: 'ABeeZee';
    font-style: normal;
    font-weight: 400;
    font-size: 20px;
    line-height: 30px;
    /* identical to box height, or 150% */

    color: #3e5270;
  }

  .mapFont {
    font-family: 'ABeeZee';
    font-style: normal;
    font-weight: 400;
    font-size: 20px;
    line-height: 30px;
    /* identical to box height, or 150% */

    color: #3e5270;
  }
}
</style>
<style lang="scss" scoped>
@media (max-width: 767px) {
  .map {
    background: #f2fcff;
  }

  .map_header {
    height: 52px;
    background: #aad4e5;
  }

  .map_font {
    font-family: 'ABeeZee';
    font-style: normal;
    font-weight: 500;
    font-size: 16px;
    line-height: 32px;
    /* identical to box height */

    display: flex;
    align-items: center;

    /* White */

    color: #ffffff;
  }

  .map_font:active {
    color: #3e5270;
  }

  .map_font:link {
    color: #3e5270;
  }

  .m-6 {
    margin: 0;
    margin-top: 15px;
    margin-bottom: 50px;
  }
  .pt-30 {
    padding: 0;
  }
  .map_header > span {
    font-size: 40px;
    font-weight: 100;
    color: #ffffff;
  }

  .map_footer {
    font-family: 'Noto Sans CJK TC';
    font-style: normal;
    font-weight: 500;
    font-size: 16px;
    line-height: 32px;
    /* or 200% */

    display: flex;
    align-items: center;
    text-align: center;
    text-decoration-line: underline;

    color: #a9a9a9;
  }

  .map_footer:active {
    color: #00a4cf;
  }

  .map_footer:link {
    color: #00a4cf;
  }
  .map_footer:hover {
    color: #00a4cf;
  }
  .map_footer + span {
    font-size: 24px;
    font-weight: 200;
    color: #a9a9a9;
    margin: 0 22px;
  }

  .rectangle {
    margin-top: 30px;
    padding: 5px 15px;
    width: 374px;
    background: #ffffff;
    display: flex;
    flex-direction: column;
  }
  .title-font {
    /* PC-Title */

    font-family: 'Noto Sans CJK TC';
    font-style: normal;
    font-weight: 700;
    font-size: 40px;
    line-height: 54px;
    letter-spacing: 0.1em;

    /* Dark Grey */

    color: #3e5270;
  }
  .font-h5 {
    font-family: 'Noto Sans CJK TC';
    font-style: normal;
    font-weight: 400;
    font-size: 20px;
    line-height: 30px;
    /* identical to box height, or 150% */

    color: #3e5270;
  }

  .mapFont {
    font-family: 'Noto Sans CJK TC';
    font-style: normal;
    font-weight: 400;
    font-size: 16px;
    line-height: 30px;
    /* identical to box height, or 150% */

    color: #3e5270;
  }
  .iframeSm {
    width: 344px;
    height: 252px;
  }
}
</style>
