MVC in Django:

MVC | MTV(Django)
--- | -----------
M - model | M - model
V - view | T - template
C - controller | V - view

---

Variable lookup in Templates:

Priority | Variable Type | Example | Reference in Python
- | - | - | -
1 | dictionary | `{{foo.bar}}` | `foo['bar']`
2 | attribute | `{{foo.bar}}` | `foo.bar`
3 | list-index | `{{foo.0}}` | `foo[0]`

---
