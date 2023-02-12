- To find if its doctype
```
frappe.is_table(DocType)
```
- To find meta data 
```
frappe.get_meta(DocType)
```
- To get all Doctype for core
```
frappe.db.get_all('DocType',dict(module="Core"))
```
- Get documents
```
frappe.get_doc('Purchase Order', '5af80f6f2d')
```

