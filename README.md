## Send Message

```
apprise -b "test message" 'apprise://localhost:8000/apprise?tags=tgtxt,tgmd&+X-Apprise-Log-Level=DEBUG' -vvv
```

```
curl -X POST -d '{"body":"test message"}'  -H "Content-Type: application/json" localhost:8000/notify/apprise/?tag=tgtxt
```

```
curl -X POST -d '{"body":"test message"}'  -H "Content-Type: application/json" localhost:8000/notify/apprise/?tag=tgtxt,tgmd
```

```
curl -X POST -H "Content-Type: application/json" "localhost:8000/notify/apprise/?tag=tgmd" -d @- <<EOF
{
    "body": "test message"
}
EOF
```
