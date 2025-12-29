・20251229: **「LIFF登録 → DynamoDBに購読保存 → 0/しきい値は ingest で即通知 → 送信停止(stale)は EventBridge で定期通知」**まで全部入り

aws cloudformation deploy \
  --template-file template.yml \
  --stack-name store-people-stack \
  --capabilities CAPABILITY_NAMED_IAM \
  --region ap-northeast-3 \
  --parameter-overrides \
    LineChannelAccessToken="YOUR_LINE_CHANNEL_ACCESS_TOKEN" \
    LineLoginChannelId="YOUR_LINE_LOGIN_CHANNEL_ID"


