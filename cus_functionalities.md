Roles and Perrmissions button in list view
```
onload: function(listview) {

		listview.page.add_menu_item(__("Clear Error Logs"), function() {

			frappe.msgprint("button called");

		});

		listview.page.add_inner_button(__("Roles"), function () {

			frappe.msgprint("bulk delete button called");

		},__("Roles & Permissions"));

		listview.page.add_inner_button(__("Permission"), function () {

			frappe.msgprint("bulk delete button called");

		},__("Roles & Permissions"));

		

	}
```
To create the frappe.session.user
```
<!--{% if frappe.session.user == 'Administrator' %}

    				<button>Admin button</button>

   				 {% else %}

   				 <button>user button</button>

   				 {% endif %} 

   				 -->

   				 <kbd>

   				{%  print " Welcome, "+ frappe.session.user  %} 

   								

   				</kbd>
```
## Add Dynamic buttons
```
button_name = ['Role','Role Profile','Activity Log'];
        route_value = ['role','role profile','activity log'];
        for (let i = 0; i < 2; i++) {
                listview.page.add_inner_button(__(button_name[i]), function () {
            frappe.set_route("List", route_value[i]);
        },__("Views"));
            }
        //frappe.has_permission("abcd", "read", user='user@321.com')
```
