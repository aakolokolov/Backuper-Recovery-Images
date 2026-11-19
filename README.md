# Retavik Recovery — загрузочные образы

Предварительные образы на Debian 13 для amd64 и arm64. После загрузки автоматически открывается GUI Retavik Recovery на Slint.

Поддерживаются Full-бэкапы дисков и отдельных разделов, восстановление Windows-цепочек Full → Incremental, включая изменение размера томов, и работа с сетевыми хранилищами через Ethernet/SMB. Wi-Fi, Bluetooth, звук, камеры/ТВ-тюнеры и тяжёлый графический стек удалены.

## Скачать

Текущий выпуск — Retavik Recovery v4 от 19 ноября 2026 года.

| Архитектура | Размер (десятичные МБ) |
| --- | ---: |
| [amd64](https://github.com/aakolokolov/Backuper-Recovery-Images/releases/download/retavik-recovery-2026.11.19-writer1/retavik-recovery-amd64.iso) | 282,66 МБ |
| [arm64](https://github.com/aakolokolov/Backuper-Recovery-Images/releases/download/retavik-recovery-2026.11.19-writer1/retavik-recovery-arm64.iso) | 299,63 МБ |

[Скачать SHA256SUMS](https://github.com/aakolokolov/Backuper-Recovery-Images/releases/download/retavik-recovery-2026.11.19-writer1/SHA256SUMS).

Проверка скачанных файлов:

```sh
sha256sum --ignore-missing -c SHA256SUMS
```

## Проверки и загрузка

Оба ISO v4 прошли в QEMU загрузку с UEFI Secure Boot, проверку GUI и виртуального USB-ввода, создание Full и восстановление диска и раздела, включая цепочку с изменением размера тома.

Это UEFI CD-ROM ISO. Прямая запись на флешку через `dd` пока не поддержана. В QEMU проверена загрузка ISO через USB optical drive и GPT/FAT32 USB-носителей, подготовленных в Linux. Для проверки на реальном ПК запишите образ через мастер Retavik. В предыдущей версии клиента используйте Custom ISO и SHA-256 из манифеста. Восстановление загрузчика Windows пока не реализовано.

GUI запускается автоматически. Учётная запись Live-среды: `recovery`, публичный пароль: `live`. Раскладки US/RU переключаются через Alt+Shift.

[Предыдущий октябрьский выпуск](https://github.com/aakolokolov/Backuper-Recovery-Images/releases/tag/linux-recovery-2026.10.11-minimal-preview).
