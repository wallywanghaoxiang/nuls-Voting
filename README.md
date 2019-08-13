# 基于nuls的投票系统 nuls-voting

## 核心功能
模块实现的核心业务是在nuls上建立投票选举事件，应征候选人，并让选举人对候选人进行投票，最后公布投票选举结果

## Core functions

 1. 为每个投票选举事件建立独立的链
 
 2. 为每个应征的候选人指定一个唯一不重复的投票地址
 
 3. 给每个投票人发放选票(某个数量的token)
 
 4. 在应征候选人阶段，候选人可以上传自己的介绍和作品链接
 
 5. 当投票开始后，投票人可以把手里的选票投给喜欢的候选人
 
 6. 当投票结束后，投票选举结果向所有用户公示

 
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
    
