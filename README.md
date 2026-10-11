# Backuper Recovery — загрузочные образы

Предварительные образы на Debian 13 для amd64 и arm64. После загрузки автоматически открывается GUI Backuper.

Поддерживаются Full-бэкапы дисков и отдельных разделов, восстановление Windows-цепочек Full → Incremental, включая изменение размера томов, и работа с сетевыми хранилищами через Ethernet/SMB. Wi-Fi, Bluetooth, звук, камеры/ТВ-тюнеры и тяжёлый графический стек удалены.

## Скачать

Версия: `linux-recovery-2026.10.11-minimal-preview`, 2026-10-11.

| Архитектура | Размер (десятичные МБ) |
| --- | ---: |
| [amd64](https://github.com/aakolokolov/Backuper-Recovery-Images/releases/download/linux-recovery-2026.10.11-minimal-preview/backuper-debian13-amd64.iso) | 279.26 МБ |
| [arm64](https://github.com/aakolokolov/Backuper-Recovery-Images/releases/download/linux-recovery-2026.10.11-minimal-preview/backuper-debian13-arm64.iso) | 296.01 МБ |

[Скачать SHA256SUMS](https://github.com/aakolokolov/Backuper-Recovery-Images/releases/download/linux-recovery-2026.10.11-minimal-preview/SHA256SUMS).

Проверка скачанных файлов:

```sh
sha256sum --ignore-missing -c SHA256SUMS
```

## Проверки и загрузка

Оба ISO прошли проверки в QEMU с UEFI Secure Boot: GUI, USB-клавиатура/мышь, Full-бэкапы, восстановление диска и раздела, цепочки с уменьшением и увеличением томов, Ethernet и SMB.

Это UEFI CD-ROM ISO. Прямая запись на флешку через `dd` пока не поддержана. Проверка USB-загрузки выполнена через эмулируемый USB optical drive; совместимость с физическими устройствами требует отдельной проверки. Восстановление загрузчика Windows пока не реализовано.

GUI запускается автоматически. Учётная запись Live-среды: `recovery`, публичный пароль: `live`. Раскладки US/RU переключаются через Alt+Shift.
