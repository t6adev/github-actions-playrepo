# Github Actions Playrepo
This repo is my playground to test github actions.

## deployments-trigger.yml
To test deployment trigger.
You can run this workflow to send a github api request.
Like this:
```
$ curl -H "Authorization: token YOUR_API_TOKEN" https://api.github.com/repos/tell-y/github-actions-playrepo/deployments -X POST -d '{"ref":"master", "task": "test", "auto_merge": false, "payload": { "foo": "bar" }, "environment":"dev", "description": "this is test"}'
```

Notice:
- There is a condition(`if: github.event.sender.login == 'tell-y'`) when it should run itself.
