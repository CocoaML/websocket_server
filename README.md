# websocket_server
python 简单实现的一个 websocket server 为了客户端测试websocket库的适用性。

url地址:  ws://127.0.0.1:9080

test_socket_html 是浏览器测试 websocket server。
如果iOS客户端测试 websocket 库，须使用模拟器才可以连接。

介绍一个比较好的 websocket库

一个比较好的 Mac & iOS websocket库： https://github.com/acmacalister/jetfire

WebSocket (RFC 6455) client library for iOS & OS X
可以在 Mac 和 iOS客户端使用

提供的接口：
``` python
@optional
/**
 The websocket connected to its host.
 @param socket is the current socket object.
 */
-(void)websocketDidConnect:(nonnull JFRWebSocket*)socket;

/**
 The websocket was disconnected from its host.
 @param socket is the current socket object.
 @param error  is return an error occured to trigger the disconnect.
 */
-(void)websocketDidDisconnect:(nonnull JFRWebSocket*)socket error:(nullable NSError*)error;

/**
 The websocket got a text based message.
 @param socket is the current socket object.
 @param string is the text based data that has been returned.
 */
-(void)websocket:(nonnull JFRWebSocket*)socket didReceiveMessage:(nonnull NSString*)string;

/**
 The websocket got a binary based message.
 @param socket is the current socket object.
 @param data   is the binary based data that has been returned.
 */
-(void)websocket:(nonnull JFRWebSocket*)socket didReceiveData:(nullable NSData*)data;

@end
```

