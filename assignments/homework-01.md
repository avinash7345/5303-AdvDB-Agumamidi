##Homework 1

##Name:

Avinash Agumamidi

##Ip Address

159.203.183.251

##Phpmyadmin Link

http://159.203.183.251/phpmyadmin

##Table Create statements

##gift_options.sql

CREATE TABLE IF NOT EXISTS `gift_options` (

  `allowGiftWrap` tinyint(1) NOT NULL,
  
  `allowGiftMessage` tinyint(1) NOT NULL,
  
  `allowGiftReceipt` tinyint(1) NOT NULL
  
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

##image_entities.sql

CREATE TABLE IF NOT EXISTS `image_entities` (

  `itemId` int(15) NOT NULL,
  
  `thumbnailImage` varchar(256) NOT NULL,
  
  `mediumImage` varchar(256) NOT NULL,
  
  `largeImage` varchar(256) NOT NULL,
  
  `entityType` varchar(15) NOT NULL,
  
  PRIMARY KEY (`itemId`,`largeImage`)
  
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

##market_place_price.sql

CREATE TABLE IF NOT EXISTS `market_place_price` (

  `itemId` int(15) NOT NULL,
  
  `price` decimal(10,2) NOT NULL,
  
  `sellerInfo` varchar(100) NOT NULL,
  
  `standardShipRate` decimal(10,2) NOT NULL,
  
  `twoThreeDayShippingRate` decimal(10,2) NOT NULL,
  
  `availableOnline` tinyint(1) NOT NULL,
  
  `clearance` tinyint(1) NOT NULL,
  
  `offerType` varchar(25) NOT NULL,
  
  PRIMARY KEY (`itemId`)
  
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

##products.sql

CREATE TABLE IF NOT EXISTS `products` (

  `itemId` int(15) NOT NULL,
  
  `parentItemId` int(15) NOT NULL,
  
  `name` varchar(175) NOT NULL,
  
  `salePrice` decimal(10,2) NOT NULL,
  
  `upc` int(15) NOT NULL,
  
  `categoryPath` varchar(175) NOT NULL,
  
  `shortDescription` varchar(1500) NOT NULL,
  
  `longDescription` varchar(3000) NOT NULL,
  
  `brandName` varchar(50) NOT NULL,
  
  `thumbnailImage` varchar(200) NOT NULL,
  
  `mediumImage` varchar(200) NOT NULL,
  
  `largeImage` varchar(200) NOT NULL,
  
  `productTrackingUrl` varchar(300) NOT NULL,
  
  `modelNumber` varchar(100) NOT NULL,
  
  `productUrl` varchar(400) NOT NULL,
  
  `categoryNode` varchar(50) NOT NULL,
  
  `stock` varchar(50) NOT NULL,
  
  `addToCartUrl` varchar(200) NOT NULL,
  
  `affiliateAddToCartUrl` varchar(350) NOT NULL,
  
  `offerType` varchar(50) NOT NULL,
  
  `msrp` decimal(10,2) NOT NULL,
  
  `standardShipRate` decimal(10,2) NOT NULL,
  
  `color` varchar(10) NOT NULL,
  
  `customerRating` varchar(15) NOT NULL,
  
  `numReviews` int(10) NOT NULL,
  
  `customerRatingImage` varchar(50) NOT NULL,
  
  `maxItemsInOrder` int(15) NOT NULL,
  
  `size` varchar(50) NOT NULL,
  
  `sellerInfo` varchar(50) NOT NULL,
  
  `age` varchar(50) NOT NULL,
  
  `gender` varchar(50) NOT NULL,
  
  `isbn` varchar(50) NOT NULL,
  
  `preOrderShipsOn` varchar(50) NOT NULL,
  
  PRIMARY KEY (`itemId`)
  
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

