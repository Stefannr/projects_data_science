Scenario

Gett, formerly GetTaxi, is an Israeli-developed technology platform devoted solely to corporate Ground Transportation Management (GTM). They have an app where customers can order taxis and drivers can accept them (offers). When a client clicks the Order button in the app, the matching system searches for the most relevant drivers and offers them the order. In this task, we'd like to look into some matching metrics for orders that didn't go as planned, i.e., the customer didn't end up getting a car.

Assignment
Build up distribution of orders according to reasons for failure: cancellations before and after driver assignment, and reasons for order rejection. Analyse the resulting plot. Which category has the highest number of orders?
Plot the distribution of failed orders by hours. Is there a trend that certain hours have an abnormally high proportion of one category or another? What hours are the biggest fails? How can this be explained?
Plot the average time to cancellation with and without driver, by the hour. If there are any outliers in the data, it would be better to remove them. Can we draw any conclusions from this plot?
Plot the distribution of average ETA by hours. How can this plot be explained?


Data Description

The data set data_orders is stored in CSV format. The columns in the data_orders are as follows:

-order_datetime = order time
-origin_longitude = order longitude
-origin_latitude = order latitude
-order_gk = order number
-m_order_eta = time before order arrival
-order_status_key = status, an enumeration of the following mappings:
	-4 (canceled by the client),
	-9 (canceled by the system, indicating a rejection)
-is_driver_assigned key = whether or not a driver has been assigned
-cancellation_time_in_seconds = the number of seconds that passed before cancellation
