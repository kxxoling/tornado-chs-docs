``tornado.gen`` --- 简化异步代码
===============================

.. automodule:: tornado.gen

   装饰器
   ------

   .. autofunction:: coroutine

   .. autofunction:: engine

   Yield points
   ------------

   这些类的实例可能会在生成器内部的 yield 表达式中使用，`Futures <.Future>` 同样可以被 yield，
   其结果方法会在合适的时候被调用。
   另外，
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

   其它类
   -----

   .. autoexception:: Return

   .. class:: Arguments

      回调函数（关键词）参数超过一个的 yield 表达式的结果。

      `Arguments` 对象同时也是 `collections.namedtuple` 对象，既可以被当作 ``(args, kwargs)`` 
      这样的元组，也可以被当作拥有 ``args`` 和 ``kwargs`` 参数的对象。
