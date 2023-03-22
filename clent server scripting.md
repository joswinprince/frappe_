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
server script call
```
frm.call({
	doc: frm.doc,
	method: 'frm_call',
	args: { 
		msg:"hiii"
	},
	freeze: true,
	freeze_message:__('calling frm_server js file'),
	callback: function(r) {
	frappe.msgprint(r.message)
	}
	});
```
# User Info server scripting
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
		frappe.msgprint("client message From server ----"+fname+mname)
		return "return from server"
	@frappe.whitelist()	
	def new_document(self,fname,mname,lname,row1,row2,row3,row4,row5,row6):
		doc = frappe.new_doc('user info server_scripting')
		doc.first_name = fname
		doc.last_name = lname
		doc.middle_name = mname
		if row1=="" :
			pass
		else:
			doc.row1 = row1
			doc.insert()
			doc.row1 = ""
		if row2=="":
			pass
		else:
			doc.row2 = row2
			#doc.autoname = doc.autoname+1
			doc.insert()
			doc.row2 = ""
		if row3=="":
			pass
		else:
			doc.row3 = row3
			#doc.autoname = doc.autoname+1
			doc.insert()
			doc.row3 = ""
		if row4=="":
			pass
		else:
			doc.row4 = row4
			#doc.autoname = doc.autoname+1
			doc.insert()
			doc.row4 = ""
		if row5=="":
			pass
		else:
			doc.row5 = row5
			#doc.autoname = doc.autoname+1
			doc.insert()
			doc.row5 = ""
		if row6=="":
			pass
		else:
			doc.row6 = row6
			#doc.autoname = doc.autoname+1
			doc.insert()
			doc.row6 = ""
		return "new document called"
		
	
```
Java script calling
```
$('#submit_file_transfer_engine') 
.off() // unbind everything to start so that you're only attaching a single handler
.on('click', () => { // bind a function to the click event
    frappe.call({
        method: "folder_name.folder_name.doctype.doctype_name.api.method_name",
        type: "GET",
        args: {
        	
        },
        async: true,
        callback: function (r) {
            frappe.msgprint('...');
        	/* if (r.exc) {
        		frappe.msgprint(__("Unable to load: {0}", [__(doctype)]));
        		throw "No doctype";
        	}
        	if (r.message == "use_cache") {
        		frappe.model.sync(cached_doc);
        	} else {
        		frappe.model.set_in_localstorage(doctype, r.docs);
        	}
        	frappe.model.init_doctype(doctype);
        
        	if (r.user_settings) {
        		// remember filters and other settings from last view
        		frappe.model.user_settings[doctype] = JSON.parse(r.user_settings);
        		frappe.model.user_settings[doctype].updated_on = moment().toString();
        	}
        	callback && callback(r); */
        }
    }); // the action you want the button to execute
});

```
