1. what feature of django?
    * built in authentication system
    * framework for basic features
        * registration
        * login
        * Auth
    * integrates with django admin

2. what are the Django user model?
    * foundation of the django auth system
    * Default user model
        * username instead of email 
        * not easy to customise
    * create a custom model for new projects
        * allows for using email instead of username
        * Future proof project for later changes to user model
    
3. how to customise user model?
    * create model
        * base from `AbstractBaseUser` and `PermissionsMixin`
    * create custom manager
        * used for cli integration
    * set `Auth_USER_MODEL` in settings.py
    * create and run migrations

4. what does `AbstractBaseUser` have?
    * provides features for authentication
    * doesn't include fields

5. `PermissionsMixin
    * support for django permission system
    * includes fields and methods

6. common issues
    * running migrations before setting custom model
        * set custom model first
    * typos in config
    * indentation in manager or model

### Design custom user model

7. what are the user fields
    * email(EmailField)
    * name(CharField)
    * is_active(BooleanField)
    * is_staff(BooleanField)

8. what does user model manager do?
    * used to manage objects
    * custom logic for creating objects
        * Hash password
    * used by django cli
        * create superuser

9. what does BaseUserManager will handle?
    * base class for managing users
    * userful helper methods
        * `noramlize_email:` for storing emails consistently
    * methods we'll define
        * `create_user:` called when creating user
        * `create_superuser:` used by cli to create a superuser(admin)
