## To verify the version of vista thats running ##
Check the frame title of Vista. It should have a date that should match the version that you downloaded

For vscript type this in the vscript interactive shell and verify the version id date to match your expectation
```
>>> from vista.gui import VistaUtils
>>> print VistaUtils.getVersionId()
u'1.0-v03/17/2010'
```