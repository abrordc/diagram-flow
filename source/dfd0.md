```mermaid
graph TD
    A[Pelanggan] -->|Pesan Barang| B((Sistem Antar Barang Online))
    B -->|Konfirmasi Pesanan| A
    C[Kurir] -->|Update Status Pengiriman| B
    B -->|Informasi Pengiriman| C
    D[Admin] -->|Kelola Data| B
    B -->|Laporan| D
```
