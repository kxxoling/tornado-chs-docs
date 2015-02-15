``tornado.ioloop`` --- 主事件循环
======================================

.. automodule:: tornado.ioloop

   IOLoop objects
   --------------

   .. autoclass:: IOLoop

   运行 IOLoop
   ^^^^^^^^^^^^^^^^^

   .. automethod:: IOLoop.current
   .. automethod:: IOLoop.make_current
   .. automethod:: IOLoop.instance
   .. automethod:: IOLoop.initialized
   .. automethod:: IOLoop.install
   .. automethod:: IOLoop.clear_instance
   .. automethod:: IOLoop.start
   .. automethod:: IOLoop.stop
   .. automethod:: IOLoop.run_sync
   .. automethod:: IOLoop.close

   I/O 事件
   ^^^^^^^^^^

   .. automethod:: IOLoop.add_handler
   .. automethod:: IOLoop.update_handler
   .. automethod:: IOLoop.remove_handler

   回调与超时
   ^^^^^^^^^^^^^^^^^^^^^^

   .. automethod:: IOLoop.add_callback
   .. automethod:: IOLoop.add_callback_from_signal
   .. automethod:: IOLoop.add_future
   .. automethod:: IOLoop.add_timeout
   .. automethod:: IOLoop.call_at
   .. automethod:: IOLoop.call_later
   .. automethod:: IOLoop.remove_timeout
   .. automethod:: IOLoop.spawn_callback
   .. automethod:: IOLoop.time
   .. autoclass:: PeriodicCallback
      :members:

   调试与事件处理
   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^

   .. automethod:: IOLoop.handle_callback_exception
   .. automethod:: IOLoop.set_blocking_signal_threshold
   .. automethod:: IOLoop.set_blocking_log_threshold
   .. automethod:: IOLoop.log_stack

   Methods for subclasses
   ^^^^^^^^^^^^^^^^^^^^^^

   .. automethod:: IOLoop.close_fd
   .. automethod:: IOLoop.split_fd
