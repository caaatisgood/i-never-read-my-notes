MVC in Django

MVC | MTV(Django)
--- | -----------
M - model | M - model
V - view | T - template
C - controller | V - view

---

Variable lookup in Templates

Priority | Variable Type | Example | Reference in Python
-------- | ------------- | ------- | -------------------
1 | dictionary | `{{foo.bar}}` | `foo['bar']`
2 | attribute | `{{foo.bar}}` | `foo.bar`
3 | list-index | `{{foo.0}}` | `foo[0]`

---

Session cookie

- Check if cookie is allowed:
```py
HttpRequest.session.set_test_cookie()
HttpRequest.session.test_cookie_worked()
HttpRequest.session.delete_test_cookie()
```

- Usage
```py
from django.contrib.sessions.models import Session
def some_session_cookie_stuff(request):
    sid = request.COOKIES['sessionid']  # or request.session.session_key
    s = Session.objects.get(pk=sid)
    # s.expire_date -> Session expire date
    # s.get_decoded() -> Session content
```

- Session related configs

  `SESSION_EXPIRE_AT_BROWSER_CLOSE` *Boolean* (Default: `False`)
  
  `SESSION_COOKIE_AGE` *Number* (Seconds, default: `1209600`, two weeks)
  
  `SESSION_SERIALIZER`
