
取消radio的选择
$('input').attr('checked', false);

选择到父节
$('#id').parent('div'); // 不包含div
$('#id').parents('div'); // 包含div

失去焦点委托body处理
$('body').on('focusout', function(e) {
  console.log('失去焦点:', e.target);
})
