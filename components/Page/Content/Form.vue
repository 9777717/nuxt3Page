<script lang="ts" setup>
import { reactive, ref } from 'vue'
import type { FormInstance, FormRules } from 'element-plus'
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
  phone: '+852',
  email: '',
  region: '',
  count: '',
  type: [],
  desc: '',
})

// 手机号码自定义验证规则
const telValidator = (rule: any, value: any, callback: any) => {
  if (!value) {
    callback(new Error('请输入手机号'))
  } else if (!/^(\+?0?852\/-?)([6|9])\d{7}$/.test(value)) {
    callback(new Error('手机号格式不正确'))
  } else {
    callback()
  }
}

const rules = reactive<FormRules>({
  name: [
    { required: true, message: '請輸入姓名', trigger: 'blur' },
    { min: 3, max: 25, message: '長度應該是3到25', trigger: 'blur' },
  ],
  phone: [{ required: true, validator: telValidator, trigger: 'blur' }],
  region: [
    {
      required: true,
      message: '請選擇選擇門診地點',
      trigger: 'change',
    },
  ],
  count: [
    {
      required: true,
      message: '請選擇從哪裡找到我們網站',
      trigger: 'change',
    },
  ],
})

const submitForm = async (formEl: FormInstance | undefined) => {
  if (!formEl) return
  await formEl.validate((valid, fields) => {
    if (valid) {
      console.log('submit!')
    } else {
      console.log('error submit!', fields)
    }
  })
}

const options = Array.from({ length: 10000 }).map((_, idx) => ({
  value: `${idx + 1}`,
  label: `${idx + 1}`,
}))
const { t } = useLang()
const arrEye = t('pages.content.eyeServe')
console.log(arrEye, 'eyeServe')
</script>
<template>
  <div class="form flex flex-col items-center">
    <div class="bookingService">
      <div>預約</div>
      <div>視光服務</div>
    </div>
    <div class="formBg">
      <el-form
        ref="ruleFormRef"
        :model="ruleForm"
        :rules="rules"
        label-position="top"
        label-width="302px"
        require-asterisk-position="right"
        class="demo-ruleForm"
        :size="formSize"
        status-icon
      >
        <el-form-item class="fontStyle" label="姓名" prop="name">
          <el-input
            v-model="ruleForm.name"
            placeholder="請輸入姓名"
            clearable
          />
        </el-form-item>

        <el-form-item class="fontStyle" label="聯絡電話" prop="phone">
          <el-input v-model="ruleForm.phone" clearable />
        </el-form-item>

        <el-form-item
          class="fontStyle"
          label="電郵地址"
          prop="email"
          :rules="[
            {
              required: true,
              message: '請輸入電郵地址',
              trigger: 'blur',
            },
            {
              type: 'email',
              message: '請輸入正確的電子郵件地址',
              trigger: 'change',
            },
          ]"
        >
          <el-input
            v-model="ruleForm.email"
            clearable
            placeholder="請輸入電郵地址"
          />
        </el-form-item>

        <el-form-item class="fontStyle" label="選擇門診地點" prop="region">
          <el-select v-model="ruleForm.region" clearable placeholder="請選擇">
            <el-option label="Zone one" value="shanghai" />
            <el-option label="Zone two" value="beijing" />
            <el-option label="Zone three" value="nanjing" />
          </el-select>
        </el-form-item>

        <el-form-item
          class="fontStyle"
          label="從哪裡找到我們網站？"
          prop="count"
        >
          <el-select
            v-model="ruleForm.count"
            clearable
            placeholder="請選擇"
            :options="options"
          />
        </el-form-item>
        <el-form-item class="fontStyle" label="請選擇服務" prop="type">
          <el-checkbox-group v-model="ruleForm.type" clearable>
            <el-checkbox
              v-for="serve in cities"
              :key="serve"
              class="serve"
              :label="serve"
              >{{ serve }}</el-checkbox
            >
          </el-checkbox-group>
        </el-form-item>
        <el-form-item class="fontStyle textarea" label="訊息" prop="desc">
          <el-input
            v-model="ruleForm.desc"
            :rows="1"
            type="textarea"
            placeholder="請輸入詳細內容"
            clearable
          />
        </el-form-item>
        <el-form-item>
          <el-button
            size="large"
            type="primary"
            class="largeColor"
            @click="submitForm(ruleFormRef)"
          >
            遞交
          </el-button>
        </el-form-item>
      </el-form>
    </div>
  </div>
</template>

<style scoped lang="scss">
.bookingService {
  padding-top: 55px;
  padding-bottom: 43px;

  font-family: 'Noto Sans';
  font-style: normal;
  font-weight: 700;
  font-size: 40px;
  line-height: 42px;
  display: flex;
  align-items: center;
  text-align: center;
  letter-spacing: 0.1em;

  color: #3e5270;
}

.bookingService > div:nth-child(1) {
  color: white;
  background: #00a4ce;
  width: 92px;
  height: 48px;
  line-height: 42px;
  padding-left: 4px;
  display: inline-block;
  box-sizing: border-box;
}

.serve {
  width: 300px;
  margin-right: 0;
}

:deep(.el-checkbox__label) {
  font-family: 'Noto Sans CJK TC';
  font-style: normal;
  font-weight: 500;
  font-size: 16px;
  line-height: 32px;

  display: flex;
  align-items: center;

  color: #3e5270;
}

:deep(.el-checkbox-group) {
  display: flex;
  flex-wrap: wrap;
}

.formBg {
  width: 732px;
  padding-top: 18px;
  padding-left: 40px;
  padding-right: 36px;
  padding-bottom: 29px;
  background: white;

  box-shadow: 4px 4px 4px rgba(0, 0, 0, 0.1);
  border-radius: 5px;

  margin-bottom: 94px;
}

.formBg > input {
  color: #6ebcd2;
}

.demo-ruleForm {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: flex-end;
}

:deep(.el-input__inner) {
  color: #6ebcd2;
}

:deep(.el-textarea__inner) {
  color: #6ebcd2;
  height: 44px;
}

:deep(.el-input__inner::placeholder) {
  font-family: 'Noto Sans CJK TC';
  font-style: normal;
  font-weight: 500;
  font-size: 16px;
  line-height: 32px;

  color: #6ebcd2;
}

:deep(.el-textarea__inner::placeholder) {
  font-family: 'Noto Sans CJK TC';
  font-style: normal;
  font-weight: 500;
  font-size: 16px;
  line-height: 32px;
  color: #6ebcd2;
}

/** 默认样式 */
:deep(.el-input__wrapper) {
  background: #ffffff;
  border: 1px solid #cccccc;
  border-radius: 8px;
}

// 宽度调整
:deep(.el-textarea__inner) {
  width: 505px;
}

:deep(.el-select) {
  width: 302px;
}

:deep(.el-input) {
  width: 302px;
}

// label文字样式
.fontStyle,
:deep(.el-form-item__label) {
  /* Noto Bold */

  font-family: 'Noto Sans CJK TC';
  font-style: normal;
  font-weight: 700;
  font-size: 20px;
  line-height: 40px !important;

  color: #3e5270;
}

.largeColor {
  width: 108px;
  height: 43px;
  background: #00a4ce;
  border-radius: 5px;
}

.largeColor {
  font-family: 'Noto Sans CJK TC';
  font-style: normal;
  font-weight: 500;
  font-size: 16px;
  line-height: 32px;
  letter-spacing: 0.5em;

  color: #ffffff;
}

:deep(.el-checkbox__label) {
  padding-left: 16px;
}

:deep(.el-checkbox__inner) {
  width: 24px;
  height: 24px;
  border: 1px solid #cccccc;
  border-radius: 8px;
}

:deep(.el-checkbox__inner::after) {
  width: 8px;
  height: 14px;
  left: 6px;
  border: 2px solid #ffffff;
  border-left: 0;
  border-top: 0;
}

/deep/ .el-checkbox {
  .el-checkbox__input.is-checked .el-checkbox__inner,
  .el-checkbox__input.is-indeterminate .el-checkbox__inner {
    background-color: #00a4ce;
    border: 1px solid #cccccc;
    border-radius: 8px;
  }

  .el-checkbox__input.is-focus .el-checkbox__inner,
  .el-checkbox__inner:hover {
    border-color: #00a4ce;
  }
}
</style>
