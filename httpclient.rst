``tornado.httpclient`` --- 异步 HTTP 客户端
==========================================

.. automodule:: tornado.httpclient

   HTTP 客户端接口
   --------------

   .. autoclass:: HTTPClient
      :members:

   .. autoclass:: AsyncHTTPClient
      :members:

   Request 对象
   ------------
   .. autoclass:: HTTPRequest
      :members:
   
   Response 对象
   -------------
   .. autoclass:: HTTPResponse
      :members:

   Exceptions
   ----------
   .. autoexception:: HTTPError
      :members:

   命令行接口
   ---------

   该模块使用 Tornado HTTP 客户端实现了一个简单的命令行请求 URL 的接口。示例：

      # 请求 URL 并输出请求体
      python -m tornado.httpclient http://www.google.com

      # 仅仅打印请求头信息
      python -m tornado.httpclient --print_headers --print_body=false http://www.google.com
