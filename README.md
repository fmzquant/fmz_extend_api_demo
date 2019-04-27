# 零成本快速打造你自己专属的多用户量化交易平台

> 本范例项目展示了使用简单的HTML页面、python服务端程序 构建一个功能强大的量化交易平台。

长期以来，量化交易平台 因其涉及技术种类多（前端，后台，数据库，回测系统，网络访问 等等），跨学科（金融、数学、计算机编程等），项目设计周期长，维护成本高 等诸多因素。造成 一些有志于 在程序化交易 、量化交易 上大展身手的 投资、资产管理团队，交易工作室，宽客爱好者等 中小交易者 望而却步！

术业专攻一直是FMZ(发明者量化) 秉承的 发展理念，如今是信息、技术 飞速发展的时代。速度几乎决定着 一个项目的成败，一次投资的成败。只有更高的效率才是制胜的根本。

FMZ 对于 技术底层做出了强有力的支持，只需使用 FMZ 的 扩展 API 接口，就可以把你从繁杂的计算机技术、各个学科专业知识等问题中解放出来。

仅仅只需要开发一个  WEB站点 、APP 或者 微信小程序  对接 FMZ 的技术底层 ，就可以实现一个专业的量化交易平台。

- ### 嵌入现有系统

  根据本DEMO项目可以参考编写服务端代码，增加前端页面以用来嵌入现有论坛，博客，社区等系统。
  以实现灵活接入现有用户群体，并且现有用户群体完全体验不到FMZ的底层技术支持，用户使用更加简洁，易操作。

- ### 支持市场

  - CTP 商品期货 （上期所、郑商所、大商所、中金所）
  - 易盛外盘 (CME, CBOT等主流国外期货交易所)
  - 全球交易30多个区块链资产交易平台

- ### 打造属于自己的量化平台

  - 高度自由的策略设计

    使用 Python 、JavaScript 、C++ 语言编写 量化交易策略，自由定制，可以在量化交易的世界天马行空般的实现自己的交易思路。

  - 强大高效的回测系统

    从此再也不用辛苦收集数据，本地回测系统引擎 只用一个命令轻松配置，链接：https://github.com/fmzquant/backtest_python

  - 精简的架构
  
    只用编写几个 前端页面，一个HTTP服务端程序，即可轻松搭建。
    
- ### DEMO项目
  
  - 名称：FMZ演示如何使用FMZ的扩展API打造自己的资产管理量化平台
  
  - 本DEMO项目 安装
    
    - 首先 clone 本DEMO项目

      ```
      git clone https://github.com/fmzquant/fmz_extend_api_demo.git 
      ```
    
      ![alt](https://www.fmz.com/upload/asset/c36383238f93ca220887b7d85e1a611ba3a99007.png)
    
    - 切换到这个 目录，执行 pip 安装

      ![alt](https://www.fmz.com/upload/asset/6074daa004ede3ce30eae01c0c7208a5db9708f5.png)
    
      ```
      pip install -r requirements.txt 
      ```
      
      ![alt](https://www.fmz.com/upload/asset/c4bdf77264d876f73dd628811865f484bb0992b7.png)
      
      注意：如果提示 Permission denied ， 需要 sudo pip install -r requirements.txt 这样执行 pip ，根据要求输入操作系统密码。
    
    - 安装完成后，配置一下 服务端程序 要使用的 FMZ 账号的 API KEY
      
      > FMZ 扩展 API KEY 使用 详见 FMZ API 文档：https://www.fmz.com/api#FMZ%20%E5%B9%B3%E5%8F%B0%E6%89%A9%E5%B1%95API
      
      创建 FMZ API KEY
      
      ![alt](https://www.fmz.com/upload/asset/28b430e0104147594a264d838838735db4114d9b.png)
    
      把 API KEY 写入 ，本DEMO 的 app.py 服务端程序。
      
      ![alt](https://www.fmz.com/upload/asset/426bb928998875dd0e7fbf5f43fed546a3ac2f2f.png )

  - 本DEMO项目 服务端运行命令

    ```
    python app.py
    ```
    
    - 运行显示：
      ![alt](https://www.fmz.com/upload/asset/60bb0b2e41e31d7354a461a63300841c24658a7f.png)
      运行服务端程序后，在浏览器打开本地页面：http://127.0.0.1:5000
      ![alt](https://www.fmz.com/upload/asset/6e179f4b1dd680dbcc4f8b96d189f289d780e853.png)
      
    - 测试注册页面
    
      ![alt](https://www.fmz.com/upload/asset/83b09142e42ae0ff4d9c8f789a771fb99c1f2d48.png)
      本项目 DEMO 量化平台 已经运行起来了，注册好 这个测试平台的 账号（储存在本地数据的），登录进去 配置 作为这个平台用户的 交易所API KEY。
      
      ![alt](https://www.fmz.com/upload/asset/d38f7155af07c0231dcdf632887585042268d058.png)
      ![alt](https://www.fmz.com/upload/asset/2c6f6c8021a8d69e357a2e0fe538f3a919f3f8b4.png)
     
      现在配置好了如图：
    
      ![alt](https://www.fmz.com/upload/asset/d7206a4113e2974683a614f455be8dc4fbce9f43.png)

      页面显示的三个策略 仅仅是 UI显示，这些还需要 资产管理量化平台 的管理者 具体设计实现，这里只做演示用。
    
    - 配置一个测试策略
    
      本DEMO项目 ，服务端 会检测到 “一键启动” 按钮按下，触发搜索FMZ账号中 包含 "main" 关键字的策略，使用该策略 绑定机器人运行。
      所以我们先创建一个 名为 main Test profit 的策略
      
      main Test profit 策略代码如下：
      
      ```javascript
      function main() {
          while(true) {
              LogProfit(Math.random()*100);
              Sleep(1000);
          }
      }
      ```
      
      ![alt](https://www.fmz.com/upload/asset/52792c59a5db460c0bdf5a229803b92f92b8cb07.png)
      
      编辑代码后，点击保存。
      注意：在运行前必须确保有一个托管者在线，认识托管者：https://www.fmz.com/bbs-topic/463 。

    - 点击 “一键启动” 按钮， 会自动创建一个 机器人 运行，这个机器人 只会 随机输出数值作为收益数值显示出来。
    
      可以看到 在FMZ的控制中心上显示 出一个 新创建的机器人：
      ![alt](https://www.fmz.com/upload/asset/61ff0f2319aaeb4138e43de626b2a0cf6b357435.png)
    
      DEMO 网页上也显示出对应的 随机数值
      ![alt](https://www.fmz.com/upload/asset/73bb8cde3237d39e927edcaf3cf7a6187d174c1d.png)
    
    - 在FMZ 上运行的机器人 由 appId 识别 当前DEMO平台 登录的 用户
      
      ![alt](https://www.fmz.com/upload/asset/0d9a9751442b9dc78ba2a0c3b3bc2347c5cd8ab9.png)
      
      ```python
      def robot_run(robotId, appId, exchanges):
          strategyId = -1
          # 从策略库里选出一个包含main字符串的策略运行, 也可以预定义
          for ele in api("GetStrategyList")['data']['result']['strategies']:
              if 'main' in ele['name']:
                  strategyId = ele['id']
          if strategyId < 0:
              raise u"not found strategy"
          settings = {
                  "name":"robot for %s" % (appId, ),
                  "args": [], # our custom arguments for this strategey
                  "appid": appId, # 为该机器人设置标签,关联到本用户
                  "period": 60,
                  "strategy": strategyId,
                  "exchanges": [],
                  }
          for e in exchanges:
              settings["exchanges"].append({"eid": e.eid, "pair": get_default_stock(e.eid), "meta" :{"AccessKey": e.accessKey, "SecretKey": e.secretKey}})
          if robotId > 0:
              return api('RestartRobot', robotId, settings)
          else:
              return api('NewRobot', settings)
      ```
      可以看到 代码中 settings 是创建 机器人的配置信息， appid 就是用来 标记用户的。
      
    - 一个简单的交易中心
    
      DEMO附带了一个简单的交易中心, 以帮助用户了解FMZ平台扩展API
      
      ![alt](https://www.fmz.com/upload/asset/05da54385c1518514b1de45c0a484a5015a895c3.png) 
      
