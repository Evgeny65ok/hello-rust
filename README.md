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

<img width="990" height="387" alt="Снимок экрана 2026-09-23 115947" src="https://github.com/user-attachments/assets/afcf25ab-2a6b-4bf5-b654-b6f22c7fd3ce" />




### Пакет в GHCR
<img width="1467" height="696" alt="Снимок экрана 2026-09-23 115758" src="https://github.com/user-attachments/assets/c8df73c4-f877-41ec-80f9-dbe5671ba521" />



