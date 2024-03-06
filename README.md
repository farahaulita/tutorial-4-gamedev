# Proses Pengerjaan Level Baru
## Pembuatan TileMap baru
Pada level baru, saya akun menggunakan spritesheet tile lain. Untuk level ini, saya menngunakan spritesheet planet dan melakukan pembuatan tilemap seperti dengan tilemap sebelumnya. Akan dibuat TileSet baru dengan tipe atlas dan membentuk shape collisionnya. Untuk collision, saya menentukan collision mask dan layer player di 1 dan 2, dan tilemap memiliki collision layer dan mask 2. Hal ini berarti tile map hanya dapat ber-collide dengan objek di layer 2, dan berada di layer 2. Player berada di layer 1 dan 2, dan dapat ber-collide dengan objek di layer 1 dan 2.
## Pembuatan Spawner Objek baru
Untuk level baru, saya menggunakan sprite bergambar lebah dari folder assets. Sama seperti fish, root node adalah sebuah RigidBody2D dengan children sprite dan collision shape. Bee akan diberikan script yang memiliki fungsi yang sama dengan fish. Agar dapat mendapat collision dengan Player, Contact Monitor perlu dicentang dan Contacts Reported diganti menjadi 1. Lalu, akan diconnect sinyal on body entered pada node RigidBody2D. Untuk collision, Bee berada di layer 1 dengan mask 1, yang berarti Bee hanya dapat berinteraksi dengan player dan bukan dengan tilemap.
## Pembuatan Level baru
<img width="505" alt="image" src="https://github.com/farahaulita/tutorial-4-gamedev/assets/92159879/cac6e2bc-b453-4d1c-a81c-0d53ee27e7cb">

Area menang pada level sebelumnya akan mengarah ke level baru ini (Level2) dan menyelesaikan level ini akan menampilkan WinScreen. Terdapat spawner baru dengan posisi yang lebih kecil dan berisi node Bee. LoseArea ditaruh di bagian bawah, yang akan menampilkan LoseScreen jika player terjatuh. Terdapat juga platform bergerak yang dapat digunakan oleh Player di level ini.

## Platform Bergerak
<img width="413" alt="image" src="https://github.com/farahaulita/tutorial-4-gamedev/assets/92159879/6c726f66-1e6a-4ebb-b32c-538358baae2b">

Platform dibuat menggunakan sebuah Node2D dengan children KinematicBody2D dan AnimationPlayer. Kinematic2D ini juga berisi sprite dan collision shape platform. Untuk animasi, digunakan AnimationPlayer. Dibuat animasi baru yang berupa perpindahan posisi platform selama 4 detik.

## Referensi
https://stackoverflow.com/questions/69728827/how-do-i-detect-collisions-in-godot
https://www.youtube.com/watch?v=p6q8Nn2yd6I
https://kidscancode.org/godot_recipes/3.x/2d/moving_platforms/
