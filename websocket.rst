``tornado.websocket`` --- 与浏览器之间的双向交流
====================================================================

.. automodule:: tornado.websocket

   .. autoclass:: WebSocketHandler

   事件 handler
   --------------

   .. automethod:: WebSocketHandler.open
   .. automethod:: WebSocketHandler.on_message
   .. automethod:: WebSocketHandler.on_close
   .. automethod:: WebSocketHandler.select_subprotocol

   输出
   ------

   .. automethod:: WebSocketHandler.write_message
   .. automethod:: WebSocketHandler.close

   配置
   -------------

   .. automethod:: WebSocketHandler.allow_draft76
   .. automethod:: WebSocketHandler.get_websocket_scheme
   .. automethod:: WebSocketHandler.set_nodelay

   其它
   -----

   .. automethod:: WebSocketHandler.async_callback
   .. automethod:: WebSocketHandler.ping
   .. automethod:: WebSocketHandler.on_pong
   .. autoexception:: WebSocketClosedError


   Client-side support
   -------------------

   .. autofunction:: websocket_connect
   .. autoclass:: WebSocketClientConnection
       :members:
