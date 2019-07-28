### Request
```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"
	xmlns="http://www.juniper.es/webservice/2007/">
	<soapenv:Header/>
	<soapenv:Body>
		<FlightCheckAvail>
			<FlightCheckAvailRQ Version="1.1" Language="es">
			<Login Email="xxxxxxxxxxx" Password="xxxxxxxxxx"/>
			<FlightCheckAvailRequest>
				<FlightOption
					RatePlanCode="pR+Drc2veFAtxSETJRPPRxMSU0S+05he6M86pFU7TItH/vJd8W5itMWaHlsRgYOkeCzN9SSMHaeDK8p0rbDJfBiLRqG6ntWJB3RDlrAd8PLSv4kcW//TCK+stcMQNxlm0CXwSkh9qvb8RaRJ0tQvpJG5V8cdPPERUyVeLGogneQNE4BzH4f/tovnelLzl/fXc/71gUmZAF24HBGRLi91PAFUXz4ZUOCyOSiPB8WeXw3TyOXg0JaRkJLhgxqg6T0JZOMwop6q7Y7lcCf7q0vJRZYvXG1YfJlEYB2TEBp68CHQLJtIsrslAyDu5t6zIQq6liM0bdTLotfi2sYR79kirAv91zIoRQVwMfy0Uh8oiYIOuT1nWcbtJ/dwedvqbJCLGynyOKGwm2uZxzdZjuJ7faHgH+ptqhzLD4fKRDI9d6Kd4uYXSr9x3ee/DIszRXbu+8cbKnrZVLYUywZcm9EyyotXRlY6CdaFriT6TE2xqUS1Q/X9WEgivdOBxvtBzbcft0BsaTZkbGzARc2z3obgcYEgxa9K4FfOxRalNJjVh2axZAMXAavb2T+VES9XX1zlZ8ciSTElT6pOrKL6SMzwqQd1GKPude1HqWPhmVzF5hoAXc4aOI6TwRh4G1zCfxTbT9bKEI17QTZQodi80JnXcm52Ov21nJ0nxfWhwEOpeEBjVku2eMvG/odhYiAAK9SS3+5YSM/dW+FBgcfOwpRSvY48iha6tUJsbKgGzMI+dhyfHxrb5RrViF66EbfXCwfz06noj5OirQQW8h3gmSAHVgBVKmewj1bXIVHqPqPL05barPQYJeJNFQMBMbZWT1Y0VXBdS4a+sPx8z+YgOrFHTiBOrPGjwDi/sWGNLATKQVdF1Gx95BM3nsafSRy7d2kqcmrXE590BhHc8dZ6im7tOmcEVAACLvdIOzJeiFydKl4="/>
			</FlightCheckAvailRequest>
				<AdvancedOptions>
			     	<ShowBreakdownPrice>true</ShowBreakdownPrice>
				</AdvancedOptions>
			</FlightCheckAvailRQ>
		</FlightCheckAvail>
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
        <FlightCheckAvailResponse xmlns="http://www.juniper.es/webservice/2007/">
            <CheckAvailRS Url="http://xml-uat.bookingengine.es" TimeStamp="2019-07-28T15:15:05.6477641+02:00" IntCode="nLDW0ROyPFshYxm12KQhlj8HHDur1Vpfr9wyoJYw6SQ=">
                <Results>
                    <FlightResult Status="OK" Direction="Outbound" LowCost="false" RatePlanCode="pR+Drc2veFAtxSETJRPPRxMSU0S+05he6M86pFU7TItH/vJd8W5itMWaHlsRgYOkeCzN9SSMHaeDK8p0rbDJfJBwUa4YfJ0vUuDEp3dzSZFf0m2Vcx7d0GT11wZ5zOsYV8fQlLC2eaXwIfG3uiLQ+evGERwX4ZKua0qCF6LnNzPk8oeq5saQpIXwCIqUIQTEXQYZJtieiIPIJBhZqJXZ24sCCDDG4KO898Z9Q9XzJM6a7C2fLxssnjPXLaRUVqPaicAclP9SVB8ysAb51PBzUQEKCzy9COKcXT99YMGOIDkNCmZCk9OSsfbbdZ6/9jn2jnA2iWYbxhawkAnNmKvvK6bVitmw0oejE2MsjU60WmeE57DoZp619Gkn+dVbPoC3YACd+xckDjjWnJuTzvCQz7GvfQZ3CvdqChW2ztZBbWmKE1Xip9opv6Z5Uuc/ULjLfat1yhVl1eq8GzVPgxKLmrU3ibvEPBm188EyIw5GZ/8M9l3psfoNsy8Yve/8AXjuZ1oy+DgW9UDUy3t+YIHSm4Jzm2gmC07OoZTkGXiNqC+RG8K0JUf+cBHktyyNLyFfcNZ6TWuY9kaAOxbSZsNxab3l+fraTyfHZUYkwowL83/LPQjAD05DQFXhncdVg5S1J8o5I+XwtvHZDxyc8J3Wr/0SLU8mJ5kh7qDlvMOqu6M1L7O50BUNk6mVmFuzpvnLDCDgehSK+IDQq/OE89sNPtOggOLCJ52gIbG1KwPl9v8CFIOUWxBmzmREr6dnWJeS+txjdub1LVD+nBPb+v8i59NM8F9G0qV6HUwe26Eu7bvinzqxXhU7KkYy9fxeej03pyIO80fOHp2udCddDKKzRM42xDOaj/vFlwPTS65ScF1MVgldcLEGhzYI9lDzTG2g">
                        <PriceInformation>
                            <Routes ValidatingCarrier="IB">
                                <Route Origin="40233" Destination="37786">
                                    <Segments>
                                        <Segment DepartureAirport="PMI" ArrivalAirport="MAD" DepartureDate="2019-10-16T06:30:00" ArrivalDate="2019-10-16T07:55:00" OperatingAirline="I2" MarquetingAirline="IB" FlightNumber="3917" JourneyDuration="P0DT1H25M0S" Class="A" Cabin="Y" AirplaneType="32A" FareBasis="AD7OB3" />
                                    </Segments>
                                </Route>
                            </Routes>
                            <Prices>
                                <Price Type="S" Currency="EUR">
                                    <TotalFixAmounts Gross="61.36" Nett="61.36">
                                        <Service Amount="17" />
                                        <ServiceTaxes Included="false" Amount="44.36" />
                                    </TotalFixAmounts>
                                    <Breakdown>
                                        <Concepts>
                                            <Concept Type="BAS" Name="Base Coste">
                                                <Items>
                                                    <Item Amount="8.5" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                                </Items>
                                            </Concept>
                                            <Concept Type="BAS" Name="Base Coste">
                                                <Items>
                                                    <Item Amount="8.5" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                                </Items>
                                            </Concept>
                                        </Concepts>
                                        <Taxes>
                                            <Tax Name="Tasas Others" Value="9.68" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                                <TtaCodes>
                                                    <TtaCode>200</TtaCode>
                                                </TtaCodes>
                                                <Total Base="17" Amount="9.68" />
                                            </Tax>
                                            <Tax Name="Tasas Qs" Value="12.5" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                                <TtaCodes>
                                                    <TtaCode>200</TtaCode>
                                                </TtaCodes>
                                                <Total Base="17" Amount="12.5" />
                                            </Tax>
                                            <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                                <TtaCodes>
                                                    <TtaCode>200</TtaCode>
                                                </TtaCodes>
                                                <Total Base="17" Amount="0" />
                                            </Tax>
                                            <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                                <TtaCodes>
                                                    <TtaCode>200</TtaCode>
                                                </TtaCodes>
                                                <Total Base="17" Amount="0" />
                                            </Tax>
                                            <Tax Name="Tasas Others" Value="9.68" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                                <TtaCodes>
                                                    <TtaCode>201</TtaCode>
                                                </TtaCodes>
                                                <Total Base="17" Amount="9.68" />
                                            </Tax>
                                            <Tax Name="Tasas Qs" Value="12.5" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                                <TtaCodes>
                                                    <TtaCode>201</TtaCode>
                                                </TtaCodes>
                                                <Total Base="17" Amount="12.5" />
                                            </Tax>
                                            <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                                <TtaCodes>
                                                    <TtaCode>201</TtaCode>
                                                </TtaCodes>
                                                <Total Base="17" Amount="0" />
                                            </Tax>
                                            <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                                <TtaCodes>
                                                    <TtaCode>201</TtaCode>
                                                </TtaCodes>
                                                <Total Base="17" Amount="0" />
                                            </Tax>
                                        </Taxes>
                                    </Breakdown>
                                </Price>
                            </Prices>
                        </PriceInformation>
                        <OptionalElements />
                    </FlightResult>
                </Results>
            </CheckAvailRS>
        </FlightCheckAvailResponse>
    </soap:Body>
</soap:Envelope>
```