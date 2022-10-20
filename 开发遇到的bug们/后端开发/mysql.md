当java端设置字符串编码方式为utf8，数据库字段和数据库表也是utf8编码但是存储却出现乱码时尝试以下操作，在applications.properties写spring.datasource.url=jdbc:mysql://127.0.0.1:3306/compkey?serverTimezone=UTC&useUnicode=true&characterEncoding=UTF-8


