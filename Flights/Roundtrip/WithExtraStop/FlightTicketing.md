# NOTE:
  All the reservation are coming with CAN status so we couldn't ticket the issue
### Request
```xml

<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns="http://www.juniper.es/webservice/2007/">
<soapenv:Header/>
	<soapenv:Body>
		<FlightTicketing>
			<FlightTicketingRQ Version="1.1" Language="es">
			<Login Email="user@mydomain.com" Password="pass"/>
			<Reservations>
				<Reservation>
				<ReservationLocator>WQT5Y1</ReservationLocator>
				<Commission Type="Fixed" Amount="10" Currency="USD"/>
				</Reservation>
			</Reservations>
			</FlightTicketingRQ>
		</FlightTicketing>
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
        <FlightTicketingResponse xmlns="http://www.juniper.es/webservice/2007/">
            <FlightTicketingRS>
                <Reservations>
                    <Reservation>
                        <Flight Locator="">
                            <Status>No flights in this reservation.</Status>
                        </Flight>
                    </Reservation>
                </Reservations>
            </FlightTicketingRS>
        </FlightTicketingResponse>
    </soap:Body>
</soap:Envelope>
```