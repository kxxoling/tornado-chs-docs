``tornado.auth`` --- 第三方 OpenID 或者 OAuth 登录
============================================================

.. automodule:: tornado.auth

   Common protocols
   ----------------

   这些类都是对 OpenID 或者 OAuth 标准的实现，想要在特定网站上使用，需要进一步实现它，
   其定制程度因网站可能大不相同，不过大多数情况只需要重载类属性（由于历史原因，以下划线开头）即可。

   .. autoclass:: OpenIdMixin
      :members:

   .. autoclass:: OAuthMixin

      .. automethod:: authorize_redirect
      .. automethod:: get_authenticated_user
      .. automethod:: _oauth_consumer_token
      .. automethod:: _oauth_get_user_future
      .. automethod:: get_auth_http_client

   .. autoclass:: OAuth2Mixin
      :members:

   Google
   ------

   .. autoclass:: GoogleMixin
      :members:
   
   .. autoclass:: GoogleOAuth2Mixin
      :members:

   Facebook
   --------

   .. autoclass:: FacebookGraphMixin
      :members:

   .. autoclass:: FacebookMixin
      :members:

   Twitter
   -------

   .. autoclass:: TwitterMixin
      :members:

   FriendFeed
   ----------

   .. autoclass:: FriendFeedMixin
      :members:

