![](images/WEBRESOURCEb508fbdf09a046c1ab28a847a0d4dbe2image.png)

![](images/WEBRESOURCE38fb73479ee5477cb6317beafbf8305dimage.png)

几个要解释的点：

1. 基于内存存储的数据库，存储的事键值对

1. 原子性说明操作不会被中断，qps为10w+

1. 通过配置可以支持数据存储

![](images/WEBRESOURCEef6f1f3d6be24573992106d98362dc4eimage.png)

![](images/WEBRESOURCE4bc4762a39a24c40ac9f4aa6f330ca5dimage.png)

![](images/WEBRESOURCE51a5a9cf0c5945bea37024b79f512166image.png)

![](images/WEBRESOURCEe75d098e780b4bc29c19fd7845bb5eeeimage.png)

ttl key 可查看key的过期时间

keys *可查看所有的string类型的key

![](images/WEBRESOURCE0b1e6351f6924252bff2849176006e26image.png)

hgetall key 查看大key所有的属性值

![](images/WEBRESOURCE7d8e811e9e0b4eff9661387ea9327013image.png)

![](images/WEBRESOURCE5a11bbcee5e441a392d013ea1baf1987image.png)

lrange key 0 -1

![](images/WEBRESOURCE55dd8cc2233d4089a45f491952fd25c3image.png)

![](images/WEBRESOURCE8ec3ddf47ccb46f1b5026c5651ad6fe0image.png)

![](images/WEBRESOURCE7f6ceb8061a04999b85701e7bf708906image.png)

![](images/WEBRESOURCEb965a68cc6924296ae8ee5761c9fe6e7image.png)

![](images/WEBRESOURCE41bd7a9548b14680bf78e7f042c4b8d6image.png)

![](images/WEBRESOURCE6b016511cd584c68afdaa2fb3e335719image.png)

![](images/WEBRESOURCE316fd8af0a0f483fa26b35c7c33d4ac1image.png)

![](images/WEBRESOURCE8a9da2202adf46a68745e803b8169135image.png)

![](images/WEBRESOURCE155e913c35a24aeda6b65dfcabdf106dimage.png)

template可以直接注入的原理是：在springboot启动类中的autoconfig有关于redis的自动配置类

![](images/WEBRESOURCEaf366d583e6d424784acfaad54ba1f76image.png)

![](images/WEBRESOURCE41cef191d0604320bb7dab8a2210b4ccimage.png)

可以看到redisTemplate的自动配置

![](images/WEBRESOURCE0dc4b86d9d5a4a1289603a94f5cb4452image.png)

持久化机制

![](images/WEBRESOURCE9cc0189bd4534f4d87128ab1d3f66660image.png)

![](images/WEBRESOURCE99893a5b192b4bdd9d76ea709bfa24acimage.png)

![](images/WEBRESOURCE46184e11c6984b7499edbf91054c8867image.png)

![](images/WEBRESOURCE4bad0521062642c3b3444a402901fac1image.png)

![](images/WEBRESOURCE7d701e25fccf4faa9b2677c888742a44image.png)

![](images/WEBRESOURCE1708fe3c03fc469abb4cbd0ad7c58cfaimage.png)