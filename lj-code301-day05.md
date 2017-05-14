#LJ-code301-day05

I learned that when address tag inside of an article tag it represents contact information for that article.
 I also learned that

 articleView.populateFilters = function() {
   This is to assign the function as a property to articleView
  $('article').each(function() {
    the function inside each is called anonymous call back function.
    if (!$(this).hasClass('template')) {
      var val = $(this).find('address a').text();
      the grab the address a.
      var optionTag = `<option value="${val}">${val}</option>`;
      to assign value to option tag.

      if ($(`#author-filter option[value="${val}"]`).length === 0) {
        this is to check if the vale is already exist in the author filter
        $('#author-filter').append(optionTag);
      }

      val = $(this).attr('data-category');
      optionTag = `<option value="${val}">${val}</option>`;
      if ($(`#category-filter option[value="${val}"]`).length === 0) {
        $('#category-filter').append(optionTag);
      }
    }
  });
};

Also we created a block so that we can input text and has a preview and shows draft if it's unfinished. 
