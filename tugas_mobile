import 'package:flutter/material.dart';
void main() => runApp(App());

class App extends StatelessWidget {
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Flutter penyimpanan data',
      home: Scaffold(
        appBar: AppBar(
          title: Text('Data Mahasiswa'),
        ),
        body: Mahasiswa(),
      ),
    );
  }
}

class DataMahasiswa{
  String tgllahir;
  String nama;
  String alamat;
  String jkelamin;
  
  
  DataMahasiswa({this.tgllahir, this.nama, this.alamat, this.jkelamin});
  
}

// class Mahasiswa
class Mahasiswa extends StatefulWidget {
  _MyappState createState() => _MyappState();
}

class _MyappState extends State<Mahasiswa> {
  //deklarasi variabel
  final txtnamamahasiswa = TextEditingController();
  final txttgllahir = TextEditingController();
  final txtjkelamin = TextEditingController();
  final txtalamat = TextEditingController();
  

  List<Widget> data = [];

  onTambah() {
    setState(() {
       data.add(ListTile(leading: Text(txtnamamahasiswa.text)));
       data.add(ListTile(leading: Text(txttgllahir.text)));
       data.add(ListTile(leading: Text(txtjkelamin.text)));
       data.add(ListTile(leading: Text(txtalamat.text)));      
      txttgllahir.clear();
      txtnamamahasiswa.clear();
      txtalamat.clear();
      txtjkelamin.clear();
    });
  }

  Widget build(BuildContext context) {
    return ListView(
      children: <Widget>[
        new Container(
          padding: EdgeInsets.all(10.0),
          child: Column(
            mainAxisAlignment: MainAxisAlignment.spaceEvenly,
            children: <Widget>[
               TextField(
                controller: txtnamamahasiswa,
                decoration: InputDecoration(hintText: 'Nama Mahasiswa'),
              ),
              TextField(
                controller: txttgllahir,
                decoration: InputDecoration(hintText: 'Tanggal Lahir'),
              ),
              TextField(
                controller: txtjkelamin,
                decoration: InputDecoration(hintText: 'Jenis Kelamin'),
              ),
              TextField(
                controller: txtalamat,
                decoration: InputDecoration(hintText: 'Alamat'),
              ),
              Divider(height: 5.0),
              ElevatedButton(child: Text("Tambah"), onPressed: onTambah),
            ],
          ),
        ),
        new Column(
          children: data,
        )
      ],
    );
  }
}
