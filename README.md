<h1 align="center">JD-HAPPY<h1>

### 前言

代码实现基于[jd-autobuy](https://github.com/Adyzng/jd-autobuy)

京东有代下单服务，但是会有限制，遇到些商品无法使用代下单，只能收到到货提醒，所以想实现个自动下单功能，以免剁手不成，悔恨不已

但是基本上该功能是没有什么卵用的，只不过看着简单用node实现了一下，坑比较少，毕竟前人栽树后人乘凉 :smile:

- [X] 扫码登录
- [X] 根据地区查询商品库存
- [ ] 库存>0时自动下单

```
   -------------------------------------
                请求扫码
   -------------------------------------

   二维码未扫描 ，请扫描二维码
   二维码未扫描 ，请扫描二维码
   请手机客户端确认登录
   请手机客户端确认登录
   请手机客户端确认登录
   扫码成功，正在登录
   登录成功

   商品详情------------------------------
   时间：2017-10-26 19:57:51
   商品名：英特尔（Intel） i7 8700K 酷睿六核 盒装CPU处理器
   价格：3999.00
   状态：无货
   连接：http://item.jd.com/5008395.html
```

### 使用

```bash
npm install

node index.js -a 2_2830_51810_0 -g 5008395
```

### 帮助
```
$ node index.js

Usage: node index.js -a 地区编号 -g 商品编号

选项：
    --version       显示版本号      [布尔]
    -a, --area      地区编号        [必需]
    -g, --good      商品编号        [必需]
    -h, --help      显示帮助信息     [布尔]
    -t, --time      查询间隔ms      [必需]    [默认值: "1000"]

示例：
    node index.js -a 2_2830_51810_0 -g 5008395

缺少这些必须的选项：a, g
```
