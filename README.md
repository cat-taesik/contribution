# Contribution guide
Any resources for contribution

 - https://github.com/kubernetes/website/
   - [Ko issue list](https://github.com/kubernetes/website/issues?q=is%3Aissue+is%3Aopen+label%3Alanguage%2Fko)
   - [Ko PR list](https://github.com/kubernetes/website/pulls?q=is%3Apr+is%3Aopen+label%3Alanguage%2Fko)
 - https://kubernetes.io/ko/docs/contribute/new-content/
 - https://kubernetes.io/ko/docs/contribute/localization_ko/
 - CLA: https://api.easycla.lfx.linuxfoundation.org/v2/repository-provider/github/sign/18706487/51478266/35428/#/?version=2

---

## Kubernetes/website 기여 가이드

다양한 Git 클라이언트들이 있으므로, 가장 기본적인 Git 커맨드와 편집도구를 활용한 기여 방법을 보여준다.

### 1. Setting your username and email in Git

https://docs.github.com/en/get-started/getting-started-with-git/setting-your-username-in-git

git config에 기여자 이름을 지정. 
기여자 명칭을 무엇으로 해도 괜찮으나, GitHub를 기반으로 기여하는 기여자는 GitHub username을 사용하는 것을 추천.

```bash
git config --global user.name "cat-taesik"
```

확인
```bash
git config --global user.name
```

git config에 이메일을 지정.
이 이메일의 경우 GitHub의 본인 계정에 등록되어 있는 이메일과 동일해야 함.
본인 계정에 이메일이 등록되어 있지 않다면, GitHub 프로파일 사진 클릭 후 Settings를 클릭하여 Access -> Add email address 에서 이메일을 추가하고 인증을 받아야 함.

https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-email-preferences/setting-your-commit-email-address

```bash
git config --global user.email "shsongist1@gmail.com"
```

확인
```bash
git config --global user.email
```

### 2. intoit

```bash
git clone https://github.com/kubernetes/website.git
cd website/
ls
```

```bash
git remote add upstream https://github.com/kubernetes/website.git
git remote -v
git fetch upstream
git branch
git checkout upstream/dev-1.24-ko.2 
git log
git checkout -b feat-dev-1.24-ko.2
```


```bash
git status
git add content/ko/docs/reference/glossary/disruption.md
git status
git commit -s -m "Translate the glossary term Disruption into Korean"
git status
git log
```


```bash
ssh-keygen -t rsa -C "shsongist1@gmail.com"
cat /home/son/.ssh/id_rsa.pub 
```


```bash
git push origin feat-dev-1.24-ko.2
```


```bash
git status
git diff
git add content/ko/docs/reference/glossary/disruption.md
git commit --amend
git status
git log
```

```bash
git push origin feat-dev-1.24-ko.2
git push origin feat-dev-1.24-ko.2 --force
```


### 3. build test


```bash
# pull in the Docsy submodule
git submodule update --init --recursive --depth 1
sudo apt install make
```

```bash
# You can set $CONTAINER_ENGINE to the name of any Docker-like container tool
make container-serve
```
