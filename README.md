

## Необходимое

1. **stable rust toolchains**: `rustup toolchain install stable`
2. **nightly rust toolchains**: `rustup toolchain install nightly --component rust-src`
3. **(if cross-compiling) rustup target**: `rustup target add ${ARCH}-unknown-linux-musl`

## Сборка & Запуск

**Запустите `cargo build`, `cargo check`, и тд если все нормально запускай программу**

RUST_LOG=info cargo run --config 'target."cfg(all())".runner="sudo -E"' --   --iface lo

**Карго билд используеться для автоматического построение eBPF и включения его в программу** 

## Кросс-Компилинг

**Кросс кромпилинг команды `target/${ARCH}-unknown-linux-musl/release/demo` можно скопировать для Линукс Серверов,Виртуальных машин и просто для запуска**

## Команды для проверки: 
     ping 127.0.0.1
    curl localhost:8000
 
