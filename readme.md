### twilio で SMS が自動応答されてしまうのをされないようにする

#### 設定手順

github.io で作成した xml の応答を返すように設定する。

twilio 側では HTTP POST -> HTTP GET に設定を変更する。

オリジナルのURLは

https://demo.twilio.com/welcome/sms/reply/

```
<?xml version="1.0" encoding="ISO-8859-1"?>
<Response>
<Message>Thanks for the message. Configure your number's SMS URL to change this message.Reply HELP for help.Reply STOP to unsubscribe.Msg&Data rates may apply.</Message>
</Response>
```

メッセージを応答に入れずに
```
<?xml version="1.0" encoding="ISO-8859-1"?>
<Response>
</Response>
```

を返すようなURLを設定した。

https://kkato233.github.io/twilio-test/sms/result.xm

