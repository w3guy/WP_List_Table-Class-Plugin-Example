# WP_List_Table-Class-Plugin-Example
A plugin demonstration on how to use WordPress WP_List_Table Class

# Database SQL dump

``` sql
CREATE TABLE IF NOT EXISTS `wp_customers` (
`ID` int(11) NOT NULL,
  `name` varchar(20) NOT NULL,
  `address` varchar(30) NOT NULL,
  `city` varchar(10) NOT NULL
) ENGINE=InnoDB AUTO_INCREMENT=13 DEFAULT CHARSET=latin1;

INSERT INTO `wp_customers` (`ID`, `name`, `address`, `city`) VALUES
(1, 'Alfreds Futterkiste ', 'Obere Str. 57', 'Berlin'),
(2, 'Ana Trujillo ', 'Avda. de la Constitución 2222', 'México D.F'),
(3, 'Antonio Moreno', 'Mataderos 2312', 'México D.F'),
(4, 'Thomas Hardy ', '120 Hanover Sq.', 'London'),
(5, 'Christina Berglund ', 'Berguvsvägen 8 ', 'Lulea'),
(9, 'Hanna Moos', 'Forsterstr. 57', 'Mannheim'),
(10, 'Frédérique Citeaux', '24, place Kléber', 'Strasbourg'),
(11, 'Martín Sommer', 'C/ Araquil, 67', 'Madrid'),
(12, 'Laurence Lebihans', '12, rue des Bouchers', 'Marseille');

ALTER TABLE `wp_customers` ADD PRIMARY KEY (`ID`);
 
ALTER TABLE `wp_customers` MODIFY `ID` int(11) NOT NULL AUTO_INCREMENT;
```

# Security

You should whitelist the orderby parameter your plugin / theme accept to avoid any form of sql injection. See [#2](https://github.com/collizo4sky/WP_List_Table-Class-Plugin-Example/issues/2)
