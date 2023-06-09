## session_unset() and session_destroy()

**session_unset() and session_destroy()** are both functions in PHP used to manage session variables, but they perform different actions.

**session_unset()** is used to unset all of the session variables that have been set during the current session. It does not destroy the session itself, it just removes all the variables that have been set. It does not take any arguments.

**session_destroy()** is used to completely destroy the session that is currently active. This function will remove all session variables, and the session itself. It does not take any arguments.

Here's a summary of the differences between the two functions:

**session_unset():** Removes all the session variables that have been set during the current session. The session itself remains active.

**session_destroy():** Completely destroys the current session, including all of its variables. The session itself is destroyed, and a new session will be started if session_start() is called again.

**session_destroy() function** destroys the whole session rather destroying the variables. When session_start() is called, PHP sets the session cookie in browser. We need to delete the cookies also to completely destroy the session.

Note: If it’s desired to kill the session, also delete the session cookie. This will destroy the session, and not just the session data.

## unset()

To unset a single session variable, you can use the unset() function in PHP. Here's an example of how to unset a single session variable:

```php
<?php 
session_start();
unset($_SESSION['email']);
unset($_SESSION['userid']);
?>
```


In this code, we use the unset() function to remove the 'email' and 'userid' session variables before destroying the session with session_destroy(). 

It's important to note that you need to call session_start() before using the unset() function to access the session variables. Once you've unset the desired session variable(s).

**The session_unset() and session_destroy() functions** do not take any arguments. 