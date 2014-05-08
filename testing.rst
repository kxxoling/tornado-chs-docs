``tornado.testing`` --- 异步代码的单元测试支持
==================================================================

.. automodule:: tornado.testing

   异步测试用例
   -----------------------

   .. autoclass:: AsyncTestCase
      :members:

   .. autoclass:: AsyncHTTPTestCase
      :members:

   .. autoclass:: AsyncHTTPSTestCase
      :members:

   .. autofunction:: gen_test

   控制日志输出
   ----------------------

   .. autoclass:: ExpectLog
      :members:

   .. autoclass:: LogTrapTestCase
      :members:

   Test runner
   -----------

   .. autofunction:: main

   Helper functions
   ----------------

   .. autofunction:: bind_unused_port

   .. autofunction:: get_unused_port

   .. autofunction:: get_async_test_timeout
