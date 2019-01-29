# hooks
https://{$ST2_IP}/api/v1/webhooks/keel?st2-api-key=xxx
https://docs.stackstorm.com/authentication.html#authentication-apikeys
st2 webhook list
https://docs.stackstorm.com/troubleshooting/webhooks.html

# actions
https://docs.stackstorm.com/reference/runners.html#http-runner-http-request
st2 --debug run keel.approve ...
st2 run keel.approve host=http://localhost:65000 name=test tag=1.1.1

# deploy
ggg .


### TODO
[ ] deal how to inject config values to actions
[ ] pass {{ image }} as {{ name}}:{{ tag }} in actions
