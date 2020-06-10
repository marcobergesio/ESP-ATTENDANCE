ESP ATTENDANCE PROJECT

Require: Ubuntu, ESP32 Module (2 to 4), Sqlite3, QT

Written in: C, C++, SQL

This is an university project able to estimate in a short and long period of time the number of persons inside the intersection area of ESP32 modules. 
It's possibile to use from 2 to 4 ESP modules. Every minute each ESP syncronizes itself with the server and collects all Wifi Probe-Request packs that can listen in promisc mode, then sends all the data  to the Server using a TCP connection. 
Server collects data every minute from ESPs, filters packets not listened from all ESPs, and try to make an estimate of the relative position of each device listened and of the total number of devices. MAC address of user's device with relative position are saved on a Database, which can be queried by the provided GUI for search long period statistics.

-On /run you'll find executable file, mac.txt that contains MAC ADDRESS of ESP module and our template database.

-On /esp_probe_req_sniffer you'll find code for the ESP modules, search on https://docs.espressif.com/projects/esp-idf/ how to flash them.

-On /server_and_analyzer you'll find code for Server, Analyzer, Database in C++ and GUI made with QT libraries. 




Walter Maffione, Stefano Tata, Marco Bergesio, Luigi Napoleone Capasso


Politecnico di Torino - Programmazione di Sistema 2018/2019
