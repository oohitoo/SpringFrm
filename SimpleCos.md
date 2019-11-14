# SimpleCos (Sample)

### 개발 DB  : MySQl 5.7
### 개발 IDE : Spring3 (version 3)

### 사용Lib : lombok, myBatis


> SQL Query
 * ```java
    CREATE TABLE `category` (
    `ctNum` INT(11) NOT NULL AUTO_INCREMENT,
    `ctGubun1` INT(11) NULL DEFAULT NULL,
    `ctGubun2` VARCHAR(100) NULL DEFAULT NULL,
    `ctWriteDate` DATETIME NULL DEFAULT NULL,
    `userID` VARCHAR(20) NULL DEFAULT NULL,
    PRIMARY KEY (`ctNum`)
    )
    COLLATE='utf8_general_ci';

    CREATE TABLE `lecture` (
    `lcNum` INT(11) NOT NULL AUTO_INCREMENT,
    `lcTitle` VARCHAR(1024) NULL DEFAULT NULL,
    `lcContent` MEDIUMTEXT NULL,
    `lcWriteDate` DATETIME NULL DEFAULT NULL,
    `lcReadCount` INT(11) NULL DEFAULT '0',
    `ctNum` INT(11) NULL DEFAULT NULL,
    `userID` VARCHAR(20) NULL DEFAULT NULL,
    PRIMARY KEY (`lcNum`)
    )
    COLLATE='utf8_general_ci';

    CREATE TABLE `user` (
    `userID` VARCHAR(20) NOT NULL,
    `userPW` VARCHAR(100) NULL DEFAULT NULL,
    `userName` VARCHAR(20) NULL DEFAULT NULL,
    `userEmail` VARCHAR(50) NULL DEFAULT NULL,
    `userEmailCheck` TINYINT(1) NULL DEFAULT '0',
    `userSalt` VARCHAR(100) NULL DEFAULT NULL,
    PRIMARY KEY (`userID`)
    )
    COLLATE='utf8_general_ci';
    ```
> 