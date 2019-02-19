# public-node-serverless-app

firebase functions

## User A makes a 'buy' order
- 'order' document created/written 
- trigger firebase function 
- get from input: userId, orderId, userAccountCashBalance, stockQuantity, stockPrice
- now search for an exising and pending 'sell' orders from Orders Collection
- sell order must have: userid, orderId, stockQuantity, stockPrice, and a positive userAccountCashBalance
- if 'sell' order found in Order Collection that matches the required critera, Update Order Document
- update User B (seller) positions, subtract quantity from positions stock, add cash to userAccountCashBalance
- if no sell order available, hand over to Backend Server and create order Queue, make a POST request to backend server

# User B makes a 'sell' order

when a 'buy' order is placed

search for an 'sell' order

if sell order for 'stock id' is found

update 'positions' of 'buy' user

update 'positions' of 'sell' user

