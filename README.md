# tecgTrain_HW
techTrainでの面談用リポジトリ

## 調査内容1 -webSocket-

1. webSocketとは
https://github.com/Hiroya3/techTrain_HW/issues/1
2. 以下のコードが何をしているのか
https://github.com/Hiroya3/techTrain_HW/issues/2

```
import "github.com/gorilla/websocket"

const (
	socketBufferSize  = 1024
	messageBufferSize = 256
)

var upgrader = &websocket.Upgrader{ReadBufferSize: socketBufferSize, WriteBufferSize: socketBufferSize}

func (r *room) ServeHTTP(w http.ResponseWriter, req *http.Request) {
	socket, err := upgrader.Upgrade(w, req, nil)
}
```

## 調査内容2 -TCP/IP-

