``tornado.escape`` --- 编码以及字符串操作
=======================================================

.. automodule:: tornado.escape

   编码函数
   ------------------

   .. autofunction:: xhtml_escape
   .. autofunction:: xhtml_unescape

   .. autofunction:: url_escape
   .. autofunction:: url_unescape

   .. autofunction:: json_encode
   .. autofunction:: json_decode

   Byte/unicode 转换
   ------------------------
   这些函数在 Tornado 中广泛使用，但对于绝大多数其它应用来说不可直接使用。
   注意：为了同时支持 Python 2 和 3，这些函数写得颇为错综复杂。

   .. autofunction:: utf8
   .. autofunction:: to_unicode
   .. function:: native_str

      将 byte 或者 unicode 类型的字符串转换为 `str`，相当于 Python 2 中的
      `utf8` 和 Python 3 中的 `to_unicode`。

   .. autofunction:: to_basestring

   .. autofunction:: recursive_unicode

   其它函数
   -----------------------
   .. autofunction:: linkify
   .. autofunction:: squeeze
