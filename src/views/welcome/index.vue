<!--<script lang="ts" setup>
defineOptions({
  name: "Welcome"
});
</script>-->
<script>
import formCreate from "@form-create/element-ui";

export default {
  name: "Welcome",
  data() {
    return {
      fapi: null,
      rule: formCreate.parseJson(
        '[{"type":"input","field":"F1kt5y8pzlkrq","title":"输入框","info":"","_fc_drag_tag":"input","hidden":false,"display":true},{"type":"inputNumber","field":"Frqm5y8pzltbl","title":"计数器","info":"","_fc_drag_tag":"inputNumber","hidden":false,"display":true},{"type":"switch","field":"F5wp1nif7w5bcs","title":"开关","info":"","_fc_drag_tag":"switch","hidden":false,"display":true},{"type":"select","field":"Fzlm1nif7w6oqn","title":"选择器","info":"","effect":{"fetch":""},"options":[{"value":"1","label":"选项1"},{"value":"2","label":"选项2"}],"_fc_drag_tag":"select","hidden":false,"display":true}]'
      ),
      option: formCreate.parseJson(
        '{"form":{"labelPosition":"right","size":"small","labelWidth":"125px","hideRequiredAsterisk":false,"showMessage":true,"inlineMessage":false},"submitBtn":true,"resetBtn":true}'
      )
    };
  },
  methods: {
    onSubmit(formData) {
      //todo 提交表单
      console.log(formData);
    }
  }
};
</script>
<template>
  <form-create
    v-model="fapi"
    :rule="rule"
    :option="option"
    @submit="onSubmit"
  />
</template>
