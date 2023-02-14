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
