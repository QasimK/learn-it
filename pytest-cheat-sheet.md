# pytest 
Remember to set onupdate and ondelete cascades on ForeignKeys.test cheat-sheet

```
--version     # shows where pytest was imported from
--fixtures    # show available builtin function arguments
-h | --help   # show help on command line and config file options

# With Django the setup time may be quite long (Don't do this normally? Do this normally!)
--nomigrations

# (Exception information is stored on sys.last_value, sys.last_type and sys.last_traceback.)
--pdb               # Open pdb on failure [Install PDB++: pdbpp]
-s | --capture=no   # Allow use of ipdb in code

-x            # Stop after first failure
--maxfail=3   # Stop after 3 failures

--lf          # Run only last failed tests (otherwise, all)
--ff          # Run last failed tests first, then the others

-l | --showlocals # Show local variables

--tb=long     # the default informative traceback formatting
--tb=native   # the Python standard library formatting
--tb=short    # a shorter traceback format
--tb=line     # only one line per failure

--durations=10  # Slowest ten tests

# -r<chars>: Show reasons for (f)ailed, (E)rror, (s)kipped, (x)failed, (X)passed, (w)arnings (pytest)
-rs

# Running particular tests
--ignore=tests/       # Ignore folder or file, you can do this multiple times

# Only run tests matching the "string expression", e.g. "MyClass and not method"
# Combine -k with the below filters
py.test -k stringexpr

# Run a module, or a folder
py.test test_mod.py
py.test somepath

# Run a method or a class
py.test test_mod.py::test_func
py.test test_mod.py::TestClass::test_method

# Run a particular fixture parameter
py.test test_mod.py::TestClass::test_method[param1-param2]
py.test -k "test_method and param1 and param2"

--pyargs      # Allow specifying a path via python module import format

# Ignore a plugin
-p no:randomly

# Creating result files
--junitxml=path
--resultlog=path      # Plain text
--pastebin=failed|all # Upload to a pastebin service
```

https://pytest.org/latest/usage.html

## setup.cfg

```
[tool:pytest]
filterwarnings =
    error::pandas.core.common.SettingWithCopyWarning
```
