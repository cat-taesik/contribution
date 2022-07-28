# Contribution guide
Any resources for contribution

## Kubernetes/website 기여 가이드

다양한 Git 클라이언트들이 있으므로, 가장 기본적인 Git 커맨드와 편집도구를 활용한 기여 방법을 보여준다.

### 1. Setting your username and email in Git

https://docs.github.com/en/get-started/getting-started-with-git/setting-your-username-in-git

git config에 기여자 이름을 지정. 
기여자 명칭을 무엇으로 해도 괜찮으나, GitHub를 기반으로 기여하는 기여자는 GitHub username을 사용하는 것을 추천.

```bash
git config --global user.name "seokho-son"
```
```bash
git config --global user.name
```

git config에 이메일을 지정.
이 이메일의 경우 GitHub의 본인 계정에 등록되어 있는 이메일과 동일해야 함.
본인 계정에 이메일이 등록되어 있지 않다면, GitHub 프로파일 사진 클릭 후 Settings를 클릭하여 Access -> Add email address 에서 이메일을 추가하고 인증을 받아야 함.

https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-email-preferences/setting-your-commit-email-address

```bash
git config user.email "email@example.com"
```

```bash
git config --global user.email
```
