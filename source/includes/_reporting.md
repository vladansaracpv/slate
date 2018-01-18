## Reporting
Reporting subsystem is a comprehensive list of endpoints that are used for getting various statistic information about user performance, and accounting.

The base URL for Production environment is:

* `https:/reporting-dot-altthirtysixproduct36.appspot.com`

The base URL for Sandbox environment is:

* `https://reporting-dot-sandboxaltthirtysixproduct36.appspot.com`

**Important notice:** There is a uniform date format which is used for time bound results. Generally, all ISO formats can be used. Nevertheless, following format is commonly used on the platform:

* *epoch_second* - A formatter for the number of seconds since the epoch
* *date or strict_date* - A formatter for a full date as four digit year, two digit month of year, and two digit day of month: yyyy-MM-dd.
* *date_hour_minute_second or strict_date_hour_minute_second* - full date, two digit hour of day, two digit minute of hour, and two digit second of minute: yyyy-MM-dd'T'HH:mm:ss.
* *date_hour_minute_second_fraction* or strict_date_hour_minute_second_fraction
* A formatter that combines a full date, two digit hour of day, two digit minute of hour, two digit second of minute, and three digit fraction of second: yyyy-MM-dd'T'HH:mm:ss.SSS

In the case of datetime ranges, if one uses date or strict_date format, it is considered by the system that the range is from 00:00.00 hour of the start date to 00:00.00 to the end date.

If the response contains cryptocurrency value, it always comes with FIAT value pair, so there is no need for conversion on client side. This considerably reduces the processing amount needed on client side, as client uses the data directly without need for further calculations.

All messages have two parts - metadata part which contain general information of data (such as current page number, number of elements per page, total number of elements etc), summary part (not provided for all report types) which contains summary information and page of data itself. This format reduces the need for clients to make excessive number of calls to the server.

Note that all information is contextualized - related only to user that asks for informations. As the system is heavily relied on roles, every request needs proper JWT token embedded in Authorization Bearer header field in order to work.
