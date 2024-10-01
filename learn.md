# Email Verification - Resend

## 1. Install Driver

```sh
composer require resend/resend-php
```

## 2. Buat akun resend

Buat akun resend, lalu buat api-key, copy

## 3. Verifikasi Domain dari Resend

Buka resend, lalu pergi ke domain, klik add domain. Nanti muncul DNS Record, copy

## 4. Set DNS Record di web hosting: domain

Buka web hosting, pergi ke domain, klik DNS Manager, set DNS Record seperti di resend

## 5. Klik verify di resend/domain

Proses verifikasi akan memakan waktu lama, jadi tunggu aja.

## 4. Konfigurasi

Buka file `.env` dan ubah

```env
MAIL_MAILER=resend
MAIL_FROM_ADDRESS=
MAIL_FROM_NAME=

RESEND_KEY=
```

buat file `config/mail.php` dan ubah

```php
'resend' => [
    'transport' => 'resend',
    'key' => env('RESEND_KEY')
],
```

## 4.
