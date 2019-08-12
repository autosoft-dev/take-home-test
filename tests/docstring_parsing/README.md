# Docstring converter

**Note**: You can use python's built in modules such as `ast` but please do not use any external library

Write a runnable python script that will convert `@param` docstring into a Google Python style docstring (http://sphinxcontrib-napoleon.readthedocs.io/en/latest/example_google.html)

We will take the following python file as input:

```py
def login(username, password):
    """
    Check credentials and log a user.
    @param username: the user username.
    @param password: the user encrypted password.
    @raises NotAuthorizedException: the credentials are invalid.
    @return True if now logged in, False on error.
    """
    pass
    
 def send_mail(sender, to, subject, content):
    """
    Send a mail.
    @param sender: email address of the sender.
    @param to: email address of the recipient.
    @param subject: the email subject.
    @param content: the email body.
    @return True if sent, else False
    """
    pass
```

You can save it into `sample.py`.


Now write a code in a file named `main.py` that will parse `sample.py` and that will produce a new file named `sample_converted.py` that will look like the following:


```py
def login(username, password):
    """
    Check credentials and log a user.
    
    Args:
        username: the user username.
        password: the user encrypted password.
    
    Raises:
        NotAuthorizedException: the credentials are invalid.
    
    Returns:
        True if now logged in, False on error.
    """
    pass
    
 def send_mail(sender, to, subject, content):
    """
    Send a mail.
    
    Args:
        sender: email address of the sender.
        to: email address of the recipient.
        subject: the email subject.
        content: the email body.
    
    Returns:
        True if sent, else False
    """
    pass
```

Write a unit test that will test your code.
