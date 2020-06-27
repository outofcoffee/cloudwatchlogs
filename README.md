# cloudwatchlogs

Web UI for accessing AWS Cloud Watch Logs.

## Install

Via Go:

```
go get github.com/sosedoff/cloudwatchlogs
```

Pull docker image:

```
docker pull sosedoff/cloudwatchlogs
```

## Example

```
docker run \
  --rm \
  -p 5555:5555 \
  -e AWS_ACCESS_KEY=key \
  -e AWS_SECRET_KEY=secret \
  sosedoff/cloudwatchlogs
```

App should be available at `http://localhost:5555`

## Usage

```
Usage:
  cloudwatchlogs [OPTIONS]

Application Options:
      --host=         Server host (default: 0.0.0.0)
      --port=         Server port (default: 5555)
      --auth-user=    User name for basic authentication
      --auth-pass=    User password for basic authentication
      --access-key=   AWS access key
      --secret-key=   AWS secret key
      --region=       AWS region
      --profile=      AWS CLI profile
      --event-filter= Log event filter (appended to any user provided input)
      --title=        Web page title
      --show-groups=  Whether to show the list of log groups (default: true)
      --show-streams= Whether to show the list of log streams (default: true)

Help Options:
  -h, --help        Show this help message
```

## Screenshot

<img src="screenshot.png" style="border: 1px solid #eee" />

## License

MIT