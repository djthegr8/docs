page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.compat.v1.assign_add


<table class="tfo-notebook-buttons tfo-api" align="left">

<td>
  <a target="_blank" href="https://github.com/tensorflow/tensorflow/tree/r2.0/tensorflow/python/ops/state_ops.py#L167-L195">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td></table>



Update `ref` by adding `value` to it.

``` python
tf.compat.v1.assign_add(
    ref,
    value,
    use_locking=None,
    name=None
)
```



<!-- Placeholder for "Used in" -->

This operation outputs "ref" after the update is done.
This makes it easier to chain operations that need to use the reset value.
Unlike <a href="../../../tf/math/add"><code>tf.math.add</code></a>, this op does not broadcast. `ref` and `value` must have
the same shape.

#### Args:


* <b>`ref`</b>: A mutable `Tensor`. Must be one of the following types: `float32`,
  `float64`, `int64`, `int32`, `uint8`, `uint16`, `int16`, `int8`,
  `complex64`, `complex128`, `qint8`, `quint8`, `qint32`, `half`. Should be
  from a `Variable` node.
* <b>`value`</b>: A `Tensor`. Must have the same shape and dtype as `ref`. The value to
  be added to the variable.
* <b>`use_locking`</b>: An optional `bool`. Defaults to `False`. If True, the addition
  will be protected by a lock; otherwise the behavior is undefined, but may
  exhibit less contention.
* <b>`name`</b>: A name for the operation (optional).


#### Returns:

Same as "ref".  Returned as a convenience for operations that want
to use the new value after the variable has been updated.