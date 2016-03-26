# 作业

#### `172.19.32.0/24`能容纳多少台电脑, 那`172.19.32.0/23`能容纳多少台呢?
 + 172.19.32.0/24能容纳**254**台电脑 *扣除网络地址172.19.32.0 广播地址172.19.32.255*
 + 172.19.32.0/23能容纳**510**台电脑 *扣除网络地址172.19.32.0 广播地址172.19.33.255*
 
>对于：172.19.32.0/23  
>首先把172.19.32.0/23化成二进制为：‭‭1010 1100‬,‭0001 0011‬,‭0010 0000‬,000 0   000
>因为斜杠后面是23，所以前23位为网络号，后9位为主机号  
>故网络地址为：**1010 1100‬,‭0001 0011‬,‭0010 000**0,0000 0000即是：172.19.32.0（只保留粗体部分，即是前23位不变，后面的全为  0）
>广播地址为：**1010 1100‬,‭0001 0011‬,‭0010 000**1‬,1111 1111，即是：172.19.33.255（即是刚刚的粗体，其余部分全为1）  
>故有效地址（可用地址）为：172.19.32.1（网络地址+1）——172.19.33.254（广播地址-1）  
>共计510个

#### 设计一个能容纳256台电脑的网络
额，不明白，是像上一题能容纳510台电脑那样吗？
#### 简述常用http状态码含义

| 状态码 	|      状态消息      	|                                                                  含义                                                                  	|
|:------:	|:------------------:	|:--------------------------------------------------------------------------------------------------------------------------------------:	|
|   200  	|        成功        	| 服务器已成功处理了请求。通常，这表示服务器提供了请求的网页。                                                                           	|
|   201  	|       已创建       	| 请求成功且服务器已创建了新的资源。                                                                                                     	|
|   202  	|       已接受       	| 服务器已接受了请求，但尚未对其进行处理。                                                                                               	|
|   203  	|     非授权信息     	| 服务器已成功处理了请求，但返回了可能来自另一来源的信息。                                                                               	|
|   204  	|       无内容       	| 服务器成功处理了请求，但未返回任何内容。                                                                                               	|
|   205  	|      重置内容      	| 服务器成功处理了请求，但未返回任何内容。与 204 响应不同，此响应要求请求者重置文档视图（例如清除表单内容以输入新内容）。                	|
|   206  	|      部分内容      	| 服务器成功处理了部分 GET 请求。                                                                                                        	|
|   300  	|      多种选择      	| 服务器根据请求可执行多种操作。服务器可根据请求者 (User agent) 来选择一项操作，或提供操作列表供请求者选择。                             	|
|   301  	|      永久移动      	| 请求的网页已被永久移动到新位置。服务器返回此响应（作为对 GET 或 HEAD 请求的响应）时，会自动将请求者转到新位置。                        	|
|   302  	|      临时移动      	| 服务器目前正从不同位置的网页响应请求，但请求者应继续使用原有位置来进行以后的请求。                                                     	|
|   303  	|    查看其他位置    	| 当请求者应对不同的位置进行单独的 GET 请求以检索响应时，服务器会返回此代码。对于除 HEAD 请求之外的所有请求，服务器会自动转到其他位置。  	|
|   304  	|       未修改       	| 自从上次请求后，请求的网页未被修改过。服务器返回此响应时，不会返回网页内容。                                                           	|
|   305  	|      使用代理      	| 请求者只能使用代理访问请求的网页。如果服务器返回此响应，那么，服务器还会指明请求者应当使用的代理。                                     	|
|   307  	|     临时重定向     	| 服务器目前正从不同位置的网页响应请求，但请求者应继续使用原有位置来进行以后的请求。                                                     	|
|   400  	|      错误请求      	| 服务器不理解请求的语法。                                                                                                               	|
|   401  	|       未授权       	| 请求要求进行身份验证。登录后，服务器可能会返回对页面的此响应。                                                                         	|
|   403  	|       已禁止       	| 服务器拒绝请求。                                                                                                                       	|
|   404  	|       未找到       	| 服务器找不到请求的网页。例如，如果请求是针对服务器上不存在的网页进行的，那么，服务器通常会返回此代码。                                 	|
|   405  	|      方法禁用      	| 禁用请求中所指定的方法。                                                                                                               	|
|   406  	|       不接受       	| 无法使用请求的内容特性来响应请求的网页。                                                                                               	|
|   407  	|    需要代理授权    	| 此状态代码与 401（未授权）类似，但却指定了请求者应当使用代理进行授权。如果服务器返回此响应，那么，服务器还会指明请求者应当使用的代理。 	|
|   408  	|      请求超时      	| 服务器等候请求时超时。                                                                                                                 	|
|   409  	|        冲突        	| 服务器在完成请求时发生冲突。                                                                                                           	|
|   410  	|       已删除       	| 如果请求的资源已被永久删除，那么，服务器会返回此响应。                                                                                 	|
|   411  	|    需要有效长度    	| 服务器不会接受包含无效内容长度标头字段的请求。                                                                                         	|
|   412  	|   未满足前提条件   	| 服务器未满足请求者在请求中设置的其中一个前提条件。                                                                                     	|
|   413  	|    请求实体过大    	| 服务器无法处理请求，因为请求实体过大，已超出服务器的处理能力。                                                                         	|
|   414  	|    请求的URI过长   	| 请求的 URI（通常为网址）过长，服务器无法进行处理。                                                                                     	|
|   415  	|  不支持的媒体类型  	| 请求的格式不受请求页面的支持。                                                                                                         	|
|   416  	| 请求范围不符合要求 	| 如果请求是针对网页的无效范围进行的，那么，服务器会返回此状态代码。                                                                     	|
|   417  	|    未满足期望值    	| 服务器未满足”期望”请求标头字段的要求。                                                                                                 	|
|   500  	|   服务器内部错误   	| 服务器遇到错误，无法完成请求。                                                                                                         	|
|   501  	|      尚未实施      	| 服务器不具备完成请求的功能。例如，当服务器无法识别请求方法时，服务器可能会返回此代码。                                                 	|
|   502  	|      错误网关      	| 服务器作为网关或代理，从上游服务器收到了无效的响应。                                                                                   	|
|   503  	|     服务不可用     	| 目前无法使用服务器（由于超载或进行停机维护）。通常，这只是一种暂时的状态。                                                             	|
|   504  	|      网关超时      	| 服务器作为网关或代理，未及时从上游服务器接收请求。                                                                                     	|
|   505  	|  HTTP 版本不受支持 	| 服务器不支持请求中所使用的 HTTP 协议版本。                                                                                             	|
#### tcp是如何建立可靠的连接, 如何断开连接的呢?
 ```seq
 Host1->Host2: Syn seq=0
 Host2->Host1: Syn=Ack Ack=1 sed=0
 Host1->Host2: Ack=1 seq=1
 ```
 >在TCP/IP协议中，TCP协议提供可靠的连接服务，采用三次握手建立一个连接。
 >
 > 三次握手建立一个连接: 
 > 
 >第一次握手：建立连接时，客户端发送syn包(syn=j)到服务器，并进入SYN_SEND状态，等待服务器确认；
 >
 >第二次握手：服务器收到syn包，必须确认客户的SYN（ack=j+1），同时自己也发送一个SYN包（syn=k），即SYN+ACK包，此时服务器进入SYN_RECV状态；
 >
 >第三次握手：客户端收到服务器的SYN＋ACK包，向服务器发送确认包ACK(ack=k+1)，此包发送完毕，客户端和服务器进入ESTABLISHED状态，完成三次握手。
 >
 >断开过程需要经过“四次握手”.
 >
 >四次握手断开：
 >
 >客户端 A 发送一个 FIN ，用来关闭客户 A 到服务器 B 的数据传送。
 >
 >服务器 B 收到这个 FIN ，它发回一个 ACK ，确认序号为收到的序号加 1。和 SYN 一样，一个FIN 将占用一个序号。
 >
 >服务器 B 关闭与客户端 A 的连接，发送一个 FIN 给客户端 A
 >
 >客户端 A 发回 ACK 报文确认，并将确认序号设置为收到序号加 1

#### OSI七层模型与TCP/IP四层模型的异同是什么?
OSI相当于学院派的作品，设计先于实现，许多设计也过于理想化。OSI强调提供可靠的数据传输服务，每一层都要进行检测和处理错误。在这方面，TCP/IP和OSI 观点不同。TCP/IP认为可靠要由端对端来保证，不要把系统搞得太复杂。传输层利用检验、ACK和超时等手段实现错误检测和恢复来保证可靠性控制就可以了。但以发展的眼光来看，OSI也有它积极的意义，它适用于更多类型的网络，而不仅仅是计算机网络。

|     OSI    |                                        | TCP/IP             |
|:----------:|----------------------------------------|--------------------|
|    分层    |                  描述                  |        分层        |
|   实体层   | 以二进制数据形式在物理媒体上传输数据   | 网络接         |
| 数据链路层 | 传输有地址的帧以及错误检测功能         | 口层               |
|   网络层   | 为数据包选择路由                       | 网络互联层（IP层） |
|   传输层   | 提供端对端的接口                       | 传输层             |
|   会话层   | 解除或建立与别的节点的联系             | 应             |
|   表示层   | 数据格式化，代码转换，数据加密         | 用               |
|   应用层   | 文件传输，电子邮件，文件服务，虚拟终端 | 层              |

#### socket和ajax相比有什么异同和**优劣**和哪种**业务环境**采用哪种?
以下纯属个人理解，因为搜不到二者比较的内容，所以可能错得很离谱。ajax通过使用HTTP请求完成功能实现，如果数据交互频繁，服务器就需要处理很多HTTP请求，这种方式即浪费带宽（HTTP HEAD 是比较大的），又消耗服务器 CPU 占用（没有信息也要接受请求）。参考这个理解的http://blog.csdn.net/yl02520/article/details/7298309。 socket就不用HTTP HEAD，而且服务器就可以直接将数据传送给客户端，但ajax兼容性好、易学易用。socket应该更适合对数据的实时与同步要求高的情景。
#### 使用UDP的好处是什么
 + 数据发送前不用建立连接，减少了开销和延迟，这一点控制系统来说是非常重要的。
 + UDP没有采用可靠交付，数据收发双方不用维护很多的用于记录连接状态的表。
 + UDP 数据报首部很短，只有8字节，处理方便。
 + UDP取消了拥塞控制，所以发送方不会降低发送速度，这点在实时应用上非常重要。
