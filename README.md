vuejs-contenteditable
=====================

contenteditable binding for vuejs

Todo
----

v-model directive can only be used on textarea o or input elements for now.
It would be nice to use it on 'contenteditable' !

Content editable involves a lot more complexity than input bindings, 
and it's best to use an external library dedicated to this purpose (e.g. Medium.js), wrapped by a custom directive.

see: [v-model directive on <div contenteditable>](https://github.com/vuejs/vue/issues/1670)

Solution ?
----------

Abdul Ahkam wrote:

```
My solution is you can use summernote's onChange callbacks like so :
let 'program' as my vue instance
and 'detail' as my model in 'program'.

	$('#summernote').summernote({
		onChange: function(contents, $editable) {
			// console.log($editable);
            program.detail = $editable;
        }
    })

I do not know if this is a good way to solve your problem
*most probably you have already got it
```

see: [](https://github.com/vuejs/vue/issues/1670#issuecomment-165998697)

