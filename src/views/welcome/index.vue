<script lang="ts" setup>
import formCreate from "@form-create/element-ui";
//获取 formCreate 组件
const FormCreate = formCreate.$form();
const rule = [
  {
    type: "input",
    field: "Fx2i5y9a3od7o",
    title: "输入框",
    info: "",
    _fc_drag_tag: "input",
    hidden: false,
    display: true
  },
  {
    type: "upload",
    field: "Frad5y9a3nh69",
    title: "上传",
    info: "",
    props: {
      action: "",
      onSuccess:
        "[[FORM-CREATE-PREFIX-onSuccess(u,s){s.url=u.data.url}-FORM-CREATE-SUFFIX]]"
    },
    _fc_drag_tag: "upload",
    hidden: false,
    display: true
  },
  {
    type: "checkbox",
    field: "Fcuc5y9a3ot35",
    title: "多选框",
    info: "",
    effect: {
      fetch: ""
    },
    options: [
      {
        value: "1",
        label: "选项1"
      },
      {
        value: "2",
        label: "选项2"
      }
    ],
    _fc_drag_tag: "checkbox",
    hidden: false,
    display: true
  }
];

const option = {
  form: {
    labelPosition: "right",
    size: "small",
    labelWidth: "125px",
    hideRequiredAsterisk: false,
    showMessage: true,
    inlineMessage: false
  },
  submitBtn: true,
  resetBtn: false
};

const onSubmit = (formData: any) => {
  console.log(formData);
};
</script>
<template>
  <div class="w-96">
    <FormCreate :rule="rule" :option="option" @submit="onSubmit" />
  </div>
</template>
