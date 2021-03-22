---
title: Code test
date: "2019-06-11T08:38:00.000Z"
draft: yes
---

Every blog starts with a single post. This is yours. Make it great.

<!-- more -->

This post intentionally left blank.

Write what you want.

```html
<script>
    let count = 0

    function handleClick() {
        count += 1
    }
</script>

<button on:click="{handleClick}">
    Clicked {count} {count === 1 ? 'time' : 'times'}
</button>

<style lang="stylus">
    .something
        font-size 1.1em
</style>
```

```python
# This is a comment

class Something:
    """
    This is a big comment block
    """
    def __init__(self):
        self.something = 'test'
    
    @property
    def a_something(self):
        return self.something

def test(this_is_a_parameter) -> bool:
    if this_is_a_parameter is not None:
        return True

```

```python
import pytest

from sr_app.test_utils.factories import ProductVersionFactory
from sr_release_notes.models import ReleaseNotes

@pytest.mark.django_db
def test_product_version_creates_release_notes():
    assert ReleaseNotes.objects.count() == 0
    product_version = ProductVersionFactory()
    assert ReleaseNotes.objects.count() == 1
    assert product_version.releasenotes is not None
    assert product_version.releasenotes.product_version is product_version
    product_version.save()
    assert ReleaseNotes.objects.count() == 1
    assert product_version.releasenotes is not None
    'test'
```

## Inline code

Ad amet irure est magna id mollit Lorem in do duis enim. Excepteur velit nisi magna ea pariatur pariatur ullamco fugiat deserunt sint non sint. Duis duis est `code in text` velit velit aute culpa ex quis pariatur pariatur laborum aute pariatur duis tempor sunt ad. Irure magna voluptate dolore consectetur consectetur irure esse. Anim magna `<strong>in culpa qui officia</strong>` dolor eiusmod esse amet aute cupidatat aliqua do id voluptate cupidatat reprehenderit amet labore deserunt.
