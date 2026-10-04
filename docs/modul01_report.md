# Laporan Praktikum Modul 1

## Langkah yang Dikerjakan
1. Verifikasi lingkungan ROS 2 Humble dan Docker.
2. Membuat package `my_first_robot_package` (ament_python).
3. Menyusun Dockerfile, entrypoint.sh, dan compose.yaml.
4. Menjalankan service `talker` dan `listener` menggunakan Docker Compose.

## Masalah dan Solusi
- **Problem**: Command `ros2` tidak ditemukan saat `docker compose exec`.
- **Solusi**: Memanggil file `/entrypoint.sh` secara eksplisit (`docker compose exec talker /entrypoint.sh ros2 node list`) agar environment ROS 2 ter-source dengan benar.
