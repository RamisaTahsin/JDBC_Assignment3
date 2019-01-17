# JDBC_Assignment3

SQL Code:
CREATE TABLE `sqlandjava`.`owners` (
  `owner_id` INT NOT NULL,
  `person_id` INT NOT NULL,
  `car_id` INT NOT NULL,
  PRIMARY KEY (`owner_id`));

INSERT INTO `sqlandjava`.`owners` (`owner_id`, `person_id`, `car_id`) VALUES ('1', '2', '3');
INSERT INTO `sqlandjava`.`owners` (`owner_id`, `person_id`, `car_id`) VALUES ('2', '1', '4');
INSERT INTO `sqlandjava`.`owners` (`owner_id`, `person_id`, `car_id`) VALUES ('3', '3', '2');
INSERT INTO `sqlandjava`.`owners` (`owner_id`, `person_id`, `car_id`) VALUES ('4', '4', '1');

GRANT SELECT ON sqlandjava.owners TO ramisa@localhost;

ALTER TABLE `sqlandjava`.`owners` 
ADD INDEX `FK_person_id_idx` (`person_id` ASC) VISIBLE,
ADD INDEX `FK_carr_id_idx` (`car_id` ASC) VISIBLE;
;
ALTER TABLE `sqlandjava`.`owners` 
ADD CONSTRAINT `FK_person_id`
  FOREIGN KEY (`person_id`)
  REFERENCES `sqlandjava`.`people` (`id`)
  ON DELETE NO ACTION
  ON UPDATE NO ACTION,
ADD CONSTRAINT `FK_carr_id`
  FOREIGN KEY (`car_id`)
  REFERENCES `sqlandjava`.`cars` (`car_id`)
  ON DELETE NO ACTION
  ON UPDATE NO ACTION;
