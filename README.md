# google-find

## Busquedas basicas


- ” ” (comillas): buscar frase exacta
- and or not: operadores lógicos “y” o “no”
- + y -: incluír y excluír. Ej: jaguar -coches: busca la palabra “jaguar”, pero omite las webs con la palabra “coches”
- * (asterisco): comodín, cualquier palabra, pero una sóla palabra
- . (punto): comodín, cualquier palabra, una o muchas
- intitle o allintitle: la expresión buscada está en el título
- inurl o allinurl: la expresión buscada está en la url
- site: sólo busca resultados dentro de la web que va detrás de “site:”
- filetype: sólo busca archivos de un tipo (doc, xls, txt…)
- link: sólo busca en páginas que tienen un link a una determinada web
- inanchor: sólo busca en páginas que tienen en el texto de enlace la expresión buscada
- cache: muestra el resultado en la cache de Google de una pagina web
- related: busca webs relacionadas con una determinada
- alintext: muestra paginas que tengan las claves en el cuerpo de esta
- info: muestra información de una pagina
- define: busca la definicción de una palabra


## Lista de dorks

- filetype:txt site:web.com passwords|contraseñas|login|contraseña
Busca contraseñas almacenadas en ficheros txt, ahí, sin cifrar ni nada… a lo loco…
- “Index of” / “chat/logs”
Muestra registros de conversaciones que han quedado registradas en diferentes servidores.
- filetype:sql “MySQL dump” (pass|password|passwd|pwd)
Similar al del ejemplo, muestra volcados de bases de datos MySQL donde se encuentren registros del tipo pass|password|passwd|pwd.
- site:gov filetype:doc allintitle:restricted
Al igual que el anterior, es similar al usado en el vídeo de ejemplo para realizar búsquedas de lectura amena entre los ficheros de las web gubernamentales.
- inurl:intranet filetype:doc confidential 
Este también busca ficheros de carácter sensible, pero se centra más en las webs que compartan información con intranets.
- “robots.txt” “disallow:” filetype:txt
El fichero robots.txt es un documento donde se le dice al buscador que indexa la página, qué partes no queremos que se muestren a los visitantes de nuestro sitio. Un buen ejemplo es,  si realizamos esta búsqueda y vemos qué es lo que el dominio www.casareal.es NO quiere que veamos… XD
- inurl:”ViewerFrame?Mode=”
No va muy en la línea de obtener datos, pero es otro ejemplo de cómo un bug y un dork de Google se alían para mostrarnos un sinfín de cámaras ip online disponibles para ser visionadas, ¡algunas de ellas incluso podremos controlarlas!
-filetype:config inurl:web.config inurl:ftp
-ext:(doc | pdf | xls | txt | ps | rtf | odt | sxw | psw | ppt | pps | xml) intext:confidential 
-ext:(doc | pdf | xls | txt | ps | rtf | odt | sxw | psw | ppt | pps | xml) intext:confidential 
-ext:inc "pwd=" "UID="
-ext:ini intext:env.ini
-ext:ini Version=... password
-ext:ini Version=4.0.0.4 password
-ext:ini intext:env.ini
.ext:log "Software: Microsoft Internet Information Services *.*"
-ext:log "Software: Microsoft Internet Information
-ext:log "Software: Microsoft Internet Information Services *.*"
-ext:log \"Software: Microsoft Internet Information Services *.*\"
-filetype:TXT TXT
-filetype:XLS XLS
-filetype:asp   DBQ=" * Server.MapPath("*.mdb")
-filetype:asp "Custom Error Message" Category Source
-filetype:asp + "[ODBC SQL"
-filetype:asp DBQ=" * Server.MapPath("*.mdb")
-filetype:asp DBQ=\" * Server.MapPath(\"*.mdb\") 
-filetype:asp “Custom Error Message” Category Source
-filetype:bak createobject sa
-filetype:bak inurl:"htaccess|passwd|shadow|htusers"
-filetype:bak inurl:\"htaccess|passwd|shadow|htusers\" 
-filetype:conf inurl:firewall -intitle:cvs 
-filetype:conf inurl:proftpd. PROFTP FTP server configuration file reveals
-filetype:dat "password.dat
-filetype:dat \"password.dat\" 
-filetype:eml eml +intext:"Subject" +intext:"From" +intext:"To"
-filetype:eml eml +intext:\"Subject\" +intext:\"From\" +intext:\"To\" 
-filetype:eml eml +intext:”Subject” +intext:”From” +intext:”To”
-filetype:inc dbconn 
-filetype:inc intext:mysql_connect
-filetype:inc mysql_connect OR mysql_pconnect 
-filetype:log inurl:"password.log"
-filetype:log username putty PUTTY SSH client logs can reveal usernames
-filetype:log “PHP Parse error” | “PHP Warning” | “PHP Error”
-filetype:mdb inurl:users.mdb
-filetype:ora ora
-filetype:ora tnsnames
-filetype:pass pass intext:userid
-filetype:pdf "Assessment Report" nessus
-filetype:pem intext:private
-filetype:properties inurl:db intext:password
-filetype:pst inurl:"outlook.pst"
-filetype:pst pst -from -to -date
-filetype:reg reg +intext:"defaultusername" +intext:"defaultpassword"
-filetype:reg reg +intext:\"defaultusername\" +intext:\"defaultpassword\" 
-filetype:reg reg +intext:â? WINVNC3â?
-filetype:reg reg +intext:”defaultusername” +intext:”defaultpassword”
-filetype:reg reg HKEY_ Windows Registry exports can reveal
-filetype:reg reg HKEY_CURRENT_USER SSHHOSTKEYS
-filetype:sql "insert into" (pass|passwd|password)
-filetype:sql ("values * MD5" | "values * password" | "values * encrypt")
-filetype:sql (\"passwd values\" | \"password values\" | \"pass values\" ) 
-filetype:sql (\"values * MD\" | \"values * password\" | \"values * encrypt\") 
-filetype:sql +"IDENTIFIED BY" -cvs
-filetype:sql password
-filetype:sql “insert into” (pass|passwd|password)
-filetype:url +inurl:"ftp://" +inurl:";@"
-filetype:url +inurl:\"ftp://\" +inurl:\";@\" 
-filetype:url +inurl:”ftp://” +inurl:”;@”
-filetype:xls inurl:"email.xls"
-filetype:xls username password email
-index of: intext:Gallery in Configuration mode
-index.of passlist
-index.of perform.ini mIRC IRC ini file can list IRC usernames and
-index.of.dcim 
-index.of.password 
-intext:" -FrontPage-" ext:pwd inurl:(service | authors | administrators | users)
-intext:"# -FrontPage-" ext:pwd inurl:(service | authors | administrators | users) "# -FrontPage-" inurl:service.pwd
-intext:"#mysql dump" filetype:sql
-intext:"#mysql dump" filetype:sql 21232f297a57a5a743894a0e4a801fc3
-intext:"A syntax error has occurred" filetype:ihtml
-intext:"ASP.NET_SessionId" "data source="
-intext:"About Mac OS Personal Web Sharing"
-intext:"An illegal character has been found in the statement" -"previous message"
-intext:"AutoCreate=TRUE password=*"
-intext:"Can't connect to local" intitle:warning
-intext:"Certificate Practice Statement" filetype:PDF | DOC
-intext:"Certificate Practice Statement" inurl:(PDF | DOC)
-intext:"Error Diagnostic Information" intitle:"Error Occurred While"
-intext:"Error Message : Error loading required libraries."
-intext:"Establishing a secure Integrated Lights Out session with" OR intitle:"Data Frame - Browser not HTTP 1.1 compatible" OR intitle:"HP Integrated Lights-
-intext:"Fatal error: Call to undefined function" -reply -the -next
-intext:"Fill out the form below completely to change your password and user name. If new username is left blank, your old one will be assumed." -edu
-intext:"Generated   by phpSystem"
-intext:"Generated by phpSystem"
-intext:"Host Vulnerability Summary Report"
-intext:"HostingAccelerator" intitle:"login" +"Username" -"news" -demo
-intext:"IMail Server Web Messaging" intitle:login
-intext:"Incorrect syntax near"
-intext:"Index of" /"chat/logs"
-intext:"Index of /network" "last modified"
-intext:"Index of /" +.htaccess
-intext:"Index of /" +passwd
-intext:"Index of /" +password.txt
-intext:"Index of /admin"
-intext:"Index of /backup"
-intext:"Index of /mail"
-intext:"Index of /password"
-intext:"Microsoft (R) Windows * (TM) Version * DrWtsn32 Copyright (C)" ext:log
-intext:"Microsoft CRM : Unsupported Browser Version"
-intext:"Microsoft ® Windows * ™ Version * DrWtsn32 Copyright ©" ext:log
-intext:"Network Host Assessment Report" "Internet Scanner"
-intext:"Network Vulnerability   Assessment Report"
-intext:"Network Vulnerability Assessment Report"
-intext:"Network Vulnerability Assessment Report" 本文来自 pc007.com
-intext:"SQL Server Driver][SQL Server]Line 1: Incorrect syntax near"
-intext:"Thank you for your order"   +receipt
-intext:"Thank you for your order" +receipt
-intext:"Thank you for your purchase" +download
-intext:"The following report contains confidential information" vulnerability -search
-intext:"phpMyAdmin MySQL-Dump" "INSERT INTO" -"the"
-intext:"phpMyAdmin MySQL-Dump" filetype:txt
-intext:"phpMyAdmin" "running on" inurl:"main.php"
-intextpassword | passcode)   intextusername | userid | user) filetype:csv
-intextpassword | passcode) intextusername | userid | user) filetype:csv
-intitle:"index of" +myd size
-intitle:"index of" etc/shadow
-intitle:"index of" htpasswd
-intitle:"index of" intext:connect.inc
-intitle:"index of" intext:globals.inc
-intitle:"index of" master.passwd
-intitle:"index of" master.passwd 007电脑资讯
-intitle:"index of" members OR accounts
-intitle:"index of" mysql.conf OR mysql_config
-intitle:"index of" passwd
-intitle:"index of" people.lst
-intitle:"index of" pwd.db
-intitle:"index of" spwd
-intitle:"index of" user_carts OR user_cart
-intitle:"index.of *" admin news.asp configview.asp
-inurl:admin inurl:userlist Generic userlist files

------------------------------------------------------------------------------------------
## Using special search string to find vulnerable websites:

inurl:php?=id1
inurl:index.php?id=
inurl:trainers.php?id=
inurl:buy.php?category=
inurl:article.php?ID=
inurl:play_old.php?id=
inurl:declaration_more.php?decl_id=
inurl:pageid=
inurl:games.php?id=
inurl:page.php?file=
inurl:newsDetail.php?id=
inurl:gallery.php?id=
inurl:article.php?id=
inurl:show.php?id=
inurl:staff_id=
inurl:newsitem.php?num= andinurl:index.php?id=
inurl:trainers.php?id=
inurl:buy.php?category=
inurl:article.php?ID=
inurl:play_old.php?id=
inurl:declaration_more.php?decl_id=
inurl:pageid=
inurl:games.php?id=
inurl:page.php?file=
inurl:newsDetail.php?id=
inurl:gallery.php?id=
inurl:article.php?id=
inurl:show.php?id=
inurl:staff_id=
inurl:newsitem.php?num=

------------------------------------------------------------------------------------------
## For finding open redirects:

inurl:url=https
inurl:url=http
inurl:u=https
inurl:u=http
inurl:redirect?https
inurl:redirect?http
inurl:redirect=https
inurl:redirect=http
inurl:link=http
inurl:link=https

