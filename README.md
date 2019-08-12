### flake8
---
https://github.com/PyCQA/flake8

https://pypi.org/project/flake8/

```py
// tests/integration/test_api_legacy.py
""" """
from flake8.api import legacy

def test_legacy_api(tmpdir):
  """ """
  with tmpdir.as_wd():
    t_py = tmpdir.join('t.py')
    t_py.write('import os # unsed import\n')
    
    style_guide = legacy.get_style_guide()
    report = style_guide.check_files([t_py.strpath])
    assert report.total_errors == 1

```

```
```

```
```


