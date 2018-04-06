FROM microsoft/windowsservercore:10.0.14393.2125

ENV chocolateyUseWindowsCompression false

RUN powershell -Command \
    iex ((new-object net.webclient).DownloadString('https://chocolatey.org/install.ps1')); \
    choco feature disable --name showDownloadProgress

run cinst ruby ruby2.devkit python2 nodejs.install -y

run gem install bundler
run npm install -g grunt-cli

cmd powershell
