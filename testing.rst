``tornado.testing`` --- 提供异步代码的测试支持
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

   日志管理
   ----------------------

   .. autoclass:: ExpectLog
      :members:

   .. autoclass:: LogTrapTestCase
      :members:

   测试运行器
   -----------

   .. autofunction:: main

   辅助方法
   ----------------

   .. autofunction:: bind_unused_port

   .. autofunction:: get_unused_port

   .. autofunction:: get_async_test_timeout
