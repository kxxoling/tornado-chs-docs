``tornado.options`` --- 命令行解析
============================================

.. automodule:: tornado.options



   全局函数
   ----------------

   .. autofunction:: define

   .. py:data:: options

       全局的 options 对象，所有配置属性都在这个对象上。


   .. autofunction:: parse_command_line
   .. autofunction:: parse_config_file
   .. autofunction:: print_help(file=sys.stderr)
   .. autofunction:: add_parse_callback
   .. autoexception:: Error

   配置解析
   ------------------

   .. autoclass:: OptionParser
      :members:
