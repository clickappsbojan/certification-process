### Request
```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"
xmlns="http://www.juniper.es/webservice/2007/">
<soapenv:Header/>
<soapenv:Body>
<FlightTicketing>
<FlightTicketingRQ Version="1.1" Language="en">
<Login Email="user@mydomain.com" Password="pass"/>
<Reservations>
<Reservation>
<ReservationLocator>FS1ML2</ReservationLocator>
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
                        <Flight>
                            <Status>OK</Status>
                            <Paxes>
                                <Pax IdPax="1">
                                    <Name>Name A</Name>
                                    <Surname>Surname A</Surname>
                                </Pax>
                                <Pax IdPax="2">
                                    <Name>Name B</Name>
                                    <Surname>Surname B</Surname>
                                </Pax>
                            </Paxes>
                        </Flight>
                    </Reservation>
                </Reservations>
            </FlightTicketingRS>
        </FlightTicketingResponse>
    </soap:Body>
</soap:Envelope>
```