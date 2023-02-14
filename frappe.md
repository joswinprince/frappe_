
Creating buttons with group
```
frm.add_custom_button(__('Get User Email Address'), function(){ frappe.msgprint(frm.doc.email); }, __("Utilities"));
```

Creating buttons 
```
	frm.add_custom_button(('clear'), ()=> {

		      console.log('clear button initiated')
		      console.log(frm.selected_doc)
		      });
		
```
changing row3 and row5 value
```

frm.set_value({
                row3: 'row 3 value',
                row5: 'row 5 value',
                })
		
```

esign
```frappe.ui.form.on('Purchase Order', {
	refresh(frm) {
		// your code here
            			frm.add_custom_button(('ESignature'), ()=> {
            
            		      
            		let d = new frappe.ui.Dialog({
                title: 'Esign',
                fields: [
                    {
                        label: 'User',
                        fieldname: 'user',
                        fieldtype: 'Data'
                    },
                    {
                        label: 'Password',
                        fieldname: 'pass',
                        fieldtype: 'Password'
                    }
                    
                ],
                primary_action_label: 'Submit',
                primary_action(values) {
                    console.log(values);
                    d.hide();
                }
            });
                    d.show();
      });
		


	}
})
```
