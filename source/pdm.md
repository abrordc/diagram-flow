```mermaid
erDiagram
    PELANGGAN ||--o{ PESANAN : membuat
    PESANAN ||--|{ DETAIL_PESANAN : memiliki
    BARANG ||--o{ DETAIL_PESANAN : terdapat_dalam
    KURIR ||--o{ PENGIRIMAN : melakukan
    PESANAN ||--|| PENGIRIMAN : memiliki

    PELANGGAN {
        int id_pelanggan "primary key"
        string nama
        string alamat
        string nomor_telepon
    }
    PESANAN {
        int id_pesanan "primary key"
        int id_pelanggan "foreign key"
        date tanggal_pesanan
        string status_pesanan
    }
    DETAIL_PESANAN {
        int id_detail "primary key"
        int id_pesanan "foreign key"
        int id_barang "foreign key"
        int jumlah
        float harga
    }
    BARANG {
        int id_barang "primary key"
        string nama_barang
        float harga
        int stok
    }
    KURIR {
        int id_kurir "primary key"
        string nama
        string nomor_telepon
    }
    PENGIRIMAN {
        int id_pengiriman "primary key"
        int id_pesanan "foreign key"
        int id_kurir "foreign key"
        date tanggal_kirim
        string status_pengiriman
    }

```
