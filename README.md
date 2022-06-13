# Google Cloud Build 

Cloud Build adalah salah satu layanan yang disediakan oleh Google Cloud dimana digunakan sebagai tools dari CI/CD yang dimana itu mempermudah kita dalam melakukan build, test, deploy.

CI/CD itu terbagi atas dua yaitu:
- CI (Continuous Integration) bertujuan untuk pengintregrasian sebuah code yang dijalankan lalu pengujian code ini dilakukan secara berulang-ulang dan juga otomatis

- CD (Continuous Deployment) salah satu proses dimana apakah alikasi yang kita buat itu bisa kita jalankan 

## Creating a basic build configuration file
Berikut bagaimana langkah-langkah untuk konfigure file di Cloud Build

Build config bertujuan untuk menjalankan perintah pada Cloud Build untuk mennjalankan tugas yang kita ingin kerjakan. Dimana dalam dalam proses ini kita dapat menjalankan proses buold, test dan juga deploy, file nya itu dapat berbentuk YAML dan juga dalam bentuk JSON, disini kita akan membuat file config nya dalam bentuk YAML

1. Create the build config file, dalam projek root direktory create file dengan nama `filename.YMAL` itu adalah nama file cofig dalam cloud build config file

2. Add the steps field, pada bagian `steps` pada file config itu berisi langkah langkag yang akan kita lakukan oleh cloud build
    ```
    steps:
    ```
3. Add the first step. di bawah `steps` ada `name` yang berisi container image untuk menjalankan sebuah command, 
    ```
    steps:
    - name: string
    ```
    pada command diatas menjalankan sebuah build step yang akan menjalankan image ubuntu

4. Add step arguments, `args` digunakan dalam menjalankan perintah yang di ambil dari `name` 
    ```
    steps:
    - name: string
    aargs: [string, string, ...]
    ```
    pada command diatas argument yang dubuat hanya untuk menampilkan `Hello, test123`



## Referns
1. [GKE and GCB](https://medium.com/@jw207427/google-kubernetes-engine-gke-and-google-cloud-build-gcb-f8991c43c64a#:~:text=Google%20Kubernetes%20Engine%20(GKE)%20and%20Google%20Cloud%20Build%20(GCB),-A%20productivity%20booster&text=Our%20team%20has%20recently%20completed,up%20with%20the%20new%20requests.)
2. [Overviuw of Cloud Bulid](https://cloud.google.com/build/docs/overview)
3. [Apa Itu CI/CD? Belajar Membuat CI/CD Pipeline di Cloud](https://www.youtube.com/watch?v=5KP9khJMJ8o&ab_channel=CloudEngineeringwithImre)
4. [Build configuration file schema](https://cloud.google.com/build/docs/build-config-file-schema#yaml_14)