# SERVER UPDATE & FIXES

 # [MODSHOP SYSTEM OVERHAUL]
Bug Fix & Improvement
System Pembelian Aksesoris
• mengganti plugin mSelection ke plugin selection (port) agar UI grid preview object bisa diklik di Android & PC
• mengganti #include <mSelection> ke #include <selection> di Tangerang.pwn
• mengganti ShowModelSelectionMenu ke ShowPlayerSelectionMenu di modshop_functions.inc
• menambahkan modshop_selection.inc berisi array model list dan define MODEL_SELECTION_Modshop
• mengganti callback OnPlayerModelSelection ke OnPlayerSelectionMenuResponse di systems_mselection.inc sesuai plugin selection
• memperbaiki urutan parameter callback (playerid, extraid, response, listitem, modelid) agar object bisa dipilih
• me-comment LoadModelSelectionMenu("vtoylist.txt") dan LoadModelSelectionMenu("objrsign.txt") karena tidak dipakai plugin selection
• memperbaiki format file objrsign.txt — menghapus parameter rotasi , 0, 0, -180 yang tidak didukung, menyisakan model ID saja per baris
System Editing Aksesoris (Android-Friendly)
• mengganti ModshopCatalogDevice — menghapus pilihan perangkat lama yang tidak berfungsi di Android
• menambahkan dialog ModshopEditDevice — player memilih antara PC/Laptop (drag object) atau Android (input manual koordinat)
• menambahkan dialog ModshopManualEdit menampilkan koordinat saat ini ``(PosX/Y/Z, RotX/Y/Z),`` player tap axis yang ingin diedit
• menambahkan dialog input per-axis: ModshopInputX, ModshopInputY, ModshopInputZ, ModshopInputRX, ModshopInputRY, ModshopInputRZ
• setiap perubahan koordinat langsung di-apply ke object dan dialog refresh otomatis menampilkan nilai terbaru
• mode PC tetap menggunakan EditDynamicObject (drag langsung di ingame)
Roadsign System
• memperbaiki roadsigns_functions.inc mengganti mS_INVALID_LISTID ke -1
• mengganti ShowModelSelectionMenu di roadsigns_cmds.inc ke ShowRoadsignModelDialog
• menambahkan ``roadsign_mobilefriendly.inc`` dialog list pilih object untuk /addrsignagar works di Android
@everyone
