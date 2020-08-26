-- phpMyAdmin SQL Dump
-- version 4.7.9
-- https://www.phpmyadmin.net/
--
-- Host: 127.0.0.1:3306
-- Generation Time: Nov 26, 2018 at 08:57 PM
-- Server version: 5.7.21
-- PHP Version: 5.6.35

SET SQL_MODE = "NO_AUTO_VALUE_ON_ZERO";
SET AUTOCOMMIT = 0;
START TRANSACTION;
SET time_zone = "+00:00";


/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!40101 SET NAMES utf8mb4 */;

--
-- Database: `criminal_data`
--

-- --------------------------------------------------------

--
-- Table structure for table `accused`
--

DROP TABLE IF EXISTS `accused`;
CREATE TABLE IF NOT EXISTS `accused` (
  `accused_id` int(11) NOT NULL AUTO_INCREMENT,
  `address` varchar(70) DEFAULT NULL,
  `name` varchar(25) NOT NULL,
  `contact` char(10) DEFAULT NULL,
  `fir_id` int(11) NOT NULL,
  PRIMARY KEY (`accused_id`),
  KEY `fir_id` (`fir_id`)
) ENGINE=MyISAM AUTO_INCREMENT=7 DEFAULT CHARSET=latin1;

--
-- Dumping data for table `accused`
--

INSERT INTO `accused` (`accused_id`, `address`, `name`, `contact`, `fir_id`) VALUES
(1, NULL, 'Sudhakar', NULL, 1),
(2, NULL, 'Sudhakar', NULL, 4),
(3, 'Govindpura', 'Manish', '9547897247', 5),
(4, 'Sihora', 'Dileep', '9547891247', 7),
(5, 'Khamaria', 'Ravi', '6547191277', 8),
(6, 'Russel Chowk', 'Samrat', '7547333277', 11);

-- --------------------------------------------------------

--
-- Table structure for table `cases`
--

DROP TABLE IF EXISTS `cases`;
CREATE TABLE IF NOT EXISTS `cases` (
  `cases_id` int(11) NOT NULL AUTO_INCREMENT,
  `cases_name` varchar(50) NOT NULL,
  `status` varchar(20) NOT NULL,
  `station_id` int(11) NOT NULL,
  `fir_id` int(11) NOT NULL,
  PRIMARY KEY (`cases_id`),
  KEY `station_id` (`station_id`),
  KEY `fir_id` (`fir_id`)
) ENGINE=MyISAM AUTO_INCREMENT=16 DEFAULT CHARSET=latin1;

--
-- Dumping data for table `cases`
--

INSERT INTO `cases` (`cases_id`, `cases_name`, `status`, `station_id`, `fir_id`) VALUES
(1, 'Sudhakar vs Virendra', 'Pending', 1, 1),
(2, 'Cash Bag snatching ', 'Resolved', 1, 2),
(3, 'Ghamapur Theft matter', 'Pending', 1, 3),
(4, 'Sudhakar vs ShivPrakash', 'Pending', 1, 4),
(5, 'Hyundai Hit And Run', 'Pending', 2, 5),
(6, 'Jewelery Snatching and threatened for death', 'Resolved ', 2, 6),
(7, 'Gagan Kidnap case', 'Resolved ', 1, 8),
(8, 'MadanYadav vs Deepak ', 'Pending', 1, 9),
(9, 'I20 Chori Mamala ', 'Resolved', 1, 10),
(10, 'Suzuki Bike accident  ', 'Resolved', 1, 11),
(11, 'Fight case among children', 'Pending', 1, 12),
(12, 'PNB robbery case ', 'Pending', 1, 13),
(13, 'LalSingh Mystery Case ', 'Pending', 1, 14),
(14, 'Genearal Store firing ', 'Resolved', 1, 15),
(15, 'JPS child kidnapping  ', 'Pending', 1, 16);

-- --------------------------------------------------------

--
-- Table structure for table `complainant`
--

DROP TABLE IF EXISTS `complainant`;
CREATE TABLE IF NOT EXISTS `complainant` (
  `complainant_id` int(11) NOT NULL AUTO_INCREMENT,
  `fir_id` int(11) NOT NULL,
  `p_id` int(11) NOT NULL,
  PRIMARY KEY (`complainant_id`),
  KEY `fir_id` (`fir_id`),
  KEY `p_id` (`p_id`)
) ENGINE=MyISAM AUTO_INCREMENT=16 DEFAULT CHARSET=latin1;

--
-- Dumping data for table `complainant`
--

INSERT INTO `complainant` (`complainant_id`, `fir_id`, `p_id`) VALUES
(1, 1, 5),
(2, 2, 8),
(3, 3, 11),
(4, 1, 13),
(5, 5, 20),
(6, 7, 36),
(7, 8, 39),
(8, 9, 42),
(9, 10, 45),
(10, 11, 48),
(11, 12, 50),
(12, 13, 54),
(13, 14, 57),
(14, 15, 60),
(15, 16, 60);

-- --------------------------------------------------------

--
-- Table structure for table `crime`
--

DROP TABLE IF EXISTS `crime`;
CREATE TABLE IF NOT EXISTS `crime` (
  `crime_id` int(11) NOT NULL AUTO_INCREMENT,
  `crime_type` varchar(30) NOT NULL,
  PRIMARY KEY (`crime_id`)
) ENGINE=MyISAM AUTO_INCREMENT=12 DEFAULT CHARSET=latin1;

--
-- Dumping data for table `crime`
--

INSERT INTO `crime` (`crime_id`, `crime_type`) VALUES
(1, 'Dacoity'),
(2, 'Rape'),
(3, 'Murder'),
(4, 'Att_to_Murder'),
(5, 'Robbery'),
(6, 'Kid_For_Ransom'),
(7, 'Snatching'),
(8, 'Theft'),
(9, 'Arson'),
(10, 'Hurt'),
(11, 'Road Accident');

-- --------------------------------------------------------

--
-- Table structure for table `criminal`
--

DROP TABLE IF EXISTS `criminal`;
CREATE TABLE IF NOT EXISTS `criminal` (
  `criminal_id` int(11) NOT NULL AUTO_INCREMENT,
  `origin_state` varchar(30) NOT NULL,
  `cases_id` int(11) NOT NULL,
  `crime_id` int(11) NOT NULL,
  `p_id` int(11) NOT NULL,
  PRIMARY KEY (`criminal_id`),
  KEY `cases_id` (`cases_id`),
  KEY `crime_id` (`crime_id`),
  KEY `p_id` (`p_id`)
) ENGINE=MyISAM AUTO_INCREMENT=21 DEFAULT CHARSET=latin1;

--
-- Dumping data for table `criminal`
--

INSERT INTO `criminal` (`criminal_id`, `origin_state`, `cases_id`, `crime_id`, `p_id`) VALUES
(1, 'MadhyaPradesh', 1, 10, 7),
(2, 'MadhyaPradesh', 2, 7, 10),
(3, 'MadhyaPradesh', 3, 8, 12),
(4, 'MadhyaPradesh', 4, 10, 7),
(5, 'MadhyaPradesh', 5, 11, 23),
(6, 'MadhyaPradesh', 6, 7, 25),
(7, 'MadhyaPradesh', 7, 6, 41),
(8, 'MadhyaPradesh', 7, 6, 66),
(9, 'MadhyaPradesh', 8, 4, 43),
(10, 'MadhyaPradesh', 8, 4, 44),
(11, 'MadhyaPradesh', 9, 8, 46),
(12, 'MadhyaPradesh', 9, 8, 47),
(13, 'MadhyaPradesh', 11, 8, 50),
(14, 'MadhyaPradesh', 10, 10, 53),
(15, 'MadhyaPradesh', 11, 5, 55),
(16, 'MadhyaPradesh', 11, 5, 56),
(17, 'MadhyaPradesh', 13, 3, 59),
(18, 'MadhyaPradesh', 14, 4, 61),
(19, 'MadhyaPradesh', 15, 6, 65),
(20, 'MadhyaPradesh', 15, 6, 62);

-- --------------------------------------------------------

--
-- Table structure for table `fir`
--

DROP TABLE IF EXISTS `fir`;
CREATE TABLE IF NOT EXISTS `fir` (
  `fir_id` int(11) NOT NULL AUTO_INCREMENT,
  `incident_date` date NOT NULL,
  `incident_time` time NOT NULL,
  `incident_place` varchar(30) NOT NULL,
  `description` varchar(500) NOT NULL,
  `status` varchar(20) NOT NULL,
  `officer_id` int(11) NOT NULL,
  PRIMARY KEY (`fir_id`),
  KEY `officer_id` (`officer_id`)
) ENGINE=MyISAM AUTO_INCREMENT=17 DEFAULT CHARSET=latin1;

--
-- Dumping data for table `fir`
--

INSERT INTO `fir` (`fir_id`, `incident_date`, `incident_time`, `incident_place`, `description`, `status`, `officer_id`) VALUES
(1, '2018-01-01', '12:30:00', 'Sadar', ' accused hit victim with baseball bat in head ,injured severely', 'investigating', 1),
(2, '2018-04-11', '12:30:00', 'Sikandara', 'accussed person attempt to snatch a bag which contains cash of 50000 Rupees ', 'closed', 2),
(3, '2018-04-16', '02:30:00', 'Sadar', 'some people or someone  entered in house and steal jewellary items worth 250000 rupees and cash amount approx 200000 rs when all family members were attending a party ', 'investigating', 1),
(4, '2018-05-11', '22:30:00', 'Ranjhi ', ' accused hit victim ,issues is relade to land .accused was having a revolver ', 'investigating', 2),
(5, '2018-05-15', '05:16:09', 'Habibganj', 'Accused  was driving car with hi speed and  drunk, collides with a bike ,bike riders injured ,their condition was fatal,one of them deceased on the  spot  ', 'investigating', 3),
(6, '2018-06-06', '13:09:34', 'Bhopal Cant', 'two bikers snatched the golden chain and golden earring from a lady.they were having a revolver ,they threatened her .But Lady remembered their vehicle number . ', 'closed', 4),
(7, '2018-08-23', '09:12:12', 'Sadar Bazar', 'victim accused his neighbor for hurting him without reason .', 'fake', 5),
(8, '2018-09-15', '13:09:31', 'SadarBazar', 'They kidnapped my son. They are Asking for rs 25000 as ransom .they threatened me and said if i will inform police my child will not be safe any more.', 'resolved', 7),
(9, '2018-08-11', '02:30:00', 'Vijaynagar', ' He attacked on me with a iron rod and knife,however i ran away from there', 'investigating', 5),
(10, '2018-07-11', '02:37:00', 'Ranjhi', ' Someone steal my car from main market parking ', 'closed', 7),
(11, '2018-07-17', '02:37:00', 'RoadWays Bus Stand ', 'A sports biker hits victim on turn ,he attempt to ran away from that place  ', 'closed', 5),
(12, '2018-07-27', '04:37:00', 'Infront Sadar SBI branch ', 'they injured my son with  cricket bat in head during playing ,he fell down  unconsiously   ', 'investigating', 1),
(13, '2018-08-07', '04:17:00', 'PNB bank civil lines branch ', 'they entered in  bank,cut the all commucating wires and caught innocent people at gun point ,the were five in numbers ,they took approx 20,00,000 rupees   ', 'investigating', 2),
(14, '2018-10-11', '02:37:00', 'Lal bhawan Shahpura', ' i found him sleeping in his room when i opened his room some, i awake him but he was not any more ', 'investigating', 2),
(15, '2018-10-01', '12:41:00', 'Behind Civic centre ', ' He entered in my shop and purchase some items worth 3000 rs whe i asked for payment he show me revolver and fired a bullet at me but i headed down behind counter .with in 30 seconds ,he ran away.  ', 'closed', 1),
(16, '2018-11-01', '12:41:00', 'Jabalpur public school ', ' They  tempted my son by giving some eatables as seen in school groud cctv camera .  ', 'Investigating', 5);

-- --------------------------------------------------------

--
-- Table structure for table `officer`
--

DROP TABLE IF EXISTS `officer`;
CREATE TABLE IF NOT EXISTS `officer` (
  `officer_id` int(11) NOT NULL AUTO_INCREMENT,
  `designation` varchar(20) NOT NULL,
  `station_id` int(11) NOT NULL,
  `p_id` int(11) NOT NULL,
  PRIMARY KEY (`officer_id`),
  KEY `station_id` (`station_id`),
  KEY `p_id` (`p_id`)
) ENGINE=MyISAM AUTO_INCREMENT=9 DEFAULT CHARSET=latin1;

--
-- Dumping data for table `officer`
--

INSERT INTO `officer` (`officer_id`, `designation`, `station_id`, `p_id`) VALUES
(1, 'Inspector', 1, 1),
(2, 'Sub-Inspector', 1, 2),
(3, 'Inspector', 2, 3),
(4, 'Sub-Inspector', 2, 4),
(5, 'Constable', 1, 25),
(6, 'Constable', 2, 28),
(7, 'Sub-Inspector', 1, 35),
(8, 'Sub-Inspector', 2, 34);

-- --------------------------------------------------------

--
-- Table structure for table `person_id`
--

DROP TABLE IF EXISTS `person_id`;
CREATE TABLE IF NOT EXISTS `person_id` (
  `p_id` int(11) NOT NULL AUTO_INCREMENT,
  `name` varchar(30) NOT NULL,
  `dob` date NOT NULL,
  `address` varchar(60) NOT NULL,
  `contact` char(10) NOT NULL,
  `gender` varchar(10) NOT NULL,
  PRIMARY KEY (`p_id`)
) ENGINE=MyISAM AUTO_INCREMENT=167 DEFAULT CHARSET=latin1;

--
-- Dumping data for table `person_id`
--

INSERT INTO `person_id` (`p_id`, `name`, `dob`, `address`, `contact`, `gender`) VALUES
(1, 'Pradyumn', '1980-12-14', 'Vijay Nagar', '6547891277', 'Male'),
(2, 'Abhijeet', '1985-11-17', 'Adhartal', '6547841247', 'Male'),
(3, 'Daya', '1984-10-15', 'HabibGanj', '6547891247', 'Male'),
(4, 'Fredricks', '1982-02-01', 'Cant Bhopal', '6547898247', 'Male'),
(5, 'Pankaj', '1985-07-02', 'Sadar Bazar', '6547897247', 'Male'),
(6, 'Virendra', '1988-02-10', 'Gorakhpur', '6547591247', 'Male'),
(7, 'Sudhakar', '1981-08-02', 'RusselChowk', '6547893247', 'Male'),
(8, 'Jayant', '1984-12-10', 'Ranjhi', '6547891217', 'Male'),
(9, 'Shinde', '1989-11-30', 'Omti', '6542891247', 'Male'),
(10, ' Sanjay', '1990-12-14', 'Sihora', '7547891277', 'Male'),
(11, 'Pranav', '1985-11-19', 'Ghamapur', '7547841247', 'Male'),
(12, 'ShivPrakash', '1984-10-19', 'Vijay nagar', '7547891247', 'Male'),
(13, 'Ashwani', '1982-02-09', 'GharhiChowk', '7547898247', 'Male'),
(14, 'Samar', '1985-07-09', 'RusselChowk', '7547897247', 'Male'),
(15, 'Kushal', '1988-02-19', 'Panagar', '6747591247', 'Male'),
(16, 'Pratap', '1981-09-02', 'Station Road', '6747893247', 'Male'),
(17, 'Saurabh', '1989-12-10', 'Ranjhi', '7547891217', 'Male'),
(18, 'Susheel', '1989-11-09', 'Bhedahat', '7542891247', 'Male'),
(19, 'Prathviraj', '1980-12-14', 'Gorakhpur', '6447891277', 'Male'),
(20, 'Rishi', '1985-11-09', 'Kolar', '6447841247', 'Male'),
(21, 'Vivek', '1984-09-15', 'HabibGanj', '8547891247', 'Male'),
(22, 'Mayur', '1982-02-09', 'KamlaNagar', '9547898247', 'Male'),
(23, 'Manish', '1985-09-02', 'Govindpura', '9547897247', 'Male'),
(24, 'Vrinda', '1988-02-09', 'Shahpura', '6547599247', 'Female'),
(25, 'Ateeq', '1989-08-02', 'Adhartal', '9547893247', 'Male'),
(26, 'Prathvi', '1980-12-14', 'Gorakhpur', '6447891277', 'Male'),
(27, 'Rishi', '1985-11-09', 'Kolar', '6447841247', 'Male'),
(28, 'Vivek', '1984-09-15', 'HabibGanj', '8547891247', 'Male'),
(29, 'Mayur', '1982-02-09', 'KamlaNagar', '9547898247', 'Male'),
(30, 'Manish', '1985-09-02', 'Govindpura', '9547897247', 'Male'),
(31, 'Vrinda', '1988-02-09', 'Shahpura', '6547599247', 'Female'),
(32, 'Afshan ', '1989-08-02', 'Adhartal', '9547893247', 'Male'),
(33, 'Salman', '1984-09-10', 'Misrod', '9547891217', 'Male'),
(34, 'Shamsher', '1989-11-09', 'Kamlanagar', '9542891247', 'Male'),
(35, ' Nakur', '1990-12-09', 'Sumannagar', '9547891277', 'Male'),
(36, 'Digvijay', '1985-09-19', 'Shahganj', '9547841247', 'Male'),
(37, 'Dileep', '1989-10-19', 'Sihora', '9547891247', 'Male'),
(38, 'Tanusha', '1992-02-09', 'Gorakhpur', '9547898247', 'Female'),
(39, 'Praveen', '1990-05-02', 'Adhartal', '8974546541', 'Male'),
(40, 'Gagan', '1998-12-03', 'Dumna', '8745126398', 'Male'),
(41, 'Ravi', '1980-12-14', 'Adhartal', '6547191277', 'Male'),
(42, 'Deepak', '1985-11-17', 'Dumna', '6517841247', 'Male'),
(43, 'Madan', '1984-10-15', 'Khamaria', '6147891247', 'Male'),
(44, 'Bahadur', '1982-02-01', 'Sadar', '6547898241', 'Male'),
(45, 'Karan', '1985-07-02', 'VijayNagar', '6547897247', 'Male'),
(46, 'Arjun', '1988-02-10', 'Rupanagar', '6547591147', 'Male'),
(47, 'Rahul', '1981-08-02', 'Adhartal', '6547813247', 'Male'),
(48, 'Nakul', '1984-12-10', 'Ranjhi', '6547812317', 'Male'),
(49, 'Ajay', '1989-11-30', 'Sadar', '6542892347', 'Male'),
(50, ' Samrat', '1990-12-14', 'Civillines', '7547333277', 'Male'),
(51, 'Aditya', '1985-11-19', 'Gorakhpur', '7547833247', 'Male'),
(52, 'Swapnil', '1994-10-19', 'RusselChowk', '7337891247', 'Male'),
(53, 'Tanzeel', '1982-02-09', 'GharhiChowk', '7547893247', 'Male'),
(54, 'Suhel', '1985-07-09', 'Panagar', '7547837247', 'Male'),
(55, 'Sohil', '1988-02-19', 'Vijaynagar', '6747591237', 'Male'),
(56, 'Salman', '1981-09-02', 'CivilLines', '6747393247', 'Male'),
(57, 'Arun', '1989-12-10', 'Ranjhi', '7547891237', 'Male'),
(58, 'Lalsingh', '1989-11-09', 'Omti', '7542891237', 'Male'),
(59, 'Shyam', '1988-02-10', 'GharhiChowk', '6547531247', 'Male'),
(60, 'Kaushik', '1981-08-02', 'Pipariya', '6547833247', 'Male'),
(61, 'Ajayraj', '1984-12-10', 'Khamaria', '6543891217', 'Male'),
(62, 'Abhay', '1989-11-30', 'RussselChowk', '6542891237', 'Male'),
(63, ' Arvind', '1999-12-14', 'GharhiChowk', '7547893377', 'Male'),
(64, 'Manoj', '1985-11-19', 'Ranjhi', '7547841237', 'Male'),
(65, 'Ritik', '1984-10-19', 'Civillines', '7533891247', 'Male'),
(66, 'Saroj', '1992-04-05', 'VijayNagar', '6547841240', 'Male');

-- --------------------------------------------------------

--
-- Table structure for table `station`
--

DROP TABLE IF EXISTS `station`;
CREATE TABLE IF NOT EXISTS `station` (
  `station_id` int(11) NOT NULL AUTO_INCREMENT,
  `station_name` varchar(30) NOT NULL,
  `station_location` varchar(30) NOT NULL,
  PRIMARY KEY (`station_id`)
) ENGINE=MyISAM AUTO_INCREMENT=4 DEFAULT CHARSET=latin1;

--
-- Dumping data for table `station`
--

INSERT INTO `station` (`station_id`, `station_name`, `station_location`) VALUES
(1, 'Dumna', 'jabalpur'),
(2, 'Habibganj', 'Bhopal'),
(3, 'CivilLines', 'Indore');

-- --------------------------------------------------------

--
-- Table structure for table `victim`
--

DROP TABLE IF EXISTS `victim`;
CREATE TABLE IF NOT EXISTS `victim` (
  `victim_id` int(11) NOT NULL AUTO_INCREMENT,
  `fir_id` int(11) NOT NULL,
  `p_id` int(11) NOT NULL,
  PRIMARY KEY (`victim_id`),
  KEY `fir_id` (`fir_id`),
  KEY `p_id` (`p_id`)
) ENGINE=MyISAM AUTO_INCREMENT=19 DEFAULT CHARSET=latin1;

--
-- Dumping data for table `victim`
--

INSERT INTO `victim` (`victim_id`, `fir_id`, `p_id`) VALUES
(1, 1, 6),
(2, 2, 9),
(3, 3, 11),
(4, 4, 12),
(5, 5, 21),
(6, 5, 22),
(7, 6, 24),
(16, 14, 48),
(9, 7, 36),
(10, 8, 40),
(11, 9, 42),
(12, 10, 45),
(13, 11, 49),
(14, 12, 52),
(15, 13, 54),
(17, 15, 60),
(18, 16, 62);
COMMIT;

/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION */;
