<img width="1362" height="526" alt="image" src="https://github.com/user-attachments/assets/3681c81e-2cc3-4659-8d58-8f4a48185a1d" /># 🦀 hello-rust — CI/CD на Rust → GHCR

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
<img width="1362" height="526" alt="image" src="https://github.com/user-attachments/assets/95fde65a-f1f8-4328-b953-51ffae2219f5" />



### Пакет в GHCR
<img width="1056" height="528" alt="image" src="https://github.com/user-attachments/assets/5c941a7d-0d91-40f7-b8aa-163f098a4b3c" />


