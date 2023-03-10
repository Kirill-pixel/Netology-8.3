# Netology-8.3. GitLab

### Задание 1

1. Разверните GitLab локально, используя Vagrantfile и инструкцию, описанные в этом репозитории.
2. Создайте новый проект и пустой репозиторий в нём.
3. Зарегистрируйте gitlab-runner для этого проекта и запустите его в режиме Docker. Раннер можно регистрировать и запускать на той же виртуальной машине, на которой запущен GitLab.

`В качестве ответа в репозиторий шаблона с решением добавьте скриншоты с настройками раннера в проекте.`

![Скриншот-1](https://github.com/Kirill-pixel/Netology-8.3/blob/main/1-2.png)
![Скриншот-1](https://github.com/Kirill-pixel/Netology-8.3/blob/main/1.png)
![Скриншот-1](https://github.com/Kirill-pixel/Netology-8.3/blob/main/1-3.png)

---

### Задание 2

1. Запушьте репозиторий на GitLab, изменив origin. Это изучалось на занятии по Git.
2. Создайте .gitlab-ci.yml, описав в нём все необходимые, на ваш взгляд, этапы.

`В качестве ответа в шаблон с решением добавьте:`

![Скриншот-1](https://github.com/Kirill-pixel/Netology-8.3/blob/main/2.png)
![Скриншот-1](https://github.com/Kirill-pixel/Netology-8.3/blob/main/2-1.png)

## Pipeline
```yaml
stages:
  - test
  - build

test:
  stage: test
  image: golang:1.17
  script: 
   - go test .

build:
  stage: build
  image: docker:latest
  script:
   - docker build .
   ```
