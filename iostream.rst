``tornado.iostream`` --- 非阻塞 socket 相关封装
=====================================================================

.. automodule:: tornado.iostream

   基类
   ----------

   .. autoclass:: BaseIOStream

   主要接口
   ^^^^^^^^^^^^^^

   .. automethod:: BaseIOStream.write
   .. automethod:: BaseIOStream.read_bytes
   .. automethod:: BaseIOStream.read_until
   .. automethod:: BaseIOStream.read_until_regex
   .. automethod:: BaseIOStream.read_until_close
   .. automethod:: BaseIOStream.close
   .. automethod:: BaseIOStream.set_close_callback
   .. automethod:: BaseIOStream.closed
   .. automethod:: BaseIOStream.reading
   .. automethod:: BaseIOStream.writing
   .. automethod:: BaseIOStream.set_nodelay

   Methods for subclasses
   ^^^^^^^^^^^^^^^^^^^^^^

   .. automethod:: BaseIOStream.fileno
   .. automethod:: BaseIOStream.close_fd
   .. automethod:: BaseIOStream.write_to_fd
   .. automethod:: BaseIOStream.read_from_fd
   .. automethod:: BaseIOStream.get_fd_error

   实现
   ---------------

   .. autoclass:: IOStream
      :members:

   .. autoclass:: SSLIOStream
      :members:

   .. autoclass:: PipeIOStream
      :members:

   异常
   ----------

   .. autoexception:: StreamBufferFullError
   .. autoexception:: StreamClosedError
   .. autoexception:: UnsatisfiableReadError
