``tornado.escape`` --- Escaping and string manipulation
=======================================================

.. automodule:: tornado.escape

   Escaping functions
   ------------------

   .. autofunction:: xhtml_escape
   .. autofunction:: xhtml_unescape

   .. autofunction:: url_escape
   .. autofunction:: url_unescape

   .. autofunction:: json_encode
   .. autofunction:: json_decode

   Byte/unicode 转换
   -----------------
   这些函数在 Tornado 内部广泛使用，但对于大多数应用来说并不直接需要。注意：这些函数有些复杂，
   主要是 Tornado 需要同时支持 Python 2 和 Python 3.

   .. autofunction:: utf8
   .. autofunction:: to_unicode
   .. function:: native_str

      将 byte 或者 unicode 字符串转换为 `str` 类型，向当于 Python 2 中的 `utf8` 
      或者 Python 3 中的 `to_unicode`。

   .. autofunction:: to_basestring

   .. autofunction:: recursive_unicode

   Miscellaneous functions
   -----------------------
   .. autofunction:: linkify
   .. autofunction:: squeeze
