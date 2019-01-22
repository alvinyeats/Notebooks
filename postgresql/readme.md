## 数据库初始化  
```sh
sudo postgresql-setup initdb
sudo systemctl start postgresql
```

## 配置数据库访问权限   
```sh
vim /var/lib/pgsql/data/pg_hba.conf

local all all peer
host all all 127.0.0.1/32 md5
host all all ::1/128 md5
```

## 启动&开机启动服务
```sh
sudo systemctl restart postgresql
sudo systemctl enable postgresql
```

## 创建用户、数据库，赋予权限
```sh
sudo su - postgres
psql
CREATE USER username WITH PASSWORD 'password';
CREATE DATABASE yourdb OWNER username;
GRANT ALL PRIVILEGES ON DATABASE yourdb to username;
\q
```

## 连接数据库
```sh
# 连接本地数据库
psql -U username -d yourdb
# 连接远程数据库
psql -h 192.168.1.1 -U username -d yourdb
```

## 数据库导入导出
```sh
# 导出
pg_dump -U username yourdb > yourdb.sql
# 导入
psql -U username yourdb < yourdb.sql
```

