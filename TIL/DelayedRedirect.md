---
title: "URL Redirect with a delay"
author: "Isaac Flath"
date: "2024-8-19"
description: "Redirect with a delay using Meta tag in FastHTML in exception handler"
categories: [FastHTML, Python, Web Development]
---

# Today I Learned

You can set up a delated redirect with the Meta HTML tag.  Conveniently you can use this in a 404 exception handler if your site moved to catch any possible route/link users go to.

I did to redirect people to the new location of the FastHTML gallery site.

```python
from fasthtml.common import *

new_url = "https://gallery.fastht.ml/"
def _not_found(req, exc):
    msg = Div(H1("We moved to ",A(href=new_url)(new_url))
            P("Please update your bookmark!  Redirecting in 3 seconds..."))
    return msg,Meta(http_equiv="refresh", content=f"3;url={new_url}")

app = FastHTML(exception_handlers={404:_not_found})

serve()
```
