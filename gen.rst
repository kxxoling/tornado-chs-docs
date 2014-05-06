``tornado.gen`` --- 简化异步代码
===============================

.. automodule:: tornado.gen

   装饰器
   ------

   .. autofunction:: coroutine

   .. autofunction:: engine

   Yield points
   ------------

   这些类的实例可能会在生成器内部的 yield 表达式中使用，
   Instances of the following classes may be used in yield expressions
   in the generator.  `Futures <.Future>` may be yielded as well;
   their result method will be called automatically when they are
   ready.  Additionally, lists of any combination of these objects may
   be yielded; the result is a list of the results of each yield point
   in the same order. Yielding dicts with these objects in values will
   return dict with results at the same keys.

   .. autoclass:: Task

   .. autoclass:: Callback

   .. autoclass:: Wait

   .. autoclass:: WaitAll

   .. autoclass:: YieldPoint
      :members:

   .. autofunction:: with_timeout
   .. autoexception:: TimeoutError

   .. autofunction:: maybe_future

   Other classes
   -------------

   .. autoexception:: Return

   .. class:: Arguments

      The result of a yield expression whose callback had more than one
      argument (or keyword arguments).

      The `Arguments` object is a `collections.namedtuple` and can be
      used either as a tuple ``(args, kwargs)`` or an object with attributes
      ``args`` and ``kwargs``.
