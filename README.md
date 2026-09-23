# 🦀 hello-rust — CI/CD на Rust → GHCR

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
<img width="1698" height="717" alt="Снимок экрана 2026-09-23 114406" src="https://github.com/user-attachments/assets/be9e94ed-584b-4ee2-abfe-253192975025" />


### Пакет в GHCR
<img width="1717" height="885" alt="Снимок экрана 2026-09-23 114445" src="https://github.com/user-attachments/assets/c4af9b47-1ae4-41f0-b18a-f0a17669b1ab" />

