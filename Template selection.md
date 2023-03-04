## cs on Template 1

```
frappe.ui.form.on('Template 1', {
	refresh(frm) {
		// your code here
			frm.add_custom_button(('Back'), ()=> {
			    frappe.confirm('Are you sure you want to goback to template selection',
    () => {
        // action to perform if Yes is selected
                 frappe.new_doc('Template'); // go back to template
    }, () => {
        // action to perform if No is selected
    })
			});
		
	}
})
```
## cs on template

```
frappe.ui.form.on('Template', {
	refresh(frm) {
		// your code here
		//frappe.msgprint("refreshed template")
		
	
	},
    
	name1:function(frm) {
	    frappe.new_doc(frm.doc.name1);
	}
})
```
Seperate Doctype should contain list of Templates
