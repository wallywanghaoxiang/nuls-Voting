# nuls-Voting
Using nuls blockchain for  Voting

## Functional design
The core business of the module is to vote and get Voting statistics for candidates

## Core functions

 1. Bind the address to a unique candidates when someone announce to be one of Electoral candidates
 
 2. Distribute ballots to voter
 
 3. When election begins, voter send their ballots to candidates.
 
 4. When election ends, get Voting statistics for candidates.
 
## Secondary functions

 1. View the candidates lists.
 
 2. View the Voting statistics for candidates lists when election ends.
 
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
      
      601. api vote host  get tickes for vote
    
    vote result
    
      701. api all the user get the result for this vote event
     

 

