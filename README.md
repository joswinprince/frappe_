# frappe

## Frappe bench initialize
```
bench init frappe_bench_name
```

## start a bench by moving inside the bench
```
bench start
```

## Create a new site after running the bench
```
bench new-site site_name
```

## Create an app in bench
```
bench new-app app_name
```

## Install app in site
```
bench --site  site_name install-app app_name
``` 

## Set Site to developer Mode
```
bench --site site_name set-config developer_mode 1
```
## To clear cache in bench sites
```
bench --site site-name clear-cache
```
## To migrate bench 
```
bench --site sitename migrate
```
events

before save
```
 before_save:function(frm) {
        
        if ((frm.doc.sub_user==null)||(frm.doc.sub_user=="")) // Code to check if first name is empty
        {
            frappe.throw({
                title :("sub user Information"),
                indicator:"red",
                message:__("Sub user should not be Empty")
            })
        }
      
 }
```
