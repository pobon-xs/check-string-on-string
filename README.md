# Check string inside another string

if ($('#wp-admin-bar-elementor_edit_page-default').length > 0) {
    var elements = $('#wp-admin-bar-elementor_edit_page-default').children('li');
    $(elements).map(function (__, element) {
      var target = $(element).find(".elementor-edit-link-title");
      if (target.text().indexOf('dynamic-content-') !== -1) {
        target.parent().parent().remove();
      }
    });
  }
