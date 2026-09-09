# Laporan Modul 1: Dockerized ROS 2 Development Environment

## Tabel 1.1 - Metrik lingkungan pengembangan
| No | Parameter | Satuan | Hasil |
|---|---|---|---|
| 1 | Waktu docker pull image dasar | s | N/A |
| 2 | Waktu build image pertama (tanpa cache) | s | 203.9 |
| 3 | Waktu build image kedua (dengan cache) | s | 0.711 |
| 4 | Ukuran image robotics-lab:dev | MB | 1890 |
| 5 | Waktu startup container | s | 1.033 |
| 6 | Waktu colcon build pertama | s | 3.687 |
| 7 | Jumlah package terbangun | buah | 1 |
| 8 | Commit hash | - | 8c3d212 |

## Tabel 1.2 - Perbandingan bind mount vs named volume
| Aspek | Bind mount `../src:/ws/src` | Named volume `ws_install` |
|---|---|---|
| Terlihat di host | Ya | Tidak (tersembunyi di internal Docker) |
| Bertahan setelah `docker compose down` | Ya | Ya |
| Cocok untuk kode sumber | Ya (agar bisa diedit di host) | Tidak |
| Cocok untuk artefak build | Tidak (menghindari bentrok OS) | Ya (terisolasi di container) |
