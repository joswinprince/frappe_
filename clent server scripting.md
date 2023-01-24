client script
```
 frappe.ui.form.on("server scripting 1", {
	refresh(frm) {
	
 	},
	enable:function(frm){
	frm.call({
	doc: frm.doc,
	method: 'mymethod',
	args: { 
		msg:"hiii"
	},
	freeze: true,
	freeze_message:__('calling frm_call method'),
	callback: function(r) {
	frappe.msgprint(r.message)
	}
	});
	}
 	
 	});
```
