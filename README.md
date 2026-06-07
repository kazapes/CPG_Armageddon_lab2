# CPG_Armageddon_lab2
Armageddon lab2

#### 05/09/2026

![image.png](https://github.com/kazapes/CPG_Armageddon_lab2/blob/2b2db7833f4772c6173fe5192c514cfb51c72088/Screenshot%202026-05-09%20201841.png)

![image.png](https://github.com/kazapes/CPG_Armageddon_lab2/blob/2b2db7833f4772c6173fe5192c514cfb51c72088/Screenshot%202026-05-09%20201935.png)

![image.png](https://github.com/kazapes/CPG_Armageddon_lab2/blob/2b2db7833f4772c6173fe5192c514cfb51c72088/Screenshot%202026-05-09%20202048.png)

![image.png](https://github.com/kazapes/CPG_Armageddon_lab2/blob/2b2db7833f4772c6173fe5192c514cfb51c72088/Screenshot%202026-05-09%20202100.png)

#!/bin/bash

# 1. Update system and install Apache

yum update -y
yum install -y httpd

# 2. Start and enable Apache web server

systemctl start httpd
systemctl enable httpd

# 3. Create the web content

# We use a 'heredoc' (EOF) to write the HTML and CSS directly to the index file

cat <<EOF> /var/www/html/index.html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Cloud Automation Lab</title>
</head>
<body>
<header>
<h1>Cassiem Davids</h1>
</header>
<section>
<h2>Adapt and overcome</h2>
<p>I am exploring Linux automation and cloud infrastructure to build scalable web environments. Make money and get big bootie bishes</p>
<img src="https://norceca.net/COL.jpg">
</section>
<section>
<h2>Project Armaggedon</h2>
<p>This protected by the red,black, and green. You Sissies.</p>
</section>
<footer>
<h3>Contact / Footer</h3>
<p>Email: [cassiem.davids316@gmail.com](mailto:cassiem.davids316@gmail.com) | AWS Cloud Lab 2026</p>
</footer>
</body>
</html>
EOF

# 4. Set appropriate permissions for the web directory

chown -R apache:apache /var/www/html
chmod -R 755 /var/www/html

05/10/2026
