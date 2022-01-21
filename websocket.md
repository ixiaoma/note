var wsServer = 'ws://localhost:8888/Demo'; //服务器地址
var websocket = new WebSocket(wsServer); //创建WebSocket对象
websocket.send("hello");//向服务器发送消息
alert(websocket.readyState);//查看websocket当前状态
websocket.onopen = function (evt) {
//已经建立连接
};
websocket.onclose = function (evt) {
//已经关闭连接
};
websocket.onmessage = function (evt) {
//收到服务器消息，使用evt.data提取
};
websocket.onerror = function (evt) {
//产生异常
}; 
