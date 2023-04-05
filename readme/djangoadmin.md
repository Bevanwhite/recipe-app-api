## Django admin

1. what is the django admin?
* graphical user interface for models
    * create, Read, Update, Delete
* very littlecoding required

2. how to enable django admin?
    * Enabled per model
    * inside admin.py
        * admin.site.register(Recipe)

3. how to customise the django admin?
    * create class based off ModelAdmin or UserAdmin
    * override/set class varibales

4. changing list of objects?
    * `ordering:` changes order items appear
    * `list_display:` fields to appear in list

5. add/update page?
    * `fieldssets:` control layout of page
    * `readonly_fields:` fields that cannot be changed

6. add Page?
    * `add_fieldsets:` fields displayed only on add page
