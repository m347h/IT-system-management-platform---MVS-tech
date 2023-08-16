# IT-system-management-platform---MVS-tech

## dependencies: 

- Lombok 
- Spring Web
- MySQL Driver
- mybatis-plus

## creating database 实例，creating the user table and adding default values. This user table is used for testing purposes. 

```
create Table user 
(
    id       int auto_increment comment '主键' 
        primary key,
    no       varchar(20)              null comment '账号/account',
    name     varchar(100)             not null comment '名字',
    password varchar(20)              null comment '密码',
    age      int                      null,
    gender   int                      null comment '性别',
    phone    varchar(20)              null comment '号码',
    role_id  int                      null comment '角色 0=高级管理员，1=管理员， 2=普通账号 user's role: 0=senior admin, 1=admin, 2=general user',
    isValid  varchar(4) default 'Y'   null comment 'valid or not, Y=valid, else=invalid'
)
    charset = utf8; 
```
