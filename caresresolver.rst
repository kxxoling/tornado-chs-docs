``tornado.platform.caresresolver`` --- 使用 C-Ares 实现的异步 DNS 分解器（Resolver）
================================================================================

.. module:: tornado.platform.caresresolver

该模块包含一个使用 c-ares 库（及其封装 ``pycares``）实现的 DNS 分解器T。

.. py:class:: CaresResolver

    基于 c-ares 的域名分解器。

    它是一个非阻塞、非线性的分解器，它的输出结果可能与系统分解器不一致，但在线程不可使用的非阻塞环境下使用它。

    c-ares fails to resolve some names when ``family`` is ``AF_UNSPEC``,
    因此仅仅推荐在 ``AF_INET`` 环境（比如 IPv4）下使用。``tornado.simple_httpclient`` 中默认如此，
    其它库的默认环境可能是 ``AF_UNSPEC``。
