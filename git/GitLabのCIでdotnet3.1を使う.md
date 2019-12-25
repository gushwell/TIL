# GitLabのCIでdotnet3.1を使う

.gitlab-ci-yml の先頭行に、以下の記述をする

```yml
image : mcr.microsoft.com/dotnet/core/sdk:3.1
```

