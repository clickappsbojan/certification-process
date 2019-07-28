### Request
## NOTE: Got error response for first 
```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns="http://www.juniper.es/webservice/2007/">
	<soapenv:Header/>
		<soapenv:Body>
			<CancelBooking>
				<CancelRQ Version="1.1" Language="es">
					<Login Password="xxxx" Email="xxxxxx"/>
					<CancelRequest ReservationLocator="5H7452" ItemId="122647"/>
				</CancelRQ>
			</CancelBooking>			
     	</soapenv:Body>
</soapenv:Envelope>

```

---
---
---

### Response

#### Success

```xml

```

#### Flield

```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <soap:Body>
        <CancelBookingResponse xmlns="http://www.juniper.es/webservice/2007/">
            <BookingRS Url="http://xml-uat.bookingengine.es" TimeStamp="2019-07-28T11:10:19.8094926+02:00" IntCode="AX/VX5AzggisUXZkijH/U5d/j7cd3oQgRoRRBz8nV/8=">
                <Errors>
                    <Error Text=" The element is the last one in the reservation - it can not be cancelled" Code="LAST_ELEMENT" />
                </Errors>
            </BookingRS>
        </CancelBookingResponse>
    </soap:Body>
</soap:Envelope>

```
