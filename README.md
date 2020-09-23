# webSocket_golang
webSocketについての勉強用リポジトリ

## 調査内容

1. webSocketとは
2. 以下のコードが何をしているのか

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

## 調査結果
Issueとしてあげる
