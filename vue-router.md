


## Navigation Guards
Sesuai dengan namanya, navigation guards yang disediakan oleh ``vue-router`` utamanya digunakan untuk mengawal navigasi dengan melakukan redirect atau membatalkannya. Terdapat beberapa ccara untuk mengaitkan ke dalam proses route navigatioin: seccara global, per route, atau dalam component (in-component).

Ingat bahwa perubahan params atau query tidak memicu pengawalan navigasi masuk/keluar. Anda dapat mengamati object ``@route`` untuk bereaksi terhadap perubahan itu, atau menggunakan pengalawan in-component ``beforeRouteUpdate``.

### Global Before Gur