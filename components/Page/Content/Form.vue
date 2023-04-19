<script lang="ts" setup>
import { reactive, ref } from 'vue'
import type { FormInstance, FormRules } from 'element-plus'
const { t } = useLang()

const formSize = ref('default')
const cities = [
  '角膜矯形鏡合適性檢查套餐',
  '兒童眼睛檢查套餐',
  '成人眼睛檢查套餐',
  '親友眼睛檢查計劃',
  '隱形眼鏡驗配套餐',
  '青光眼檢查套餐',
  '驗配眼鏡',
  '老花隱形眼鏡檢查及試戴套餐',
  'RGP鏡適配性檢查套餐',
  '其他',
]
const ruleFormRef = ref<FormInstance>()
const ruleForm = reactive({
  name: '',
  tel: '+852',
  email: '',
  address: '',
  FromMe: '',
  checkServe: [],
  sms: '',
})
const telValidator = (rule: any, value: any, callback: any) => {
  if (!value) {
    callback(new Error('請輸入手機號'))
  } else if (!/^(\+?0?852\/-?)\d{8}$/.test(value)) {
    console.log(value, '456465')
    callback(new Error('手機號格式不正確'))
  } else {
    callback()
  }
}

const rules = reactive<FormRules>({
  name: [
    { required: true, message: '請輸入姓名', trigger: 'blur' },
    { min: 3, max: 25, message: '長度應該是3到25', trigger: 'blur' },
  ],
  tel: [{ required: true, validator: telValidator, trigger: 'blur' }],
  email: [
    {
      required: true,
      message: '請輸入電郵地址',
      trigger: 'change',
    },
    {
      type: 'email',
      message: '請輸入正確的電子郵件地址',
      trigger: 'change',
    },
  ],
  address: [{ required: true, message: '請選擇門診地點', trigger: 'blur' }],
  FromMe: [{ required: true, message: '請選擇', trigger: 'blur' }],
  // 目前没有强制校验
  // checkServe: [
  //   {
  //     type: 'array',
  //     required: true,
  //     message: 'Please select at least one activity type',
  //     trigger: 'change',
  //   },
  // ],
})

const submitForm = async (formEl: FormInstance | undefined) => {
  if (!formEl) return
  await formEl.validate((valid, fields) => {
    if (valid) {
      console.log('submit!', ruleForm)
    } else {
      console.log('error submit!', fields)
    }
  })
}
</script>
<template>
  <div>
    <div class="iconHeader">
      <div>
        <span>預約</span>
      </div>
      <div>視光服務</div>
    </div>
  </div>
  <div class="Form">
    <el-form
      ref="ruleFormRef"
      :model="ruleForm"
      :rules="rules"
      label-width="120px"
      require-asterisk-position="right"
      label-position="top"
      class="demo-ruleForm"
      :size="formSize"
      status-icon
    >
      <el-form-item :label="t('pages.content.form.name')" prop="name">
        <el-input v-model="ruleForm.name" clearable placeholder="請輸入姓名" />
      </el-form-item>
      <el-form-item :label="t('pages.content.form.tel')" prop="tel">
        <el-input v-model="ruleForm.tel" clearable placeholder="請輸入手機號" />
      </el-form-item>
      <el-form-item :label="t('pages.content.form.email')" prop="email">
        <el-input
          v-model="ruleForm.email"
          clearable
          placeholder="請輸入電郵地址"
        />
      </el-form-item>
      <el-form-item :label="t('pages.content.form.address')" prop="address">
        <el-select
          v-model="ruleForm.address"
          clearable
          placeholder="請選擇"
          placement="bottom"
        >
          <el-option label="Zone one" value="shanghai" />
          <el-option label="Zone two" value="beijing" />
        </el-select>
      </el-form-item>
      <el-form-item :label="t('pages.content.form.FromMe')" prop="FromMe">
        <el-select
          v-model="ruleForm.FromMe"
          placeholder="請選擇"
          placement="bottom"
          clearable
        >
          <el-option label="Zone one" value="shanghai" />
          <el-option label="Zone two" value="beijing" />
        </el-select>
      </el-form-item>
      <el-form-item :label="t('pages.content.form.checkServe')">
        <el-checkbox-group v-model="ruleForm.checkServe" clearable>
          <el-checkbox
            v-for="serve in cities"
            :key="serve"
            class="serve"
            :label="serve"
            >{{ serve }}</el-checkbox
          >
        </el-checkbox-group>
      </el-form-item>
      <el-form-item :label="t('pages.content.form.sms')" prop="sms">
        <el-input
          v-model="ruleForm.sms"
          type="textarea"
          style="min-height: 40px"
          :rows="2"
          placeholder="請輸入詳細內容"
          clearable
        />
      </el-form-item>
      <el-form-item>
        <el-button @click="submitForm(ruleFormRef)">
          {{ t('pages.content.form.submit') }}
        </el-button>
      </el-form-item>
    </el-form>
  </div>
</template>

<style scoped lang="scss">
@media (min-width: 768px) {
  .Form {
    background: #fff;
    width: 732px;
    height: 634px;
    box-shadow: 4px 4px 4px rgba(0, 0, 0, 0.1);
    border-radius: 5px;
    margin: 0 auto;
    padding: 20px 36px 30px 40px;
    margin-bottom: 94px;
  }
  .iconHeader {
    margin: 20px 0;
    margin-bottom: 43px;
    font-family: 'Noto Sans';
    font-style: normal;
    font-weight: 700;
    font-size: 40px;
    line-height: 54px;
    display: flex;
    align-items: center;
    justify-content: center;
    letter-spacing: 0.1em;

    /* 白色 */
    color: #ffffff;
  }

  .iconHeader > div:nth-child(1) {
    position: relative;
    width: 94px;
    height: 54px;
    background: #00a4ce;
    box-sizing: border-box;
    & > span {
      margin-left: 6px;
    }
  }

  .iconHeader > div:nth-child(2) {
    color: #3e5270;
    margin-left: 2px;
  }
  :deep(.el-form) {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: flex-start;
  }
  :deep(.el-form-item) {
    width: 302px;
  }
  :deep(.el-form > div:nth-child(2n + 1)) {
    margin-right: 48px;
  }
  :deep(.el-form > div:nth-child(6)) {
    width: 600px;
  }
  :deep(.el-form > div:nth-child(7)) {
    width: 505px;
    height: 40px;
    margin-right: 0;
  }
  :deep(.el-form > div:last-child) {
    width: 120px;
    height: 40px;
    margin-right: 0;
    margin-top: 26px;
    margin-left: 30px;
  }
  :deep(.el-select) {
    width: 100%;
  }
  :deep(.el-checkbox) {
    width: 268px;
  }
  :deep(.el-button) {
    width: 120px;
    height: 40px;
    background: #00a4ce;
    border-radius: 5px;
    font-family: 'Noto Sans CJK TC';
    font-style: normal;
    font-weight: 500;
    font-size: 16px;
    line-height: 32px;
    /* identical to box height, or 200% */

    letter-spacing: 1em;

    /* 白色 */

    color: #ffffff;
    & > span {
      margin-left: 18px;
    }
  }
  :deep(.el-form-item__label) {
    font-family: 'Noto Sans CJK TC';
    font-style: normal;
    font-weight: 700;
    font-size: 20px;
    line-height: 40px;
    /* or 200% */

    /* Dark Grey */

    color: #3e5270;

    /* Inside auto layout */

    flex: none;
    order: 0;
    align-self: stretch;
    flex-grow: 0;
  }
  :deep(
      .el-form-item.is-required:not(.is-no-asterisk).asterisk-right
        > .el-form-item__label:after
    ) {
    color: #00a4ce;
  }
  :deep(.el-input__wrapper) {
    width: 302px;
    height: 40px;
    border: 1px solid #cccccc;
    border-radius: 8px;
  }
  :deep(.el-input__inner) {
    font-family: 'Noto Sans CJK TC';
    font-style: normal;
    font-weight: 500;
    font-size: 16px;
    line-height: 32px;
    /* or 200% */

    display: flex;
    align-items: center;

    /* Blue */

    color: #6ebcd2;
  }
  :deep(.el-form-item__content) {
    line-height: 44px;
  }
  :deep(.el-textarea__inner) {
    width: 505px;
    min-height: 40px;
    font-size: 16px;
    line-height: 1;
    margin: 3px 11px;
    border: 1px solid #cccccc;
    font-weight: 500;
    border-radius: 8px;
    color: #6ebcd2;
  }
  :deep(.el-input) {
    input {
      &::placeholder {
        font-family: 'Noto Sans CJK TC';
        font-style: normal;
        font-weight: 500;
        font-size: 16px;
        line-height: 32px;
        color: #6ebcd2;
      }

      &::-webkit-input-placeholder {
        font-family: 'Noto Sans CJK TC';
        font-style: normal;
        font-weight: 500;
        font-size: 16px;
        line-height: 32px;
        color: #6ebcd2;
      }
    }
  }

  :deep(.el-textarea) {
    textarea {
      &::placeholder {
        font-family: 'Noto Sans CJK TC';
        font-style: normal;
        font-weight: 500;
        font-size: 16px;
        line-height: 36px;

        color: #6ebcd2;
      }

      &::-webkit-input-placeholder {
        font-family: 'Noto Sans CJK TC';
        font-style: normal;
        font-weight: 500;
        font-size: 16px;
        line-height: 32px;

        color: #6ebcd2;
      }
    }
  }
}
</style>
<style lang="scss" scoped>
/**********************************************************分割线*******************************************************************************************/
@media (max-width: 767px) {
  .Form {
    width: 350px;
    margin: auto;
    margin-bottom: 92px;
    padding: 19px 24px;
    background: #ffffff;
    /* Soft Shadow */

    box-shadow: 4px 4px 4px rgba(0, 0, 0, 0.1);
    border-radius: 5px;
  }

  .iconHeader {
    margin: 20px 0;
    font-family: 'Noto Sans CJK TC';
    font-style: normal;
    font-weight: 700;
    font-size: 24px;
    line-height: 36px;
    display: flex;
    align-items: center;
    justify-content: center;
    letter-spacing: 0.1em;

    /* 白色 */
    color: #ffffff;
  }

  .iconHeader > div:nth-child(1) {
    position: relative;
    width: 54px;
    height: 36px;
    background: #00a4ce;
    box-sizing: border-box;
  }

  .iconHeader > div:nth-child(2) {
    color: #3e5270;
    margin-left: 2px;
  }

  :deep(.el-button) {
    background: #00a4ce;
    width: 108px;
    height: 43px;

    font-family: 'Noto Sans CJK TC';
    font-style: normal;
    font-weight: 500;
    font-size: 16px;
    line-height: 32px;
    /* identical to box height, or 200% */

    display: flex;
    align-items: center;
    letter-spacing: 0.5em;

    /* 白色 */

    color: #ffffff;
  }

  /* deep 都是修改element默认样式的穿透 el-form-item__label:after ✳的颜色 el-form-item__label 标题的颜色 el-input__inner input输入框输入的字颜色 el-input__wrapper 边框样式 .el-input)   input   &::placeholder    提示文字的样式  */
  :deep(
      .el-form-item.is-required:not(.is-no-asterisk).asterisk-right
        > .el-form-item__label:after
    ) {
    color: #00a4ce;
  }

  :deep(.el-form-item__label) {
    font-family: 'Noto Sans CJK TC';
    font-style: normal;
    font-weight: 700;
    font-size: 20px;
    line-height: 40px;
    color: #3e5270;
  }

  :deep(.el-input__inner) {
    font-family: 'Noto Sans CJK TC';
    font-style: normal;
    font-weight: 500;
    font-size: 16px;
    line-height: 32px;
    color: #6ebcd2;
  }

  :deep(.el-input__wrapper) {
    width: 302px;
    height: 40px;
    border: 1px solid #cccccc;
    border-radius: 8px;
  }

  :deep(.el-textarea__inner) {
    width: 302px;
    height: 90px;
    line-height: 2;
    font-size: 16px;
    border: 1px solid #cccccc;
    font-weight: 500;
    border-radius: 8px;
    color: #6ebcd2;
  }

  :deep(.el-checkbox-group) {
    display: flex;
    flex-direction: column;
  }

  /** 选中选项颜色 */
  :deep(.el-checkbox__input.is-checked + .el-checkbox__label) {
    color: #3e5270;
  }

  :deep(.el-checkbox__inner) {
    width: 24px;
    height: 24px;
    border-color: #ccc;
    border-radius: 8px;
    // 00a4ce
  }

  :deep(.el-checkbox__input.is-checked .el-checkbox__inner) {
    border-color: #00a4ce;
    background-color: #00a4ce;
  }

  :deep(.el-checkbox__inner::after) {
    box-sizing: content-box;
    content: '';
    border: 2px solid #fff;
    border-left: 0;
    border-top: 0;
    height: 12px;
    left: 7px;
    position: absolute;
    top: 2px;
    transform: rotate(45deg) scaleY(0);
    width: 5px;
    transition: transform 0.15s ease-in 50ms;
    transform-origin: center;
  }

  :deep(.el-checkbox__label) {
    font-family: 'Noto Sans CJK TC';
    font-style: normal;
    font-weight: 500;
    font-size: 16px;
    line-height: 32px;
    color: #3e5270;
  }

  :deep(.el-input) {
    input {
      &::placeholder {
        font-family: 'Noto Sans CJK TC';
        font-style: normal;
        font-weight: 500;
        font-size: 16px;
        line-height: 32px;
        color: #6ebcd2;
      }

      &::-webkit-input-placeholder {
        font-family: 'Noto Sans CJK TC';
        font-style: normal;
        font-weight: 500;
        font-size: 16px;
        line-height: 32px;
        color: #6ebcd2;
      }
    }
  }

  :deep(.el-textarea) {
    textarea {
      &::placeholder {
        font-family: 'Noto Sans CJK TC';
        font-style: normal;
        font-weight: 500;
        font-size: 16px;
        line-height: 32px;

        color: #6ebcd2;
      }

      &::-webkit-input-placeholder {
        font-family: 'Noto Sans CJK TC';
        font-style: normal;
        font-weight: 500;
        font-size: 16px;
        line-height: 32px;

        color: #6ebcd2;
      }
    }
  }
}
</style>
