TaobaoTopClient
===============

对淘宝TopSdk的简单修改


安装
----

    ```
    "require": {
        ...
        "elvis-bi/bq-wechat-sdk": "0.1.0Alpha"
        ...
    }
    ```
    php composer.phar update
    
    
使用
----

  $config = array(
    'appkey' => '...',
    'secretKey' => '...'
    );
    
  $topClient = new \TaobaoTopClient\TopClient($config);
  
  $shopGetRequest = $topClient->get('ShopGetRequest');
  $shopGetRequest->setNick('abc');
  $shopGetRequest->setFields('sid,cid,...');
  
  $shopData = $topClient->execute($shopGetRequest, $sessionKey);