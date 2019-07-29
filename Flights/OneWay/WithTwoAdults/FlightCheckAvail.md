### Request
```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"
	xmlns="http://www.juniper.es/webservice/2007/">
	<soapenv:Header/>
	<soapenv:Body>
		<FlightCheckAvail>
			<FlightCheckAvailRQ Version="1.1" Language="es">
			<Login Email="user@mydomain.com" Password="pass"/>
			<FlightCheckAvailRequest>
				<FlightOption
					RatePlanCode="lZmAomcqR8KeVwNrCaYbm7YYwekKD4434aJbEwrpVfyzE48fargROzff5Ej7JNfS4z++RgVGHpLhJ7FoSGEOI5lY6PZWqXOpyOqeCc56MfwonvEsUc/E5U4f7sP2uorawr2wC/vEH/jGSqcwKuS2CBqnPdOeAoH9sx5Pj2w/RWmRdi9SqpztRWvhI0B+kJIBn12LhxaNPIcukKB0F8myesGtL1/cWAGYh7pY3owqTTzlz+LvItcyZas/RvD7NUi0zFsgj/0Phc49K+13yVY4mBvcqc85ZtONKQIiGeBso16XeT6KhI3LH1tpzrEVJfaukLS4MfOUN74ElUuFHiX1f76vpp62iMG674a8j9yBb/xofJUuAy/URZ1QQkGJXaCm1VO39TTzvVIdoIA4F941RVrfjpR1Vcnr2O9MCpDmERMb7KagE1oP+ryhX4TRvU9nCF5A/qSpWR78RgyqLcoySNQLoycRhSOJu8TgFDILXu8GOLkPK5BNMSpM6t1uIz5Oyf9g3vLZd5FZpDYH2hS+Xzmugh72rJr64v04LnKjFSbM+B+9yqH3qe0H9dCEuwEd1WYVYnEfh0N2WofpFUKF8pYZuXBZul3rXGaacdzR+GnpzdUpDGZvIbyr/OCi188edkJrqIQoIpwIEeVtdRAHGT6OHPBbbu6AE9sZbFszMXDSpWuRMjEZONI81jmnBZ+VzVsmCVGPjRZM0ATq64U7bhDYGaOX7av1Uw5nfTOhNnXFJFCIut0L2JxkD5wfBdBiFn+EiqeEv3d3rpCj/WHxyUoY+nu70vHTibvDfB5jUwVD6eQFtd7X1prWt+QdWx4du4zDyp3yh0mYrns//VHFTV3VYKYYELUjZ8FQtDiUG0noM6dGKxyIrPO6jz/PTHAQAE4h/OFnsqpKfxyGukTMRYGcV7lLf+cr+w++Gat3JFwVZMzz5e2dSeEjarTh7Hv/3Uhr1RiSVOrZ9/FGcOKbvF7HRUELWJx1gwiiF/ZS/ieNSJKAgHpXRWDbofWE1qqaH/TKn3OHarMhtPDAdzk6mKBl1ulbZeS4CGHSS5tzywbPEOK9tpH048zDCU+L4FuIjnA8eXMJe5zUYhgwSsrzcmCDhdkU6q51c7uhXX8TpB/U/W9KFIa/vhV1+D6Tk6gdsDu8yDmVUb77sRquBvJILJR3gYkbJoidaHISQPGsbsfs5L+DB2ALUSeGd5cEtrWJYjiGNowWIoGRjLvGGwOnMnjw/+907NtUIbK/dYF4b2XktUN0WKfhReULwr4ZCXQ5qwHrM8ficIJKA+VKwmQm5oxkw/pCTFKVpssFD8ped+1skVWvAuAyW7ipg1EQrkJgVxYqgSgUn1X39BSoygu24NlZJBmkXuzdT6PWLENdel/vtS2C+JgwMexEX7f0Xe1BhFO7tyxdqDTIByk8IcwLCXsknczUiWa9QlHN/Zk9S8ocBfpJ1h4wMThaOe1SEM++v9fPGO3vte8z+aS4nWyOzQUaII0XwV6H9ndY21NhwrHTq9BisGrZmMPvHS2pUz5f/CpUEm0LUU9OuTJzeBQ8k3xobUABTPTG9yxHoHtZj4caXlVniyW3Wy8P6wyrnTnx8jHxYbHpiBKgt8lgn1YDwRa1a8KygDxQQ/q/gutnmLr/AUUm90awWkV1XrKEVZ/GnfwqZSjMMKQAWbzwuQEFMA=="/>
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
            <CheckAvailRS Url="http://xml-uat.bookingengine.es" TimeStamp="2019-07-29T15:42:38.6162928+02:00" IntCode="OgLn7pMPThIWH5QUYiJ3xIv+NgKZa2vHhaDKHreBbRk=">
                <Results>
                    <FlightResult Status="OK" Direction="Outbound" LowCost="false" RatePlanCode="lZmAomcqR8KeVwNrCaYbm7YYwekKD4434aJbEwrpVfyzE48fargROzff5Ej7JNfS4z++RgVGHpLhJ7FoSGEOIzmNzm7/mgny5pNjgeHekKQooPo/URn1CZbr4Rx4CL99rFTQJBKWz4OEiM9c2C7YhKkVepxpMQ5teSxTGkS91qc3OzwWWPbit7elomwoWN3+RwpWeozKIaWxwUOcaZ4FCmYL7nvDBZlRlOYsWqLvhzOUCDCsY6k9kn4QptfC/sPt4n5Ai5HuqDf5d9SVTN91CJ06xL9P46vgzcx0XGqelCh8dQDFghPo+6QVM2cerO30FS2gTNDBaBkexCCMupJ01qJ6bCRAMKCgxRTWtsJ2lQp/JuCZUJgCSmEDA3Sb4JkaRWrCd4f7F1eUBnqtmTi0TjZ24YVTY1wfDXeOlC2yF1qeJVDW3XJN+sZnoP0Ir6o3im+YQy6uUduPRYYLK943k+aYQgzJIxJnFoiHPKLUwHkK/zmEiNcBdHN1NCFOvvIA5eJYr/rLjbbWVydfmF/iMPeDwGo2BkQtD3JDqGRcT+6+RPMhN461WhvXZsBqR9SERFjH4XNj/LxzWwXxaenMyTdK61l2hmkU6j+Mla1Hy1pQbLqCxmLejpaOH/Mx40aMMbD1gTI9yDamommkE/RzlQFsZ+gtDi0mI+Khx7L/dDhRZSVmdN9AZWjcRXIccPzgd46Rb3cW6IbCn2GT0NLxUqJ5OfsFeS5Qc6g02quchYHo+fS4QfgYTcLBM6W5bdbO7xIlmwR9vYJMaeBKAnQtrGFSzMQ2PpT+MyF/ibIPL5EUj8YkQcrfLBalBnw7iTFDVxM0p7pqddbFpKgLmnfL665UX/LfjFJlICw0IkF+vdcUWwc+U/JHtVOH/WgLoKTUwwyR0u2Fedrb/nMekMJDVTqjEhuLcKc+xPiUMcpdOCfOKbQOXfIxSRLcyrHB4G1NuHW7KL9g6+qU+FYZ9NJ5Gj1zOSYJU38PpKxDbKrm5Oww5p5rDndbTWZSb8p7TZOlsPzhGXsD+xXdM3K47DvV5k0CVG79FaIBk5aoSfhufEYE7M27TbKm6kX8/FVcLhmr8tC9mdL8D7INwrgKeee9Jpp4ypKSAAIjit7wHm611iywzRmDyfBJLQ4H9BbCx+Hvw6KcnNWVp6m85EbL15yz3I+sxnxDKLTagfggCFzXPIOE3z0n4kqW72jJB8fo8kB3nqhtdRBF5DicJECxQKpXClOzYjqsesR+MhcQHv4iGaE6ZrKx0NrD7yqj+FUEeA++83+GAB2ysAf8V0r3XlyE2YH0TDwgdt15/fuMZtlZXwFNj6RaWPJbx1M7Db50V19KINSkO2io0deYS5MN17UKyJWfUiXDr1Forx0bQ+gTHFbjO3gAw8bhnSONZjIdxj5yD8tCQ+LckJ6N78VmW49//f2+EU41lRtQJgkzAx7Jx6U2+sjsRCfAZYesiY5YNOgIYOTDYQV5izd7/0jQwxTW28O//ed94M3YEJw7+2j0Jx2VfGZ6XENrUp5SxFA2PDkum3l0oRdkw8Q6iyf1ZLshrOj5lUdqYxhvFJ7J//JlZmiePAhPCSioM9SnX+GVfoVS63wKQl61xW/sZTrFk45D8A==">
                        <PriceInformation>
                            <Routes ValidatingCarrier="TK">
                                <Route Origin="39681" Destination="37786">
                                    <Segments>
                                        <Segment DepartureAirport="MCO" ArrivalAirport="IAD" DepartureDate="2019-10-16T18:59:00" ArrivalDate="2019-10-16T21:08:00" OperatingAirline="UA" MarquetingAirline="TK" FlightNumber="8613" JourneyDuration="P1DT12H41M0S" Class="Z" Cabin="C" AirplaneType="739" FareBasis="Z3BOXYY1" />
                                        <Segment DepartureAirport="IAD" ArrivalAirport="IST" DepartureDate="2019-10-16T23:00:00" ArrivalDate="2019-10-17T16:15:00" OperatingAirline="TK" MarquetingAirline="TK" FlightNumber="8" JourneyDuration="P1DT12H41M0S" Class="Z" Cabin="C" AirplaneType="789" FareBasis="Z3BOXYY1" />
                                        <Segment DepartureAirport="IST" ArrivalAirport="MAD" DepartureDate="2019-10-18T10:15:00" ArrivalDate="2019-10-18T13:40:00" OperatingAirline="TK" MarquetingAirline="TK" FlightNumber="1357" JourneyDuration="P1DT12H41M0S" Class="Z" Cabin="C" AirplaneType="73H" FareBasis="Z3BOXYY1" />
                                    </Segments>
                                </Route>
                            </Routes>
                            <Prices>
                                <Price Type="S" Currency="EUR">
                                    <TotalFixAmounts Gross="5941.42" Nett="5941.42">
                                        <Service Amount="5382" />
                                        <ServiceTaxes Included="false" Amount="559.42" />
                                    </TotalFixAmounts>
                                    <Breakdown>
                                        <Concepts>
                                            <Concept Type="BAS" Name="Base Coste">
                                                <Items>
                                                    <Item Amount="2691" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                                </Items>
                                            </Concept>
                                            <Concept Type="BAS" Name="Base Coste">
                                                <Items>
                                                    <Item Amount="2691" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                                </Items>
                                            </Concept>
                                        </Concepts>
                                        <Taxes>
                                            <Tax Name="Tasas Others" Value="279.71" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                                <TtaCodes>
                                                    <TtaCode>200</TtaCode>
                                                </TtaCodes>
                                                <Total Base="5382" Amount="279.71" />
                                            </Tax>
                                            <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                                <TtaCodes>
                                                    <TtaCode>200</TtaCode>
                                                </TtaCodes>
                                                <Total Base="5382" Amount="0" />
                                            </Tax>
                                            <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                                <TtaCodes>
                                                    <TtaCode>200</TtaCode>
                                                </TtaCodes>
                                                <Total Base="5382" Amount="0" />
                                            </Tax>
                                            <Tax Name="Tasas Others" Value="279.71" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                                <TtaCodes>
                                                    <TtaCode>201</TtaCode>
                                                </TtaCodes>
                                                <Total Base="5382" Amount="279.71" />
                                            </Tax>
                                            <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                                <TtaCodes>
                                                    <TtaCode>201</TtaCode>
                                                </TtaCodes>
                                                <Total Base="5382" Amount="0" />
                                            </Tax>
                                            <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                                <TtaCodes>
                                                    <TtaCode>201</TtaCode>
                                                </TtaCodes>
                                                <Total Base="5382" Amount="0" />
                                            </Tax>
                                        </Taxes>
                                    </Breakdown>
                                </Price>
                            </Prices>
                        </PriceInformation>
                        <OptionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </OptionalElements>
                    </FlightResult>
                </Results>
            </CheckAvailRS>
        </FlightCheckAvailResponse>
    </soap:Body>
</soap:Envelope>
```