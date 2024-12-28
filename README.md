WhatsApp clone

import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      home: Scaffold(
          appBar: AppBar(
            backgroundColor: Color(0xff075e54),
            title: Text(
              "Whatsapp",
              style: TextStyle(
                color: Color(0xffffffff),
              ),
            ),
          ),
          body: SingleChildScrollView(
            child: Column(
              children: [
                buildListTile("Luffy", "Orewa Monkey.D.Luffy",
                    "https://qph.cf2.quoracdn.net/main-qimg-86a6872cb7874b8d5659e2e86343d3f0"),
                buildListTile("Zoro", "Orewa Roronova Zoro",
                    "https://cdn.oneesports.gg/cdn-data/2024/04/Anime_OnePiece_Zoro_Sword_Attack.jpg"),
                buildListTile("Sanji", "Orewa Vinsmoke Sanji",
                    "https://images.saymedia-content.com/.image/ar_4:3%2Cc_fill%2Ccs_srgb%2Cfl_progressive%2Cq_auto:eco%2Cw_1200/MTc5MzIwNjMyNjE2NzU2OTMx/sanji-and-women-a-legacy-of-kindness.jpg"),
                buildListTile("Sanks", "Orewa Sanks",
                    "https://w0.peakpx.com/wallpaper/146/580/HD-wallpaper-one-piece-shanks-one-piece.jpg"),
                buildListTile("Law", "Orewa Water.D.Law",
                    "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRNrnC6abxPDvo4yZ79ids0_oXptm-557Ly1g&s"),
                buildListTile("Usopp", "Orewa God.D.Usopp",
                    "https://us-tuna-sounds-images.voicemod.net/a577bb2f-ac7b-4463-99f9-c5e479919e2a-1678301466422.jpg"),
                buildListTile("Buggy", "Orewa Buggy",
                    "https://i.pinimg.com/736x/64/ed/c2/64edc2f1f217d35f4474705fe9113e00.jpg"),
                buildListTile("Brook", "Yo ho ho",
                    "https://lh6.googleusercontent.com/proxy/Z4W2Q_KksThILAYr6zRDiHaztertv9IyDaSoJTAhE5DBKQejhgXgIBIhrUTGlWi9rUDbF7y4y2cgmeZ59At3Xuq0wM4p"),
                buildListTile("Garp", "Monkey.D.Garp",
                    "https://i.pinimg.com/originals/7b/2b/b0/7b2bb02184e1ce0360cde6893b1608f2.jpg"),
                buildListTile("ace", "arigato",
                    "https://i.pinimg.com/736x/e7/50/91/e750917efa38a814044331bd926b0a2d.jpg"),
                buildListTile("Dragon", "I am luffy's father",
                    "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTQFtnZ4ZNCndw9ucgyqs80VeTSypEu2ZFaVg&s")
              ],
            ),
          )),
    );
  }

  ListTile buildListTile(tile, subtile, img) {
    return ListTile(
      leading: CircleAvatar(
        backgroundImage: NetworkImage(img),
      ),
      title: Text(
        tile,
        style: TextStyle(
          fontSize: 17,
          fontWeight: FontWeight.bold,
        ),
      ),
      subtitle: Text(subtile),
      trailing: Column(
        mainAxisAlignment: MainAxisAlignment.center,
        children: [
          Text("19/08/2024"),
          Icon(
            Icons.done_all,
            color: Colors.blue,
          ),
        ],
      ),
    );
  }
}

