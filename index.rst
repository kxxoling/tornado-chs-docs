.. title:: Tornado Web Server

.. meta::
    :google-site-verification: g4bVhgwbVO1d9apCUsT-eKlApg31Cygbp8VGZY8Rf0g

|Tornado Web Server|
====================

.. |Tornado Web Server| image:: tornado.png
    :alt: Tornado Web Server

`Tornado <http://www.tornadoweb.org>`_ 既是一个 Python web 框架，也是一个异步网络库，
最初由 `FriendFeed <http://friendfeed.com>`_ 开发。 通过使用非阻塞式的网络 I/O，
Tornado 能够应对数以万计的网络连接，非常适合
`long polling <http://en.wikipedia.org/wiki/Push_technology#Long_polling>`_ 以及 
`WebSockets <http://en.wikipedia.org/wiki/WebSocket>`_ 这样需要长时间与用户保持连接状态
的技术和应用。

升级须知
-------

对于 Tornado 3.2，如果要运行在 Python 2 环境中，则必须安装 
`backports.ssl_match_hostname <https://pypi.python.org/pypi/backports.ssl_match_hostname>`_。
如果你使用 ``pip`` 或者 ``easy_install`` 包管理器，它将会被自动安装.

快速链接
-------

* :doc:`Documentation <documentation>`
* |Download current version|: :current_tarball:`z` (:doc:`release notes <releases>`)
* `Source (github) <https://github.com/facebook/tornado>`_
* `Mailing list <http://groups.google.com/group/python-tornado>`_
* `Stack Overflow <http://stackoverflow.com/questions/tagged/tornado>`_
* `Wiki <https://github.com/facebook/tornado/wiki/Links>`_

.. |Download current version| replace:: Download version |version|

Hello, world
------------

这是一个简单的 Tornado “Hello, world” 的例子 ::

    import tornado.ioloop
    import tornado.web

    class MainHandler(tornado.web.RequestHandler):
        def get(self):
            self.write("Hello, world")

    application = tornado.web.Application([
        (r"/", MainHandler),
    ])

    if __name__ == "__main__":
        application.listen(8888)
        tornado.ioloop.IOLoop.instance().start()

该例子并未使用任何 Tornado 的异步特性，想要感受 Tornado 异步开发可以看看下面这个例子：
`simple chat room <https://github.com/facebook/tornado/tree/master/demos/chat>`_.

安装
------------

**自动安装**::

    pip install tornado

Tornado 已经在 `PyPI <http://pypi.python.org/pypi/tornado>`_ 目录中，因此你可以使用
 ``pip`` 或者 ``easy_install``安装。 注意：Tornado 的源代码中包括了 demo 应用，
但通过该方法安装则没有，所以也许你有必要单独下载 Tornado 的源码包。

**手动安装**: Download :current_tarball:`z`:

.. parsed-literal::

    tar xvzf tornado-|version|.tar.gz
    cd tornado-|version|
    python setup.py build
    sudo python setup.py install

Tornado 的源代码托管在 `GitHub <https://github.com/facebook/tornado>`_ 上。

**安装依赖**: Tornado 可以运行于 Python 2.6, 2.7, 3.2, 3.3, 3.4 等版本，在所有版本中都依赖 
`certifi <https://pypi.python.org/pypi/certifi>`_ ，在 Python 2 环境下依赖 
`backports.ssl_match_hostname <https://pypi.python.org/pypi/backports.ssl_match_hostname>`_ 。
（在使用 ``pip`` 或者 ``easy_install`` 时这些都将会自动安装。）. 
Tornado 的某些特性和功能还会产生以下依赖：

* `unittest2 <https://pypi.python.org/pypi/unittest2>`_ is needed to run
  Tornado's test suite on Python 2.6 (it is unnecessary on more recent
  versions of Python)
* `concurrent.futures <https://pypi.python.org/pypi/futures>`_ is the
  recommended thread pool for use with Tornado and enables the use of
  `~tornado.netutil.ThreadedResolver`.  It is needed only on Python 2;
  Python 3 includes this package in the standard library.
* `pycurl <http://pycurl.sourceforge.net>`_ is used by the optional
  ``tornado.curl_httpclient``.  Libcurl version 7.18.2 or higher is required;
  version 7.21.1 or higher is recommended.
* `Twisted <http://www.twistedmatrix.com>`_ may be used with the classes in
  `tornado.platform.twisted`.
* `pycares <https://pypi.python.org/pypi/pycares>`_ is an alternative
  non-blocking DNS resolver that can be used when threads are not
  appropriate.
* `Monotime <https://pypi.python.org/pypi/Monotime>`_ adds support for
  a monotonic clock, which improves reliability in environments
  where clock adjustments are frequent.  No longer needed in Python 3.3.

**平台**: 理论上，Tornado 可以运行于任何类 Unix 平台，不过为了最佳的性能和扩展性，
推荐使用（支持 ``epoll`` 的） Linux 和（支持 ``kqueue`` 的）BSD 系统作为生产环境的部署系统。
（虽然 Mac OS X 也起源于 BSD 并且支持 kqueue，但其网络性能并不佳，因此仅仅推荐作为开发环境。）
虽然没有官方配置，不过 Tornado 也支持 Windows，同样仅推荐作为开发环境使用。

讨论和支持
---------

你可以在 `Tornado 开发者邮件列表 <http://groups.google.com/group/python-tornado>`_
中参与讨论，在 `GitHub issue tracker <https://github.com/facebook/tornado/issues>`_ 
上提交 bug。其它资源参见 `Tornado wiki <https://github.com/facebook/tornado/wiki/Links>`_。

Tornado 来自于 `Facebook's open source technologies <http://developers.facebook.com/opensource/>`_ 
遵循 `Apache License, Version 2.0 <http://www.apache.org/licenses/LICENSE-2.0.html>`_ 协议开源。

本站所有文档遵循 `Creative Commons 3.0 <http://creativecommons.org/licenses/by/3.0/>`_ 共享协议。
中文文档遵循 `Creative Commons 3.0 BY-NC-SA<http://creativecommons.org/licenses/by-nc-sa/3.0/deed.zh>`_ 共享协议，请勿用于商业用途。

.. toctree::
   :hidden:

   documentation
