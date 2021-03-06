# playground
Random scripts, pipelines, etc. for testing integration with GitHub


## Web Hook trigger for GitHub Actions

## Linux

```
curl -X POST https://api.github.com/repos/sondreb/playground/dispatches \
-H 'Accept: application/vnd.github.everest-preview+json' \
-H 'Authorization: token TOKEN_VALUE_HERE' \
--data '{"event_type": "CUSTOM_ACTION_NAME"}'
```

```
curl -XPOST -u "[username]:[token]" \
  -H "Accept: application/vnd.github.everest-preview+json" \
  -H "Content-Type: application/json" \
  https://api.github.com/repos/[username]/[repository]/dispatches \
  --data '{"event_type": "production-deploy"}'
```

## Windows

CURL on Windows is a bit funky, so you'll need to do this, escape the single quites:

```
curl -XPOST -u "[username]:[token]" \
  -H "Accept: application/vnd.github.everest-preview+json" \
  -H "Content-Type: application/json" \
  https://api.github.com/repos/[username]/[repository]/dispatches \
  --data "{\"event_type\": \"production-deploy\"}"
```

If you put this in a bat file, you can do the following:

```
curl -XPOST -u "[username]:[token]" ^
  -H "Accept: application/vnd.github.everest-preview+json" ^
  -H "Content-Type: application/json" ^
  https://api.github.com/repos/[username]/[repository]/dispatches ^
  --data "{\"event_type\": \"production-deploy\"}"
```

