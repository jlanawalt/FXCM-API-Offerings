These are examples of the use of the Java API to place market orders on the first account found (JavaFixTrader.java) and to pull historical rates with the Java API (JavaFixHistoryMiner.java).

Introduction

The FXCM Trading SDK provides clients with a fully functioning programmable API into the FXCM FX trading platform. The APIs main features are streaming executable FX trading prices, the ability to open/close positions and entry orders as well as set/update/delete stops ands limits. The API Object model is based on the FIX specification for FX (http://www.fixprotocol.org) and is very simple and easy to use. Brief overview of core API classes

IGateway: This is the primary interface into the FXCM trading platform. It contains all the entry points into application usability.

FXCMLoginProperties: This class is used in the login method of IGateway and contains the properties necessary to log in.

CollateralReport: represents an FXCM accounts properties at the time the message was generated. When it is a part of a batch responsethe RequestID can be used to match against the RequestID received from the IGateway.

ExecutionReport: This class represents an orders status in the system. When it is a part of a batch response the RequestID can be used to match against the RequestID received from the IGateway.

PositionReport: This class is used to represent a positions status in the FXCM system. When it is a part of a batch response the RequestID can be used to match against the RequestID received from the IGateway.

ClosedPositionReport: This class represents a closed position in the FXCM system. When it is a part of a batch response the RequestID can be used to match against the RequestID received from the IGateway.

OrderSingle: This class is used to send orders into the system.

CollateralInquiryAck: This class is the first leg of a batch response to retrieve accounts.

RequestForPositionsAck: This class is the first leg of a batch response to retrieve open or closed positions.

MessageGenerator: This class is a factory for all order types available in the API

OrderCancelRequest: This class is used to delete stop/limit orders.

OrderCancelReplaceRequest: This class is used to update entry order prices and also to update stop/limit order prices.

IGenericMessageListener: Implementations of this interface are registered with IGateway to receive application messages.

IStatusMessageListener: Implementations of this interface are registered with IGateway to receive application status messages.

How to access the JAVA JAR files

1) Click on the link below and download the zip file

https://apiwiki.fxcorporate.com/api/java/trading_sdk.zip

2) Extract the fxcm-api folder to a location of your choice

3) Rename fxcm-api.jar and fxmsg.jar to fxcm-api.zip and fxmsg.zip

4) Extract these files to a location of your choice

You now have access to the contents of the JAR files.