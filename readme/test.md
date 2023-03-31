### testing in django 

1. why do you use django test framework?
    * this comes built-in
    * based on the unittest library.
    * django adds features
        * test client - dummy web browser
        * simulate authentication
        * temporary database
    * django rest framework adds features
        * api test client

2. where do you put tests?
    * placeholder `tests.py` added to each app 
    * or create `tests/` subdirectory to split tests up
    * keep in mind:
        * only use `tests.py` or `tests/` directory (not both)
        * test modules must start with test_
        * test directories must contain `__init__.py`

3. can we have a test database?
    * test code that uses the db
    * specific database for tests
    * happens for every test(by default)

4. what  are the test classes?
    * SimpleTestCase
        * no database integration
        * useful if no database is required for your test
        * save time executing tests
    * TestCase
        * Database integration
        * useful for testing code that uses the database

5. how to write writing test?
    * import test class
        * SimpleTestCase - no database
        * TestCase - Database
    * import objects to test
    * define test class
        * you have to base the class from either the SimpleTestCase or TestCase
            * `class ViewTests(SimpleTestCase):` or
            * `class ViewTests(TestCase):`
    * add test method
        * when you write the test you need to prefix the method name start from `test_` then only it will be picked up by the test runner.
    * setup inputs - variable or data to test the code
    * execute code to be tested 
    * check output - whether it equals to what you predict

6. what is mocking? 
    * override or charge behaviour of dependencies
    * avoid unintended side effects
    * isolate code being tested

7. why use mocking?
    * aviod relying on external services
        * can't guarantee they will be available
        * makes tests unpredictable and inconsistent
    * aviod unintended consequences
        * accidentally sending emails
        * overloading external services

8. what happen in mocking? 
    * register_user() -> create_in_db -> send_welcome_email()
    * we are mocking the send_welcome_email()
    * prevent email being send
    * ensure send_welcome_email() called correctly

9. another benefit 
    * speed up tests 
        * check_db() -> sleep() -> in this without sleeping you can mock the code

10. how to mock code?
    * use unittest.mock 
        * MagicMock / Mock - replace real objects
        * patch - overrides code for tests

