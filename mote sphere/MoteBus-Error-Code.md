# Error Codes  

## 1. error codes of MoteBus  
以下定義來自mbStack或jRPC錯誤碼一覽表  

|   No  |   Error Code   |        Error Message       |
| :---: | :------------: | :------------------------: |
|   1   |     -32001     |          Timeout           |
|   2   |     -32002     |        System error        |
|   3   |     -32003     |       Host not found       |
|   4   |     -32004     |     Address not found      |
|   5   |     -32005     |   Authentication failed    |
|   6   |     -32050     |      Too many account      |
|   7   |     -32060     |       Data not found       |
|   8   |     -32099     |        Runtime error       |
|   9   |     -32100     |          RPC error         |
|   10  |     -32600     |       Invalid Request      |
|   11  |     -32601     |      Method not found      |
|   12  |     -32602     |       Invalid params       |
|   13  |     -32603     |       Internal error       |
|   14  |     -32604     |  Invalid parameter number  |
|   15  |     -32605     |Invalid parameter error - %s|
|   16  |     -32606     |Value cannot be null or empty - %s|
|   17  |     -32700     |         Parse error        |


## 2. error codes of Motechat  
|   No  |  Code  |       Error Message        | 
| :---: | :----: | :------------------------: |
|   1   |    0   |             OK             | 
|   2   | -10199 |          in error          | 
|   3   | -10101 |    in: open XRPC error     | 
|   4   | -10102 |      in: XRPC not open     | 
|   5   | -10103 |    in: motebus not open    | 
|   6   | -10104 |        in: send error      | 
|   7   | -10105 |     in: open XMsg error    | 
|   8   | -10106 |      in: invalid data      | 
|   9   | -10299 |       motechat error       | 
|   10  | -10201 |   motechat: no DC setting  | 
|   11  | -10202 |      motechat not open     | 
|   12  | -10203 |   motechat: invalid data   | 
|   13  | -10204 |  motechat: invalid stoken  | 
|   14  | -10205 | motechat: no rcve function | 
|   15  | -10306 |  motechat: no matched DDN  | 
|   16  | -10207 |      motechat: no DDN      | 
|   17  | -10399 |        wsocket error       | 
|   18  | -10301 |    wsocket: invalid data   | 
|   19  | -10302 |    wsocket: no socket id   | 
