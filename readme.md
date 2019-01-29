# hooks
st2 apikey create -k -m '{"used_by": "keel.sh"}

# actions
st2 run keel.trigger.image image=test tag=1.1.1

# deploy
ggg .
st2 pack install --force file:///makeomatic/stackstorm-keel
service st2chatops restart


# debug
curl -k https://localhost/api/v1/webhooks/keel?st2-api-key=OTVlZjUxZGViMTViNmRlN2VkYmY3ZDdjZmYyYzA4ZWM5YzYwZmViOTI5YmM5YmU3ZjYxNjM0NDNlMDY0ZjE1Yg \
  -H 'Content-Type: application/json' \
  -d '{"level": "LevelSuccess", "message": "Successfully updated deployment <your deployment namespace/name> (gcr.io/webhookrelay/webhook-demo:0.0.10)"}'
