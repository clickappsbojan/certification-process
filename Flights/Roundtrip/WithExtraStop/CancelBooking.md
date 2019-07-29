# NOTE:
  All the reservation are coming with CAN status so we couldn't Cancel any of them

### Request
```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns="http://www.juniper.es/webservice/2007/">
	<soapenv:Header/>
		<soapenv:Body>
			<CancelBooking>
				<CancelRQ Version="1.1" Language="es">
					<Login Email="user@mydomain.com" Password="pass"/>
					<CancelRequest ReservationLocator="V4W2HZ"/>
				</CancelRQ>
			</CancelBooking>			
     	</soapenv:Body>
</soapenv:Envelope>
```

---
---
---

### Response

```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <soap:Body>
        <CancelBookingResponse xmlns="http://www.juniper.es/webservice/2007/">
            <BookingRS Url="http://xml-uat.bookingengine.es" TimeStamp="2019-07-28T17:14:40.6293307+02:00" IntCode="Rb45qQYedpBmcyFQd0bN+n5KgSgUbY5WdJZ6ysLpPHc=">
                <Errors>
                    <Error Text=" The reservation is already cancelled" Code="RESERVATION_ALREADY_CANCELLED" />
                </Errors>
            </BookingRS>
        </CancelBookingResponse>
    </soap:Body>
</soap:Envelope>
```