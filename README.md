# CPG_Armageddon_lab2
Armageddon lab2

![image.png](attachment:48a9f235-cd91-4b07-9b0b-39a40ffe1890:image.png)

#### 05/09/2026

Redo image did not populate

![image.png](attachment:c73364bb-6ceb-4579-93d6-696cba299e54:image.png)

![image.png](attachment:b6f66bdf-b01c-4351-930d-9924826c8903:image.png)

![image.png](attachment:35d3bb4f-ef60-4c02-b7c4-5b4ce2ce5e61:image.png)

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