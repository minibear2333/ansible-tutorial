# Usage

.. _installation:

## Installation

To use Lumache, first install it using pip:

```shell
   (.venv) $ pip install lumache
```

## Creating recipes

To retrieve a list of random ingredients,
you can use the `lumache.get_random_ingredients()` function:

.. autofunction:: lumache.get_random_ingredients

The `kind` parameter should be either `"meat"`, `"fish"`,
or `"veggies"`. Otherwise, :py:func:`lumache.get_random_ingredients`
will raise an exception.


.. autoexception:: lumache.InvalidKindError

For example:

```bash
>>> import lumache
>>> lumache.get_random_ingredients()
['shells', 'gorgonzola', 'parsley']
```
