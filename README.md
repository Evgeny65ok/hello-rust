Учебный проект: пайплайн **CI/CD** на Rust с публикацией Docker-образа в **GitHub Container Registry**.


## Что делает пайплайн

* `cargo fmt --check` — форматирование
* `cargo clippy -D warnings` — линтинг
* `cargo test` — тесты
* `cargo build --release` — сборка
* **Docker build + push** в GHCR (только при push в `main`)

## Запуск

```bash
docker build -t hello-rust .
docker run --rm hello-rust
```

**Вывод:**

```text
Hello from Rust in Docker! 🦀🐳
OS: linux
Arch: x86_64
Hello, Docker!
Sum 1..10 = 55
```

## Образ в GHCR

```bash
docker pull ghcr.io/evgeny65ok/hello-rust:latest
docker run --rm ghcr.io/evgeny65ok/hello-rust
```


## Результаты

### Workflow в Actions

<img width="990" height="387" alt="image" src="https://github.com/user-attachments/assets/c4e9f3e0-1f0b-4862-a84d-1c276cba709a" />





### Пакет в GHCR
<img width="1467" height="696" alt="image" src="https://github.com/user-attachments/assets/0cb85751-dfc4-430d-85fc-903427b31b46" />

