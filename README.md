# Postest-PBO-4

## Manajemen Tiket Event Cosplay

Program ini adalah aplikasi console berbasis Java untuk mengelola tiket acara cosplay.
Fitur utama program adalah CRUD (Create, Read, Update, Delete) dengan tambahan Search.

Program dikembangkan dengan tambahan:

- Encapsulation : atribut dibuat private, akses lewat getter & setter.

- Inheritance : terdapat satu superclass (Ticket) dan dua subclass (RegularTicket, VipTicket).

- Overriding : subclass menimpa method info() untuk menampilkan label sesuai jenis tiket.

- Abstraction : Membuat kode lebih fleksibel lewat abstract class dan interface.

- Polymorphism : Diterapkan dengan Overriding (method label() di subclass) dan Overloading (method search() di TicketService).

## Encapsulation

Semua atribut Ticket (id, name, date, status) dibuat private. Data hanya bisa diakses lewat getter & setter. Contoh:

<img width="450" height="450" alt="image" src="https://github.com/user-attachments/assets/1c22c5d4-af01-4f85-b366-d6355b07e582" />

### Inheritance

RegularTicket dan VipTicket dibuat dengan extends Ticket. Keduanya mewarisi atribut dan method dari superclass.

<img width="537" height="41" alt="image" src="https://github.com/user-attachments/assets/6b88c707-3cdd-423a-94d9-65a82bb0bf49" />

<img width="491" height="28" alt="image" src="https://github.com/user-attachments/assets/0c1f7fec-e78c-457c-bddd-44fb8f393195" />

## Overriding

Subclass RegularTicket dan VipTicket mewarisi Ticket lalu menimpa (override) method info() agar menambahkan label sesuai jenis tiket.

<img width="350" height="349" alt="image" src="https://github.com/user-attachments/assets/a515c927-712a-4879-bb7e-afbcae138500" />

<img width="350" height="352" alt="image" src="https://github.com/user-attachments/assets/5c8c11b9-28a2-48a6-95ba-847445cb4d62" />

### Abstraction

Ticket.java dijadikan abstract class : tidak bisa dibuat objek langsung, hanya subclass yang bisa digunakan.

Priced.java adalah interface : menentukan kontrak method price().

RegularTicket mengimplementasikan price() dengan nilai Rp 50.000.

<img width="298" height="120" alt="image" src="https://github.com/user-attachments/assets/4be576d1-dab5-4064-bc3c-b56fe10da936" />

VipTicket mengimplementasikan price() dengan nilai Rp 150.000.

<img width="295" height="107" alt="image" src="https://github.com/user-attachments/assets/d06cadf7-2f69-4eb1-9a38-562b04aa3c7a" />

### Polymorphism

Overriding : label() ditimpa oleh RegularTicket & VipTicket.

<img width="450" height="450" alt="image" src="https://github.com/user-attachments/assets/3f7e1dbf-d69d-436e-bedd-1eb39fa73ba8" />

Overloading : TicketService memiliki dua method search(...):

<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/5ec508e3-45f6-42b1-9429-8c5bc504633a" />
