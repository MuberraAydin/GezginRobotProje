# GezginRobotProje
 
Gezgin Robot Projesi

Projede, daha önce oluşturulan dünya üzerinde yeni objeler eklenerek dünya üzerindeki nesnelerin tespitini gerçekleştirmek amaçlanmıştır.

cd catkin_ws/src 
 #komutu catkin_ws projemizde src klasörüne giriyoruz.

git clone --recursive https://github.com/leggedrobotics/darknet_ros.git
#darknet_ros'u buraya klonluyoruz

cd ..
#catkin_ws dosyamıza dönüyoruz

catkin_make -DCMAKE_BUILD_TYPE=Release

catkin build
#devel log ve build klasörlerini silerek catkin_ws dosyamızı yeniden build ediyoruz.

roslaunch turtlebot3_gazebo turtlebot3_empty_world.launch
#projeyi çalıştırdık

roslaunch darknet_ros yolo_v3.launch> output.txt
#YOLO’yu çalıştırıyoruz ve tespit edilen nesneler txt dosyasına yazdırıyoruz.

![alt text](https://github.com/MuberraAydin/GezginRobotProje/blob/main/Pictures/Results.png)

 Terminalde YOLO’yu çalıştırdıktan sonra robotun görebildiği nesneler txt dosyasına yazdırılmıştır. Nesnelerin Koordinatı bulunmamıştır. Aynı nesne tekrar edebilmektedir. Tespit edilen nesneler .txt dosyasına yazdırılmıştır.




