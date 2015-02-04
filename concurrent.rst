``tornado.concurrent`` --- Work with threads and futures
========================================================

.. automodule:: tornado.concurrent
    :members:
    :exclude-members: Future, TracebackFuture

    .. autoclass:: Future

    消费者方法
    ^^^^^^^^^^^^^^^^

    .. automethod:: Future.result
    .. automethod:: Future.exception
    .. automethod:: Future.exc_info
    .. automethod:: Future.add_done_callback
    .. automethod:: Future.done
    .. automethod:: Future.running
    .. automethod:: Future.cancel
    .. automethod:: Future.cancelled

    生产者方法
    ^^^^^^^^^^^^^^^^

    .. automethod:: Future.set_result
    .. automethod:: Future.set_exception
    .. automethod:: Future.set_exc_info
