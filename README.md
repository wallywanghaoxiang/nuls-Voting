# 基于nuls的投票系统 nuls-voting

## 核心功能
模块实现的核心业务是在nuls上建立投票选举事件，应征候选人，并让选举人对候选人进行投票，最后公布投票选举结果

## Core functions

 1. 为每个投票选举事件建立独立的链
 
 2. 为每个应征的候选人指定一个唯一不重复的投票地址
 
 3. 给每个投票人发放选票(某个数量的token)
 
 4. 在应征候选人阶段，候选人可以上传自己的介绍和作品链接。投票开始前，截止应征作品修改,将会把加密后的候选人应征作品内容存储在链上和节点文件系统中
 
 5. 当投票开始后，投票人可以把手里的选票投给喜欢的候选人
 
 6. 当投票结束后，投票选举结果向所有用户公示
 
 注：投票选举活动发起人空投给每个选举人选票将会产生的费用，为了控制整体费用，可以加入智能合约进行选举人资格筛选。

 
## 次要功能点

 1. 查看投票选举事件列表
 
 2. 查看候选人列表
 
 3. 投票开始后查看每个候选人的得票情况
 
## General design
  1. roles
  
     admin：
     
     vote hosts：
     
        create and manage the vote events
        
     candidates：
     
         the people who have achievement to be vote
         
     attends：
     
        vote for the candidates
        
        
  2. sinario
     
     vote host regist and login create a new vote event( title,description,Electoral nominations start time ,end time,vote start time and so on)
     
     during Electoral nominations time
     
     candidates  regist and login upload his achievement
     
     when vote starts
     
     attends  regist and login get free tickes ,vote for candidates
     
     when vote ehds
     
     vote host get Voting statistics,and all uses can see the result
     
  3. functions and api
  
    public functions
    
      register and login
      
      001.  api 手机短信认证
      
      002.  api 注册
      
      003.  api 登录
       
       
    public square show all vote events
    
      101. api 取得所有选举事件
     
    all votes past comming and in the furch
    
      102. api 按时间检索选举事件
     
    personal center(ID card identification)
    
      201. api 实名认证
     
     my attend(我参加的选举)votes and my host(我举办的选举)votes.  
     
      202. api 按照我参加的和我举办的 取得选举
     
     create new votes 
     
      301. api 新建选举
     
     to be candidates
     
      401. api 参加候选人报名资料上传(或者填写推荐人/推荐码)
      
     vote 
      
      501. api 投票开始候选人成果公示
      
      502. api voteing 选民投票
        
     
    acccecs and get tickes for vote
      
      601. api vote host get the Voting statistics
    
    vote result
    
      701. api all the user get the result for this vote event
     
 
前端设计原型：
    https://teymyp.axshare.com
    密码：wanghaoxiang

与后端交互api设计：
apidoc(todo): https://segmentfault.com/a/1190000017145798

## 开发/测试环境搭建步骤：

1. restfulapi环境：https://github.com/nuls-io/nuls-v2/blob/release/module/nuls-api/documents/nuls-api_RESTFUL.md

2. 智能合约开发：https://docs.nuls.io/NULS2.0/smartContractManual.html#_1-introduction

  将开发好的智能合约发布取得 code 用1的智能合约发布接口进行发布
  
  需要开发的智能合约列表
  
         1. NRC-20 发币 (增加 防篡改加密hash字段)


3. lnmp环境搭建，用mysql数据库存储不上链的业务数据

4. 安装php的restfullapi管理框架phalapi2.0，开发调试api: http://docs.phalapi.net/#/v2.0/
    改用线上api管理平台：https://www.eolinker.com/#/invite?inviteCode=9pUUmi

   api调试页面: http://wanghx.eicp.top/phalapi/public/
   
   h5调试页面 http://wanghx.eicp.top/h5
   
