Yes LINEPY NEWLIB
```LINE has discontinued the use of getGroup and switched to using getChat```
####
```python
#GetAllgroup
allgroup = client.getAllChatMids().memberChatMids
#Getgroup
group = client.getChats([to]).chats[0]
#Getgroupmid
gmid = client.getChats([to]).chats[0].chatMid
#GetgroupcreatedTime
gcreatedt = client.getChats([to]).chats[0].createdTime
#GetgrouppicturePath
gpicture = client.getChats([to]).chats[0].picturePath
#Getlink Group
group = client.getChats([to]).chats[0]
if group.extra.groupExtra.preventedJoinByTicket == False:
    print(f"https://line.me/R/ti/g/{client.reissueChatTicket(to).ticketId}")
#on/off linkgroup    
group = client.getChats([to]).chats[0]
if group.extra.groupExtra.preventedJoinByTicket == False:
    print("already on linkgroup")
else:
    group.extra.groupExtra.preventedJoinByTicket = False
    print("yes on linkgroup")
#on/off linkgroup      
group = client.getChats([to]).chats[0]
if group.extra.groupExtra.preventedJoinByTicket == True:
    print("already off linkgroup")
else:
    group.extra.groupExtra.preventedJoinByTicket = True
    print("yes off linkgroup")
#GetmemberMid
client.getChats([to]).chats[0].extra.groupExtra.memberMids
#GetinviteeMid
client.getChats([to]).chats[0].extra.groupExtra.inviteeMids
#KickMember
client.deleteOtherFromChat(to, [mid])#? not work use >>(to, mid)
#InvMember
client.inviteIntoChat(to, mid)
#JoinGroup
client.acceptChatInvitation(to)
#CancdlGroupInv
client.rejectChatInvitation(to)
#LeaveGroup
client.deleteSelfFromChat(to)
```