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
     
     1 register and login
     
     2.1 public square
     
     3.1 all votes past comming and in the furch
     
     3.2 personal center(ID card identification)
     
     4.1 my attend(我参加的选举)votes and my host(我举办的选举)votes.  
     
     4.2 create new votes 
     
     4.3 votes management  (start votes stop votes) in 
     
     4.4 vote 
     
     5.1 acccecs and get tickes for vote
     
     5.1 vote result.
 

