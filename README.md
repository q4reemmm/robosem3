# Robotics TurtleBot3 - Modul 1

Lingkungan pengembangan ROS 2 Humble menggunakan Docker.

## Cara Menjalankan (Reproducibility)
1. Masuk ke direktori docker: cd docker
2. Build image: docker compose build
3. Jalankan container: docker compose up -d
4. Masuk ke environment: docker compose exec dev bash
5. Di dalam container, jalankan node:
   source /ws/install/setup.bash
   ros2 run my_first_robot_package hello_robot
