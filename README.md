# JDBC_Assignment3

SQL Code:
CREATE DATABASE sqlandjava;

CREATE TABLE `sqlandjava`.`people` (
  `id` INT NOT NULL,
  `firstname` VARCHAR(45) NOT NULL,
  `lastname` VARCHAR(45) NULL,
  PRIMARY KEY (`id`));

INSERT INTO `sqlandjava`.`people` (`id`, `firstname`, `lastname`) VALUES ('1', 'Anna', 'Bolt');
INSERT INTO `sqlandjava`.`people` (`id`, `firstname`, `lastname`) VALUES ('2', 'Carl', 'Dolk');
INSERT INTO `sqlandjava`.`people` (`id`, `firstname`, `lastname`) VALUES ('3', 'Erik', 'Fram');
INSERT INTO `sqlandjava`.`people` (`id`, `firstname`, `lastname`) VALUES ('4', 'Gina', 'Hult');

CREATE USER ramisa@localhost IDENTIFIED BY 'tahsin';
GRANT SELECT ON sqlandjava.people TO ramisa@localhost;
