``tornado.platform.asyncio`` --- ``asyncio`` 与 Tornado 之间的桥梁
=================================================================

.. module:: tornado.platform.asyncio

.. versionadded:: 3.2

该模块将 Tornado 与 Python 3.4 中引入（提供`独立下载 <https://pypi.python.org/pypi/asyncio>`_ ）
的 ``asyncio`` 相结合，这使得在同一个事件 IO 中使用这两个类库成为可能。

大多数应用应该在默认的 ``asyncio`` 事件循环之上使用 `AsyncIOMainLoop`，需要多线程
事件循环的可以使用`AsyncIOLoop` 来创建多个循环。

.. py:class:: AsyncIOMainLoop

    ``AsyncIOMainLoop`` 创建一个相当于现有 ``asyncio`` 循环（比如 ``asyncio.get_event_loop()`` 
    的返回值）的 `.IOLoop`。    推荐用法：

        from tornado.platform.asyncio import AsyncIOMainLoop
        import asyncio
        AsyncIOMainLoop().install()
        asyncio.get_event_loop().run_forever()

.. py:class:: AsyncIOLoop

    ``AsyncIOLoop`` 是一个运行于 ``asyncio`` 事件循环之上的 `.IOLoop` ，该类遵循 Tornado 
    的惯用语法来创建新的 ``IOLoops``，这些循环对于默认的事件循环来说并不是必要的。
    推荐用法：

        from tornado.ioloop import IOLoop
        IOLoop.configure('tornado.platform.asyncio.AsyncIOLoop')
        IOLoop.instance().start()
