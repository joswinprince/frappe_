Creating buttons with option
```
	frm.add_custom_button(('clear'), ()=> {

		      console.log('clear button initiated')
		      console.log(frm.selected_doc)
		
```
changing row3 and row5 value
```

frm.set_value({
                row3: 'row 3 value',
                row5: 'row 5 value',
                })
		
```
