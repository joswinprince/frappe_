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
 server script time
 ```
 # Copyright (c) 2023, jos and contributors
# For license information, please see license.txt

import frappe
from frappe import _
from frappe.model.document import Document

class userinfoserver_scripting(Document):
	#def validate(self):
	#	frappe.msgprint("Hello Frappe")
	#def before_save(self):
	#	frappe.msgprint("before Frappe")
	@frappe.whitelist()
	def frm_call(self,msg):
		import time
		time.sleep(5)
		frappe.msgprint(msg)
		return "Hi message from_call"
		```
