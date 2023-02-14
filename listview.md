To add button in list view
```
refresh: function(listview) {
        listview.page.add_inner_button("Button Name", function() {
            ButtonFunction(listview);
        });;
    }
 ```
 To add menu button 
 ```
 listview.page.add_menu_item(__("Clear Error Logs"), function() {

			frappe.msgprint("button called");
   ```
    
