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


server script
```
import frappe
from frappe import _
from frappe.model.document import Document

class userinfoserver_scripting(Document):
	#def validate(self):
	#	frappe.msgprint("Hello Frappe")
	#def before_save(self):
	#	frappe.msgprint("before Frappe")
	@frappe.whitelist()
	def mymethod(self,msg):
		return "Hi message from_call"
    ```
