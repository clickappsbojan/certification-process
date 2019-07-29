### Request
```xml
<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope" xmlns="http://www.juniper.es/webservice/2007/">
    <soap:Header/>
    <soap:Body>
        <FlightAvail>
            <FlightAvailRQ Version="1.1" Language="en">
                <Login Email="user@mydomain.com" Password="pass"/>
               
                <Paxes>
               	   
               	    <Pax IdPax="1">
               	    	<Age>28</Age>
               	    </Pax>
               	    
               	    <Pax IdPax="2">
               	    	<Age>28</Age>
               	    </Pax>
               	</Paxes>
                
                <FlightRequest>
                    <SearchSegmentsFlight>
                        <SearchSegmentFlight Cabin= "Business">
                            
                            <CountryOfResidence>SA</CountryOfResidence>
                            <Routes>
                                <Route Origin="39681" Destination="37786" Date="2019-10-16"/>
                            </Routes>
                        </SearchSegmentFlight>
                    </SearchSegmentsFlight>
                    <RelPaxesDist>
                        <RelPaxDist>
                            <RelPaxes>
                                <RelPax IdPax="1"/>
                                <RelPax IdPax="2"/>
                            </RelPaxes>
                        </RelPaxDist>
                    </RelPaxesDist>
                </FlightRequest>
                <AdvancedOptions>
                    <CalendarSearch>true</CalendarSearch>
                    <ShowBreakdownPrice>true</ShowBreakdownPrice>
                    <UseCurrency>USD</UseCurrency>
                </AdvancedOptions>
            </FlightAvailRQ>
        </FlightAvail>
    </soap:Body>
</soap:Envelope>
```
---
---
---

### Response

```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <soap:Body>
        <FlightAvailResponse xmlns="http://www.juniper.es/webservice/2007/">
            <AvailabilityRS Url="http://xml-uat.bookingengine.es" TimeStamp="2019-07-29T15:40:04.3457826+02:00" IntCode="1cqKkp17HGhWy7G3XRJdoY7clywdW6SJs7rxtlGokm8=">
                <Results>
                    <FlightResult FareType="PUB" AvailableSeats="4" Number="1" Direction="Outbound" LowCost="false" RatePlanCode="lZmAomcqR8KeVwNrCaYbm7YYwekKD4434aJbEwrpVfyzE48fargROzff5Ej7JNfS4z++RgVGHpLhJ7FoSGEOI5lY6PZWqXOpyOqeCc56MfwonvEsUc/E5U4f7sP2uoraGH0fIt8ehNKwhVvRK7r5jiWxMWEi0xLz1iEB5YDghdrLWqyl+Wyr5Ekgp1J4F8Mw6zUCwjaTeFy+o7Y3zg23pO4LnHSs9tAOTNQcVUcg4IXIQ8GxTzcb+rsAmXkPiRcYNLC/on9nn5oaP1LKHAzRIgi2T/PuviOxGXHQ1nP9s/WblPAbESk6nuha6vkeifBWqnsDoX2Ik+JV0n5QdLfLApKhv3dsvNqh4JohwhVD8KFiRdejoRqDanblyd7llrvB4PqAhqQSKXtTLEHy3E5/Z87vWVKQROec/SlEJp3gwSJiknnhfiYrJW5w2xl6Tr5pv9+JLYHr03+v3yQoysxbUkZuct/IH4jgniFol0mqcUMNJ8xkExrjY3813XONSK+i8b9DXlCEDP6BrYwjOKlEHemarxF8F0nacZmyGiz0JghMJiBuhcn5DWm/X5C/Vyat72XAiqihmitk5JnwpTYOoXISlkrp1mA4Byi0f45uQ8xxmDotPM1W/yRlOx6vJW+jVym65RLjo3EpO6Id+X7mFOVhkDHqhpbKFXHlAApbd80gF6gjB+SLqXb8n/D4gcv38CwmL9Ez54sWH0z198y8atx9PsoaAz3pzRyG59lF0kukGVaPZqdpler3L1ky58Rd/rGpks493cz0WjjGLl/HC7yBCOv7GyO98Mefsn9y+rYHOxfOX36CP3p+6GQMFkTmXy3Z2UeDFDltmq9KLrG2ZXcpTGKNWwJOtP0Q9LlpqQOID7fNpZF/IEK85koKBDHT0VTlpjvHjAaPZZXxNOtupT2fFD3/+FdM8VVEG2peQ33kwEDFlVWXBIZl7vpD6K+DubDlJg49GUBn48YMXWALGXKAQB/fnwfBEo8KzSjFXISrWsrLxA0rjHT6pn4BkRShyMU+qGHlX4GqPQ6vNyb6jYw/cKMlYLfqr1k5chJdeBnwezJrHP4dSYy/ELcnn8Huljetv/DsABppi335Hnc8EcoPQEASkw/AP/fThBZA5b5/Wp/8uK4LCl0aibLi96m+SF6/GX/rJBHPGziv7WAc/HQ4TyMkIMo5f8j6+hrk0NwNEIhuS+VbgA+dKW/pyipf38cYbdUo8Pne8GYNC8WvUDvmh6ItHDkh2omLyN1TWDM5ZLaAOigW1bEBpeR5QN2zC2m1umWNBuRgTGy4lSeujPTw1x+GUeBxlUnXv/EBab9/XK4xvkbvz5wjlsZMiisDCsls2dwznqtz+5lpxGp35mva1//ZYHv51Z2yisfwn4lsPGcVkmDcN/4/RdtSKlFrGVSWISZuVYDiXQV7XzTJcB6vWA5Y16m9QBtLFVuH7ya8bA6x0WDoE/eeMKpGNTI6J7iq5e0qx5rLwsYi3WogWzeL1dsYe1lBM6BV0Zh+Rbk0LQOBxy1GJc8xfSQjOE1ssJcYBGqcVZgErTLsGknet3+tSr8THMHbZH2j2e1CSgPF/8+Fn/ltFZA6EtB1BCPLAxOR632E4AHoDndz5w/VPwiiRgQCgivNnO0iB6E67Vj1r67mXCKUsu/BMx8WJY2O31L+euuctcYvSC9NF9P6Hw==" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="TK">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="IAD" DepartureDate="2019-10-16T18:59:00" ArrivalDate="2019-10-16T21:08:00" OperatingAirline="UA" MarquetingAirline="TK" FlightNumber="8613" JourneyDuration="P1DT9H36M0S" Class="Z" Cabin="C" AirplaneType="739" FareBasis="Z3BOXYY1" />
                                    <Segment DepartureAirport="IAD" ArrivalAirport="IST" DepartureDate="2019-10-16T23:00:00" ArrivalDate="2019-10-17T16:15:00" OperatingAirline="TK" MarquetingAirline="TK" FlightNumber="8" JourneyDuration="P1DT9H36M0S" Class="Z" Cabin="C" AirplaneType="789" FareBasis="Z3BOXYY1" />
                                    <Segment DepartureAirport="IST" ArrivalAirport="MAD" DepartureDate="2019-10-18T07:05:00" ArrivalDate="2019-10-18T10:35:00" OperatingAirline="TK" MarquetingAirline="TK" FlightNumber="1857" JourneyDuration="P1DT9H36M0S" Class="Z" Cabin="C" AirplaneType="333" FareBasis="Z3BOXYY1" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="USD">
                                <TotalFixAmounts Gross="6612.4" Nett="6612.4">
                                    <Service Amount="5989.8" />
                                    <ServiceTaxes Included="false" Amount="622.6" />
                                </TotalFixAmounts>
                                <Breakdown>
                                    <Concepts>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="2994.9" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="2994.9" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                            </Items>
                                        </Concept>
                                    </Concepts>
                                    <Taxes>
                                        <Tax Name="Tasas Others" Value="311.3" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="5989.8" Amount="311.3" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="5989.8" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="5989.8" Amount="0" />
                                        </Tax>
                                        <Tax Name="Tasas Others" Value="311.3" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="5989.8" Amount="311.3" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="5989.8" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="5989.8" Amount="0" />
                                        </Tax>
                                    </Taxes>
                                </Breakdown>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-01</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="4" Number="2" Direction="Outbound" LowCost="false" RatePlanCode="lZmAomcqR8KeVwNrCaYbm7YYwekKD4434aJbEwrpVfyzE48fargROzff5Ej7JNfS4z++RgVGHpLhJ7FoSGEOI5lY6PZWqXOpyOqeCc56MfwonvEsUc/E5U4f7sP2uorawr2wC/vEH/jGSqcwKuS2CBqnPdOeAoH9sx5Pj2w/RWmRdi9SqpztRWvhI0B+kJIBn12LhxaNPIcukKB0F8myesGtL1/cWAGYh7pY3owqTTzlz+LvItcyZas/RvD7NUi0zFsgj/0Phc49K+13yVY4mBvcqc85ZtONKQIiGeBso16XeT6KhI3LH1tpzrEVJfaukLS4MfOUN74ElUuFHiX1f76vpp62iMG674a8j9yBb/xofJUuAy/URZ1QQkGJXaCm1VO39TTzvVIdoIA4F941RVrfjpR1Vcnr2O9MCpDmERMb7KagE1oP+ryhX4TRvU9nCF5A/qSpWR78RgyqLcoySNQLoycRhSOJu8TgFDILXu8GOLkPK5BNMSpM6t1uIz5Oyf9g3vLZd5FZpDYH2hS+Xzmugh72rJr64v04LnKjFSbM+B+9yqH3qe0H9dCEuwEd1WYVYnEfh0N2WofpFUKF8pYZuXBZul3rXGaacdzR+GnpzdUpDGZvIbyr/OCi188edkJrqIQoIpwIEeVtdRAHGT6OHPBbbu6AE9sZbFszMXDSpWuRMjEZONI81jmnBZ+VzVsmCVGPjRZM0ATq64U7bhDYGaOX7av1Uw5nfTOhNnXFJFCIut0L2JxkD5wfBdBiFn+EiqeEv3d3rpCj/WHxyUoY+nu70vHTibvDfB5jUwVD6eQFtd7X1prWt+QdWx4du4zDyp3yh0mYrns//VHFTV3VYKYYELUjZ8FQtDiUG0noM6dGKxyIrPO6jz/PTHAQAE4h/OFnsqpKfxyGukTMRYGcV7lLf+cr+w++Gat3JFwVZMzz5e2dSeEjarTh7Hv/3Uhr1RiSVOrZ9/FGcOKbvF7HRUELWJx1gwiiF/ZS/ieNSJKAgHpXRWDbofWE1qqaH/TKn3OHarMhtPDAdzk6mKBl1ulbZeS4CGHSS5tzywbPEOK9tpH048zDCU+L4FuIjnA8eXMJe5zUYhgwSsrzcmCDhdkU6q51c7uhXX8TpB/U/W9KFIa/vhV1+D6Tk6gdsDu8yDmVUb77sRquBvJILJR3gYkbJoidaHISQPGsbsfs5L+DB2ALUSeGd5cEtrWJYjiGNowWIoGRjLvGGwOnMnjw/+907NtUIbK/dYF4b2XktUN0WKfhReULwr4ZCXQ5qwHrM8ficIJKA+VKwmQm5oxkw/pCTFKVpssFD8ped+1skVWvAuAyW7ipg1EQrkJgVxYqgSgUn1X39BSoygu24NlZJBmkXuzdT6PWLENdel/vtS2C+JgwMexEX7f0Xe1BhFO7tyxdqDTIByk8IcwLCXsknczUiWa9QlHN/Zk9S8ocBfpJ1h4wMThaOe1SEM++v9fPGO3vte8z+aS4nWyOzQUaII0XwV6H9ndY21NhwrHTq9BisGrZmMPvHS2pUz5f/CpUEm0LUU9OuTJzeBQ8k3xobUABTPTG9yxHoHtZj4caXlVniyW3Wy8P6wyrnTnx8jHxYbHpiBKgt8lgn1YDwRa1a8KygDxQQ/q/gutnmLr/AUUm90awWkV1XrKEVZ/GnfwqZSjMMKQAWbzwuQEFMA==" Status="OK" Source="Amad">
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
                            <Price Type="S" Currency="USD">
                                <TotalFixAmounts Gross="6612.4" Nett="6612.4">
                                    <Service Amount="5989.8" />
                                    <ServiceTaxes Included="false" Amount="622.6" />
                                </TotalFixAmounts>
                                <Breakdown>
                                    <Concepts>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="2994.9" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="2994.9" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                            </Items>
                                        </Concept>
                                    </Concepts>
                                    <Taxes>
                                        <Tax Name="Tasas Others" Value="311.3" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="5989.8" Amount="311.3" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="5989.8" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="5989.8" Amount="0" />
                                        </Tax>
                                        <Tax Name="Tasas Others" Value="311.3" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="5989.8" Amount="311.3" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="5989.8" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="5989.8" Amount="0" />
                                        </Tax>
                                    </Taxes>
                                </Breakdown>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-01</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="7" Number="3" Direction="Outbound" LowCost="false" RatePlanCode="lZmAomcqR8KeVwNrCaYbm7YYwekKD4434aJbEwrpVfzZrpgggMY6/Hhjpfr4PLpqAC50HLToYsyXjL95CT/v0FFeeuAFW+4MlXtxEZR4ZOAYEHCYNK14wEuXgXIqnxetf5HYxI3uwILc/su4YiELbN1Ku6zgw6LSchLWVn8ONIMPSzp3hqFBI/Q5tVzyq/UYE4SsPCZEcLg6F5BryITUFqep/uAJg3ZI/FhbjAA90ZWtrrEOqzSOyotpnWX2qi6OrLpLD7fq3Z5f8+o2yvjSBQ4RX2PqPQATaVXI38FhO/IGxOr0nhgkTxcZEaSW64VnjfwO7Az2b1TiqgNdnHZtqEbAcwD0PlHGUqQl4t85k9n051oDJ8gJpfQ1T7E1k0m7hJk/2RWKa8eby/5v9oO6Y3xYe/YATXOXx6f4OJIDEEwXxE/KcvW0DV7iwl3NywQu1TZX/C8KOWsugGJ5n9OW7jp6geG+d2WMx/TpGXGGPjZ14RGeykjKDb8rHR9/R+F43jv/JRplY/yYUBOVWeMWTpUcjAzXLkK9b6omCH0kByOjVDqn5qjpIjuWqR2pIDVdV3n9RReffzlXaY4JkPtueFCY1C39QteWYCNlZ9v03J6aYa+Agm5+rSdr25nnrXj//PDcb71/ogMxOONLo8tJUg1IUOxDj0yrE4agLpqYDKpkoHmREGcGnDtWAK47lyqaPs1VoO0f0C2+gTBAJWmJhPIOmOuTb2KMtlJT3Mt2R8dmGVk7f1E8QBpZzlg9aOLYT/ZdMKSvX7W1V2s/23vP7u3JOIXUy7XCq9gjs+5cyWQGWp8pW1NP9POrLnZ2h1FtHxmTQ4KYoWUdReZOMVbb/rW5vMlFm2vUko4bztKPoHNgW/5qq2YMo7Ya8svns0CMCef48lqDlUlNlNuw04VfONn7dyaYk3+uAzwp6qP/s9f/owI5y6vzcnv4fh1NmC3lPwen7ZzMH7V+0qDEWVQBdMvpiv/Uo59MKPATz8Rh0WD8xtRYyOU+TaWj3h2DkavOqk4yUC8WZhEDsK7wTC2YcF9/unV6TNUopxx0waeE970oaFeg1mmgj64nUoUKBFzN1MVAyBwfLYzYNmrVNPTnnIxgAicVQLMAGL/scJxk6yNAMO/SB2wsNxiYltpGrPSAQ1V9NYhyptkzjEP3CDO4LsCQCBmEpKzG6mquTZ3j204P9xbDCDxM/FINevm0KYcJEwp/ylOBEb6Q7fNHYeCpjE+yC74pWJE1Ndk4x/CzMmUZRBbSSuFf0Whq5wuqxTe/juuM8VmK5NXjTKnzGMxnMGjXvWfWhqisOiw0ijscIp/GmNgF6LZ1gCNc4GN31XmMWHYzPUmpIJ4GKEgFyRYY0Q==" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="EK">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="DXB" DepartureDate="2019-10-16T14:10:00" ArrivalDate="2019-10-17T12:20:00" OperatingAirline="EK" MarquetingAirline="EK" FlightNumber="220" JourneyDuration="P1DT0H10M0S" Class="I" Cabin="C" AirplaneType="77W" FareBasis="IOEASUS1" />
                                    <Segment DepartureAirport="DXB" ArrivalAirport="MAD" DepartureDate="2019-10-17T14:30:00" ArrivalDate="2019-10-17T20:20:00" OperatingAirline="EK" MarquetingAirline="EK" FlightNumber="143" JourneyDuration="P1DT0H10M0S" Class="I" Cabin="C" AirplaneType="388" FareBasis="IOEASUS1" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="USD">
                                <TotalFixAmounts Gross="9710" Nett="9710">
                                    <Service Amount="8231.24" />
                                    <ServiceTaxes Included="false" Amount="1478.76" />
                                </TotalFixAmounts>
                                <Breakdown>
                                    <Concepts>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="4115.62" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="4115.62" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                            </Items>
                                        </Concept>
                                    </Concepts>
                                    <Taxes>
                                        <Tax Name="Tasas Others" Value="739.38" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="8231.24" Amount="739.38" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="8231.24" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="8231.24" Amount="0" />
                                        </Tax>
                                        <Tax Name="Tasas Others" Value="739.38" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="8231.24" Amount="739.38" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="8231.24" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="8231.24" Amount="0" />
                                        </Tax>
                                    </Taxes>
                                </Breakdown>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-10-06</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="4" Direction="Outbound" LowCost="false" RatePlanCode="lZmAomcqR8KeVwNrCaYbm7YYwekKD4434aJbEwrpVfyzE48fargROzff5Ej7JNfSu3kWhm40IuoY0DNsDoZxDX7ey1v8/CIzcI6Dez785Qy/TKoQqLvl8yJ4V7vcKxzhiGLOJvy2s4DiU6J2QSOZFG57cAo76za2522cppbOIGR14qpeHUdoEXSaAUbEngweW6lCnJTgZ5KdsAqQ4PsfxKNO9y6CyVtl62cvRTif5UTyzNCJ5z/uPfIYChckIdY/nV11RZr5urge2ZT2CSYK+ZnxOXe4t6wNyb3RtRXVak4+R9aoyAla4FsnArLS61QXAKpsFMQAo6kjCu6gtkf014eH3pnIG10pGQsiPDl8IKMj5h9/EBmMruKZxBPRkls5/MEdQ/X/6yGB3+QPqb5IAeeT4suin+p340Th1nPztPKuB5zzxHXe9tLpjAeOT1xmq1enOH20F4BmlubHpt2BxWWiOlSlgQfybN2TDLJ4B+B1u6vPNP66A5pvcANz7ZaJvdlOrdzLrMJWp35y6xvH+tNYOXqFDurP4+6MgkFLSnoA2KxyLHSm9hS6w2WXxYynZ88LUuZSlfswRgVQ60gRp0GfYAuQFG4vAFgEcSZ4EOBf/WSezQEbM7Z2V8mN0OVScv9BNeOHC7HuweLt28CbMoDsaCAS/UonUGTT0Q80LuSWat1pwk+kvmX6LytMgFGBw8pFw39HAwkqpHkRTtMh0R9ZWi2lYFAVsb2f353nNjeTj0J0n+UMo4OPN9aKyBIRaTm3IX4hBEmK084cNdm2/bwjz23GLnP3LNEEhGPP7vDpKyYWz7XJJmWIQnBvEO66x4RFATay7yYJ8ctEO+MCcVATwv6mYTo1B0ZAFc5xS2lJ3eOn4iQJAoSZHvshuDbVRzNUZgQ+uyBuKAyotc9juJ0NxU3ERdHEKCBJfY9IfgqTMK1X7ighMrbFKsyqV7FdqloBFh38W23JHEKNbMgFmZkX7L1Jka74csf856VmpAyQgy7NOwWRe2c9v2tZXVjPfWmvNF/fDIvppS7apVKnLt4NlKV1zUeB7VZUvPf69dQX7VS1e+vx3R28NtoEmgksNbO5/mFy68ugJux0xAczOD633W/wEJVmMTsskjH0U4tVQ1UDOrRPkRECtSUSX5p0ExKJ5N/COfyofr6cUlwYN9RMUpbxeNqtknpfLRWKAYr6i4S/SDSBeHS0GFtzee4rI6TnLChQqK2sKkxuUdTWsqtvbAy5G2v0tKb5m47SNq6nk2cPnHDr5aHbRkRH63y2pKIcg5Bmbz41dbxfA7bp5Ym9FzhO2N7fMkjoYFtof/d+QQgrna941yQmiYG0E80n2VMdXricV+0cQDLNisoeaw==" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="AF">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="JFK" DepartureDate="2019-10-16T15:12:00" ArrivalDate="2019-10-16T18:00:00" OperatingAirline="DL" MarquetingAirline="AF" FlightNumber="2985" JourneyDuration="P0DT12H3M0S" Class="J" Cabin="C" AirplaneType="321" FareBasis="DN1H01D1" />
                                    <Segment DepartureAirport="JFK" ArrivalAirport="MAD" DepartureDate="2019-10-16T19:38:00" ArrivalDate="2019-10-17T09:15:00" OperatingAirline="DL" MarquetingAirline="AF" FlightNumber="3679" JourneyDuration="P0DT12H3M0S" Class="D" Cabin="C" AirplaneType="764" FareBasis="DN1H01D1" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="USD">
                                <TotalFixAmounts Gross="10545.92" Nett="10545.92">
                                    <Service Amount="9272.94" />
                                    <ServiceTaxes Included="false" Amount="1272.98" />
                                </TotalFixAmounts>
                                <Breakdown>
                                    <Concepts>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="4636.47" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="4636.47" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                            </Items>
                                        </Concept>
                                    </Concepts>
                                    <Taxes>
                                        <Tax Name="Tasas Others" Value="636.49" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="636.49" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="0" />
                                        </Tax>
                                        <Tax Name="Tasas Others" Value="636.49" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="636.49" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="0" />
                                        </Tax>
                                    </Taxes>
                                </Breakdown>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-01</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="5" Direction="Outbound" LowCost="false" RatePlanCode="lZmAomcqR8KeVwNrCaYbm7YYwekKD4434aJbEwrpVfyzE48fargROzff5Ej7JNfSu3kWhm40IuoY0DNsDoZxDX7ey1v8/CIzcI6Dez785Qw4F9SW+NBUPmClPGVUlpHBH8z0VcYJTNtHwDunFoJqyVFrXbETDdq2mQzfF/BZ6YCu8uGaTbfzf86OOyi5F7QAqf93jraqUFg4Kqad+YdbrYm8UUc/LcdJZjJr9waWqQ5h7aVJREOQgxN/ugf69tN+rfFQWwMLU+y2div547I2Xvy86g9YyNoj/M4VxdPukWNkmIHmjrqNeIrjf7z30zjOBdsV2flqrJ80uStLqINxhM3B0URALO12EkSTR56njbN5OKzJgx5UkTcayVkrHx5ORkF73cNeo2TC4E79nbCNRCh/xWGgpYn67OXW8stqV/6krwnyiVvEb1CrUnatNWA8fxjVSS9IPWS8ygakSvhhguByOkO/DqVsIOCRez+25qvkaQFZ2xQDSwxKQYi01V2pmPszulMRb7f72UHr1iFixdEnlNfyjhn2j2DBFS50H7R3JMDBVcHbM9HF5jQV6Y3tXF75kQ5+B5hn3ykE75pnwgnIATJpzhSVuD4N1AxYr2YwWVS91H3PjV62zTo+VeilVULHPIR0iHx94SYDIETmCxmUIN2NDguwaZuy16uEWuqhqe54RAE9HYmIdfanXSm6I8JoUnHBJZ7MjCdglj+I83tLbyJrk6K6M+kIqnciDhLeu7VxEkn717shvInsSsv5xnQ9CyGnxjIHnVmhc+4Mq4MCRKxAXQy9eY7j1um1ortqU/WJ0TEUYQpgBdRN/4EASuJc3ktAv8qxgHpjZMh1IXlBEGcMBvhG7uvw0jovUGXP4TYk7vPGBr97RfqCKxj2A5e8Jkm/qLSvife+udyFuN0oLvsKc9CPoDE1i/nRkxkUdWGAHcN1lrsw9v1j2rqk1BPDo/k5NDNpoQ9t7ltgT3X6NIINOX2k8pfYGTG2y6S5HkZSZIG3g2DP1Br2Ng4N451B6pNEf8J5dVQXAU0frv8youHbTAvi8+O7N5LkMVQuaIGIvInpNmpK0vOZ4gz+SFlPjRU7u3mMEeoOHKv5WyGSZnN4vbjWz5xD9kcKzEq9Qy6j5zTT7Bb8N8NJia+JOOjG6Z3TR7jvNP9eBzxd/kAQl/qKqWxDnKu1ZAOQF0VvkSxDtEjwqn1PvP/QPr+KR5GmrAlq9AI5bOW3uRk7xlttf5kKRsFRW5V3ryn2DNE0lf/hyF/0WXIOADMI1j3UAD9ohO4p3pCvuHvMe3OQT1tQAG0Re/BpH2crm6mf6oNh3aKOqQv4LdfOnhjVWGihRySQV6cag3os534bAToNVg==" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="AF">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="ATL" DepartureDate="2019-10-16T14:20:00" ArrivalDate="2019-10-16T15:53:00" OperatingAirline="DL" MarquetingAirline="AF" FlightNumber="2739" JourneyDuration="P0DT12H15M0S" Class="J" Cabin="C" AirplaneType="757" FareBasis="DN1H01D1" />
                                    <Segment DepartureAirport="ATL" ArrivalAirport="MAD" DepartureDate="2019-10-16T17:55:00" ArrivalDate="2019-10-17T08:35:00" OperatingAirline="DL" MarquetingAirline="AF" FlightNumber="3627" JourneyDuration="P0DT12H15M0S" Class="D" Cabin="C" AirplaneType="764" FareBasis="DN1H01D1" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="USD">
                                <TotalFixAmounts Gross="10545.92" Nett="10545.92">
                                    <Service Amount="9272.94" />
                                    <ServiceTaxes Included="false" Amount="1272.98" />
                                </TotalFixAmounts>
                                <Breakdown>
                                    <Concepts>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="4636.47" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="4636.47" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                            </Items>
                                        </Concept>
                                    </Concepts>
                                    <Taxes>
                                        <Tax Name="Tasas Others" Value="636.49" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="636.49" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="0" />
                                        </Tax>
                                        <Tax Name="Tasas Others" Value="636.49" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="636.49" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="0" />
                                        </Tax>
                                    </Taxes>
                                </Breakdown>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-01</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="6" Direction="Outbound" LowCost="false" RatePlanCode="lZmAomcqR8KeVwNrCaYbm7YYwekKD4434aJbEwrpVfyzE48fargROzff5Ej7JNfSu3kWhm40IuoY0DNsDoZxDX7ey1v8/CIzcI6Dez785Qz+UcTlH0RtmT1kkiqqiI+r4qgyfdNxlEYy8wfzJzIEQ7bLl5flO/DBZQpkHigb+z3A/VoGiysEg9l1nrTPgLLT5YbzYRrKPTxX8mzENvTUIM5R9yikrxVWQWiSPo7FrWusDNd9n8vBu2pC0WGcI00QB6vudtafqU4Mzf/Jnmu1s6Fas0twRFJIsTu7cuhLGWegck01yswISxoxEGbUYLBP0yG3ljFL9NWDmJCMsYA7HM/md4Qo8yPbgLflZwoNUXgqlbPA5EaWogvUoNZ86sw3IAHVnJ6XnJgcbxDZ1scYkY6jDev2Ukq/7N88VTVWKjAWHU54v76fyz72/ZEAbHjaoXdfKlVwilzLoZ0QDA9p7DPdS2bi+fL239lC+2gt7cG0f13nloTDBi1iLRWyzf6wIjKd4L8OKe0hvcnWlt96LruwDqMS2PVlxVeMX4wSR+9zYnje95NmQi6ey1QSv+3Ojrm4uGgqgc9NZk2RfSOclRMgIMVZbwGMOYATDClawiUL6m/2Zv5rXYAdhOJyKHMQjFgwrcBeOHPBjrmtTBqmbqqU0oFo8GKm/RANvTi+aHHSd6y+LPuekY5qJuXt6sbnhMZAvxp6/i923vWhAPN4s1XNsqgZqd8Ka/djL4bD+rmllrLuZGtYoftwOpfl402HJuA8TiL7E/RLWSZfpn8lkcekL9tz/EYOnWAMZayxaoDrvqHv94bW8KFL2mBhzM7AYh51xe4zVwMkhCcs/AxdHsx+eJsD2zbXR15dqm2erKfEx6aVDr2NDw0Q6XQoOnfvlABU2wFCoO3TtoMjdJmnqA36EMJ974RJM72VJ9cCPKDe6dvosLAdEfh2hNzu/t2Lr3s7N9cDZSMGoT5aWYMVTdwVOv2t4QRAf9oA8fXgpC6axPSoejOPUIY8DIEwevcVFFkvIeBz+2EwOMfv7lEGB0hxs8Cy7AhjhZUpg/9r82ydmnCWfk8a9eS/zEBsf89bXQdSLm4n4Ke+fnGJqMRRg4n1dUKb8YHynzXF1uwvzDzDX+uL8ekSd0ucE9Ub3OinftLrParvOFfthMskZy84NptdDl6ot2aBUFqmFPLM/fpAfPppsNu15GaywVFPAdh148E/aBxP8stwr2WEB6WS/I3NeZjmi1SY0WEX9c7bCOvtrRZhacAHD0CfjSzTLPazi1UirkaPvuDDWFbJ5FJ230wqEGj8LYsdncrx0OfXmdlxvktgM5SeTUjRxFEHVdK4gOoqFt+5TpSqjqCtN+cfkg==" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="AF">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="ATL" DepartureDate="2019-10-16T13:25:00" ArrivalDate="2019-10-16T14:57:00" OperatingAirline="DL" MarquetingAirline="AF" FlightNumber="8590" JourneyDuration="P0DT13H10M0S" Class="J" Cabin="C" AirplaneType="757" FareBasis="DN1H01D1" />
                                    <Segment DepartureAirport="ATL" ArrivalAirport="MAD" DepartureDate="2019-10-16T17:55:00" ArrivalDate="2019-10-17T08:35:00" OperatingAirline="DL" MarquetingAirline="AF" FlightNumber="3627" JourneyDuration="P0DT13H10M0S" Class="D" Cabin="C" AirplaneType="764" FareBasis="DN1H01D1" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="USD">
                                <TotalFixAmounts Gross="10545.92" Nett="10545.92">
                                    <Service Amount="9272.94" />
                                    <ServiceTaxes Included="false" Amount="1272.98" />
                                </TotalFixAmounts>
                                <Breakdown>
                                    <Concepts>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="4636.47" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="4636.47" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                            </Items>
                                        </Concept>
                                    </Concepts>
                                    <Taxes>
                                        <Tax Name="Tasas Others" Value="636.49" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="636.49" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="0" />
                                        </Tax>
                                        <Tax Name="Tasas Others" Value="636.49" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="636.49" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="0" />
                                        </Tax>
                                    </Taxes>
                                </Breakdown>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-01</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="7" Direction="Outbound" LowCost="false" RatePlanCode="lZmAomcqR8KeVwNrCaYbm7YYwekKD4434aJbEwrpVfyzE48fargROzff5Ej7JNfSu3kWhm40IuoY0DNsDoZxDX7ey1v8/CIzcI6Dez785QztM4k5BL2LY6yDNvmQr6ZemxPoebPxIhHUhfLtI1SNDaW8PDkblWOGuk0EqXJclKgcL0WqmywLKvDK12RJ/g8K0O7rvfC+INd2xkcT8v0WFLpyxn4ZNQcSEMRm7IcXIWPqXfMpHgclW2Dm7wZEdObZE8stIw7KqGewrC9gmdjnuwdSq/Sfe0t4aMWF/C50Bhpb/uW9RJRImecfIkV8jTe22ArtGDVV7U7nZiilV59eDRGDmSZVulBevMj0JX3LIoJEew4UIyUKF1FznFEvcHv4iswZv+w2UFSPh5DfzTinUVoKuh+QVNjYbk3zNzDrNr3cy+ifTFLtV4QH8AqvE+uXn/QTpNQqu4iXvwBdR+tJLhD/iyXDVZ/2afhmITug1+5HVZITUws8hoqSWGJ4RIX+Y+fm/Zv2JMvfpmoZY9zmuthBa205X8nlgcqmI571J9wO2KtfD7CKvyTSCnkSYRZj0wW64CYEAvAJd5bcVzzvDvOSMJ85Z/txyMaidgN0o9YtpU+/P2tmYdXpKPmoxDgjOpjf/gOVGdguVCL/t3bB0qVkcoH8lxVRhIBd1LPTUl4mfPdEQhvF+5oJXTGy6J9WqteA8KaBqZnrLOjmUSuFiZUEIFKOihBZm0+WwTVyGWkaZadj7GUOQKeuaZREMjQRPVuAnnSx7G38CsxV96AgKMNI/R+S+WMjU9csP5hGWvOdKeCJz4Z72UusL6DS1CUOrHIaxv2DdVRR7YRevDfj6l8ELoAvyDmGAVdNR+hQQmM8VUmylVW4b7EqG+q2QPzUtIcu/1Bk56yxWkcfL0wVFIVfiOKUctKGcMMxWHoKvk7oY2/ksgOns2eo1UwPRNreHwuskyqyY8Y4Y2gwPytpr/88i1c5VbW/mkKHDLzJpy1J3SLnA0EEudOOTbtR1/PZA3fdOd1wNNKuuNZzzJmbO5nRxF7Agg3WgrspX8jCS7yMpNghOUdI4tqKoTsv1rQ2YAcBPud9JG8qTaj8kONTtJ8TCBjcFfI9yp3KgfUXts1BXpOD6UnuKvuaC+JcZfHJNVTSKkJHVIPPtKgdczqlrYCUKJqZao7GeqMIYTlxEfnMNgs1/6tbK7CAeSHp1Fv8mpAO0fLUBwHEJWY6jxC0uroD8r9xnMO038T8R/4soCWzWsoxHzsOsRTOJprRNxClAZAMViiopKuGqi6MNrnZ7CEcbH12fK++CuMZovM0jhOO0M/shhceECtQgMBMKSv20kYbCVn+JK1FTukNhmdDNQ==" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="AF">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="JFK" DepartureDate="2019-10-16T11:57:00" ArrivalDate="2019-10-16T14:30:00" OperatingAirline="DL" MarquetingAirline="AF" FlightNumber="5722" JourneyDuration="P0DT15H18M0S" Class="J" Cabin="C" AirplaneType="321" FareBasis="DN1H01D1" />
                                    <Segment DepartureAirport="JFK" ArrivalAirport="MAD" DepartureDate="2019-10-16T19:38:00" ArrivalDate="2019-10-17T09:15:00" OperatingAirline="DL" MarquetingAirline="AF" FlightNumber="3679" JourneyDuration="P0DT15H18M0S" Class="D" Cabin="C" AirplaneType="764" FareBasis="DN1H01D1" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="USD">
                                <TotalFixAmounts Gross="10545.92" Nett="10545.92">
                                    <Service Amount="9272.94" />
                                    <ServiceTaxes Included="false" Amount="1272.98" />
                                </TotalFixAmounts>
                                <Breakdown>
                                    <Concepts>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="4636.47" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="4636.47" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                            </Items>
                                        </Concept>
                                    </Concepts>
                                    <Taxes>
                                        <Tax Name="Tasas Others" Value="636.49" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="636.49" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="0" />
                                        </Tax>
                                        <Tax Name="Tasas Others" Value="636.49" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="636.49" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="0" />
                                        </Tax>
                                    </Taxes>
                                </Breakdown>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-01</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="8" Direction="Outbound" LowCost="false" RatePlanCode="lZmAomcqR8KeVwNrCaYbm7YYwekKD4434aJbEwrpVfyzE48fargROzff5Ej7JNfSu3kWhm40IuoY0DNsDoZxDX7ey1v8/CIzcI6Dez785QwFHUFLfBohblCeeUD+9xu5j2nFtx77T2gTsyCKelebA9V54xdAkON23xe1+y61ss2SVmVjQfRRmG4+dRsK6WKvU/A9l3KJzzmK6iGG+ZdMZVP2ZtV30EXzvdvkbBls/Qaz1PKJo1LroC68mlh2jBUnUwZfoidfbH0sAOwFRsOxaM6XT4jIZiOAd+Cxe238rdA4l8G9DgM2m2pDL6lMou0sfzp+tGl6QKIfWAJGTNEGH0ymVtea+Bg+Gl/cnTbYOLcTE2qZu1OdTl8k2GMiXuWpWeHVVFX0wZbHgabvGQnTk5dweMjdMzUj/j/9cRTFBG7JNcSQ4rRV3YVnkm9DYr9NYDj8ohq5saDXMcG4NoAVMtVzdWzkLoaO1GbrzwAox86N/wBKRgtC3NFhibgiDmN2Y82IYU6CZO/ui8va4GqBdAy12ov+Q4mqP/N45f/8MOOEURyg09kaDqXvabWzh/R4qPEvUgS/kB8JVXujvG6WjU6VQPBCWMELWyD2+uSeBhom5DlqISwBOicP34VTRsggIivlMtVpA1C/07JYvpTnWcJbh68Z3Jzqyj3fli6WyXfavqbgQKUK0JseqIyxX1uiMucW5sZEFPlzJyCjqkEy2bPpWtY8+JFROmOeX7ZR7iROwbqKt90QVR7yTu5kqHgCSHL/y6qFeKCsGYRaYDRac4avfyJjN9lUBnpEO71F6u4zKjOLDqHcs2UyOvFzlGgnR6GhtJN/CrerqaOhGzszwxplYpKSOmMGXj1iZNWLe8QvRBvVbGq1zAEXfznLosKUG6aLIQtMezQSGDXdQXXAuEO82USEvhHemM61McftkrkRLnDttwIspUK+xELe4eKgQrERKvulj1BLpydFSI1QswAMOEIzTVyP/cQHUTV26/jbaOeYevZeSU5GAG7gl1ggHgBDFG9Mv4hSmaO1gR3YlMRcb5cFiUewSRwoErs5mXTsZFo+jhZu0DoxBxXM9S3puxn8sy1h/MrHKFk/m4o23f8h7bOhYmQKnWrtqqZqGoT5zU+NK884iD4H3OYPXip80HhU7KRin+O91ojbvSqZ0nP/pyzBqDB8hVvagR7p9UNPyi7NyyS0aFBp3aQWAIwwyPHGrKAbynDb03oouZ/3bylJD0dZsPEHKN8ubWyINT6A+cmCaNXYppB0adZXkTQKz+pojhMui4aWsun/0mzpn+3NnxW5x5A5EaXiRq6S7iKJB7FZ0Esf3quRPXwE5reNRi3x9Ahk6QOFoMczsL8rtg==" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="AF">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="JFK" DepartureDate="2019-10-16T15:12:00" ArrivalDate="2019-10-16T18:00:00" OperatingAirline="DL" MarquetingAirline="KL" FlightNumber="5157" JourneyDuration="P0DT12H3M0S" Class="D" Cabin="C" AirplaneType="321" FareBasis="DN1H01D1" />
                                    <Segment DepartureAirport="JFK" ArrivalAirport="MAD" DepartureDate="2019-10-16T19:38:00" ArrivalDate="2019-10-17T09:15:00" OperatingAirline="DL" MarquetingAirline="KL" FlightNumber="6126" JourneyDuration="P0DT12H3M0S" Class="D" Cabin="C" AirplaneType="764" FareBasis="DN1H01D1" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="USD">
                                <TotalFixAmounts Gross="10545.92" Nett="10545.92">
                                    <Service Amount="9272.94" />
                                    <ServiceTaxes Included="false" Amount="1272.98" />
                                </TotalFixAmounts>
                                <Breakdown>
                                    <Concepts>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="4636.47" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="4636.47" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                            </Items>
                                        </Concept>
                                    </Concepts>
                                    <Taxes>
                                        <Tax Name="Tasas Others" Value="636.49" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="636.49" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="0" />
                                        </Tax>
                                        <Tax Name="Tasas Others" Value="636.49" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="636.49" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="0" />
                                        </Tax>
                                    </Taxes>
                                </Breakdown>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-01</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="9" Direction="Outbound" LowCost="false" RatePlanCode="lZmAomcqR8KeVwNrCaYbm7YYwekKD4434aJbEwrpVfyzE48fargROzff5Ej7JNfSu3kWhm40IuoY0DNsDoZxDX7ey1v8/CIzcI6Dez785QzQ3l4mORUuuaGAPC4aaiIvB0aDoKjlU62AQokjeCfStivnmyXJiaO6NNYmU/MjHwtXYGbMdXozzi8eZcJ/Dm+kY3JfBNunZUKYK4ctChm5DcRIRFQgKB24BuzI8oGs1pizg7sDjC3tnEE0lHY6DyAA8Zsi6bBeWk4Aqc0BGwil2PDzMEk5g7OKxTzVFXMOj+Sb72cLb0bjs0pS6xsgjE9k2gs6t5xWpm1dk2tegVkWmjZCup/jVHsjARl96KST04/lTzglWsS3Np/W70g0CYiQEvK8svuLZ0Qy+EwdOLgvnMBwWo2jcz9R3YYP6seMLomaDVMtTZ+zAaqu7CdyVIpx5ID8upDY4kCjdkuaEZWcm5Q9n+9NMQ+GW5zJMbdMXSzSFQNrEWCeHreTslnywDMBirjUcNeuK67IHj5xiRVnlTyH4LAjTflQ295EFFJQYbRG1NX8538B+Qn72zJh3G3KNvjQiW9M16cO90tQgT6EQrZ2oGUDXOYYot5yexHDk41LFtfgj4QqyUtNfO66+qAQdvw38xmlbPx5JcKznO7aet9eijsD8qf0Gk3dRYI61TQ2XWKlSrxlb39JF6B5FmbRDg6nxN+dEdunDi7yI3NmKjCXvUEFximUs7FxzC2CNQoYS5Sufmw1TqifoCwDVnXc8z4dBsNnEyESPQRXc9CnHACA8zJPquEFTM4QbrwIbNEYUR2UoquTpWuHWH3ItXa+U/H2oEHcscIbCzaki0zdZ8qg92prwfomo7zTc3G7LaLWtbtNnyyWbXSvVZRLiJg7os0G3N1J+fH3RvvYgZrtBn6qkkZ0gZR/g7BCfyocn7szgI9r9yNDbe0UpZ+w4jj2Cu0KKyLutqGGElJOEz4wYlGqQZwLPpSR1MBqSmqH+6qYmlh9JZStvQjbSClR5GkDNJqoQGcSJMsIDA/D3F9LbmsAVu0BLnTOd8ttUNKb4zdDvtesB36iKGES23Bg68/zOVTYLWvBdocr+wA2/HHt+8xywbfyjH+TLxi10dEO7eIvxzh3WzmRDvFdaWkfCpIT06Fb/K1RMxcHWLxTdD3VzVQ84sGDdMgvhlkJzbU2YsMnlyAqkgwNb8ec2x9k/I9zGKB6I3ft3leh1WV1f63JZ4g/jsscc1fJokktPq8qmBJ4NTjagWFCYcKC0keWMRJwa9Cr5w/A2b5bmmopOkDaQhO85px42bQDUcBMi0UovNqZZ0eLFm4NGzcpA2kFUddhRw7gnbAd7XF+jRu3z7bbig==" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="AF">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="ATL" DepartureDate="2019-10-16T14:20:00" ArrivalDate="2019-10-16T15:53:00" OperatingAirline="DL" MarquetingAirline="KL" FlightNumber="5591" JourneyDuration="P0DT12H15M0S" Class="D" Cabin="C" AirplaneType="757" FareBasis="DN1H01D1" />
                                    <Segment DepartureAirport="ATL" ArrivalAirport="MAD" DepartureDate="2019-10-16T17:55:00" ArrivalDate="2019-10-17T08:35:00" OperatingAirline="DL" MarquetingAirline="KL" FlightNumber="6028" JourneyDuration="P0DT12H15M0S" Class="D" Cabin="C" AirplaneType="764" FareBasis="DN1H01D1" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="USD">
                                <TotalFixAmounts Gross="10545.92" Nett="10545.92">
                                    <Service Amount="9272.94" />
                                    <ServiceTaxes Included="false" Amount="1272.98" />
                                </TotalFixAmounts>
                                <Breakdown>
                                    <Concepts>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="4636.47" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="4636.47" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                            </Items>
                                        </Concept>
                                    </Concepts>
                                    <Taxes>
                                        <Tax Name="Tasas Others" Value="636.49" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="636.49" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="0" />
                                        </Tax>
                                        <Tax Name="Tasas Others" Value="636.49" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="636.49" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="0" />
                                        </Tax>
                                    </Taxes>
                                </Breakdown>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-01</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="10" Direction="Outbound" LowCost="false" RatePlanCode="lZmAomcqR8KeVwNrCaYbm7YYwekKD4434aJbEwrpVfyzE48fargROzff5Ej7JNfSu3kWhm40IuoY0DNsDoZxDX7ey1v8/CIzcI6Dez785Qx8xqoT1u8g2tE0XqFFo2SwBYTRJbNnxkdGlX/VM2ZROov1gI7DvjOK7/W7OcMH1tL1i2xqqjBshrkiV92DhX39M0Xedq1c9GGmrVKUZCSTwcUAQq3fOz0B7dCya2JloI073i6KsU4IXXHoW5cFw9HxiIHzpMuI8uTdUwh3sQ8VjY1V5qaOtrSp9nvkfx9QAi8mXmZBfEtLGXKlMCXGQd2ip4pc/Ls8gj4KdV41N+ETcs5aUhQ2a+gxN1ScnzSW0F73xmxlj8ZXAqNfv+kz3r4RnzPEe/YHwOltYS+G6p3NEIxwYvNzLlW/D+tp0oEVfEEAPU8q4dz5BOsBMZjPLrer2l0jz2LgkqWA865jRJUf34MMjqGCf3U/suFqsPjDsdU+WXxe8+WMVd8BWFhBC1jOPThMh5dEt28s43GtYZUOgVDswfXdvzKgh/zCphi2yHfv0IPBs7wwF598sj2uo4rX8JCaBV2zguIR5COREdQpzZdWu/ui0VOIrKRMHIJcA9SUk4KY0zhk8cNfkhAloSQvdgADhGDlw6s3NorpEZn5IWmwnd9vxlwBIGnHemOKmJcpG7t5m+8p+CI+z6YuOyuzhTDM1pHWwWFSiMTfO5Q00GvDkRyCneYyEj75inmufTJ3gfsP3BlraOWdXvA2zSj3eh0yynXRCwuHmRrEv7/RxBCpFtQ6eT++XhPVUHqoILP56US33IVHw6zInkdE1t2KUCP95KSJgaaeO+LdncamVNScqIeiijzLhsEokgMc+WcZNiHhDRVDlkPTz7QiaC0gDXlANIub4JcYgC4i8nysxPfa5UO5hMbVkW/svvevieAnePyWD/7ItdwW5BJU/5Ev4CQiSBj7YqRDsljzsb5iXANBzj6cFwGxemuXw64xQ63v8c7U0MnhZwrPkyRm5qzOho+xTS6BuWEyIOex+P3XfG6F4ZXYHyHveQAFNUZeSC8VGjTg+VEbEjH1OL68BfZQmBA9ebY6OmOJsFiYrReuXiAE3IT8BK4zGhJv39C+gPBFLNxN0yZX8TqrqJvSNnzcWEtlkkGYyoi924N1jWflw5CA0Va9CADHGK37SQnx+bqaFxrR4Or8J056Td/TcQ4oPZHyCOq/4ChPG4KnPVVjmm+HsJaNCvSWIt7khhbVTdtrx0clBOyH5ziIbnYMOOXXQQRkmMVGAODkS7Gazh0n+6naWtSlSC/j61GNFXNiDVPCrZ7JjLECIem97lLOKDKHk0tNfgzBRTY5obFnEfDN9Q==" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="AF">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="ATL" DepartureDate="2019-10-16T13:25:00" ArrivalDate="2019-10-16T14:57:00" OperatingAirline="DL" MarquetingAirline="KL" FlightNumber="6875" JourneyDuration="P0DT13H10M0S" Class="D" Cabin="C" AirplaneType="757" FareBasis="DN1H01D1" />
                                    <Segment DepartureAirport="ATL" ArrivalAirport="MAD" DepartureDate="2019-10-16T17:55:00" ArrivalDate="2019-10-17T08:35:00" OperatingAirline="DL" MarquetingAirline="KL" FlightNumber="6028" JourneyDuration="P0DT13H10M0S" Class="D" Cabin="C" AirplaneType="764" FareBasis="DN1H01D1" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="USD">
                                <TotalFixAmounts Gross="10545.92" Nett="10545.92">
                                    <Service Amount="9272.94" />
                                    <ServiceTaxes Included="false" Amount="1272.98" />
                                </TotalFixAmounts>
                                <Breakdown>
                                    <Concepts>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="4636.47" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="4636.47" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                            </Items>
                                        </Concept>
                                    </Concepts>
                                    <Taxes>
                                        <Tax Name="Tasas Others" Value="636.49" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="636.49" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="0" />
                                        </Tax>
                                        <Tax Name="Tasas Others" Value="636.49" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="636.49" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9272.94" Amount="0" />
                                        </Tax>
                                    </Taxes>
                                </Breakdown>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-01</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="7" Number="11" Direction="Outbound" LowCost="false" RatePlanCode="lZmAomcqR8KeVwNrCaYbm7YYwekKD4434aJbEwrpVfyzE48fargROzff5Ej7JNfSA55HwRyfqBo7qSz8tdl+C3o5Vc06mBUDIob+wgolavoOuQcTbsBiR3qU9ldB9tgZhH8ej/fFk332iC+Oa7c12KvWE5yvxC9FZYIQ303rVEU9sZVEsarm2JdhkO1e+sKAcWQakBPUNKT/GoWLnlTG+VwHPOFqfqBGAxaGrFJe+k4jdxSaS6OLcfwqrNYry2utJqz2kyxod/wyPRRCJshUADKtN0SpFfS4cy8DePje30Bou6lVvnf4GgOjaramW1CrlZE933cGZ2u6mC3QkhL8WAxIftyU2UGAhbvJqFjGqZPvjl8LtZT1tL1PS6f0HSw1+OTCusBn0cxvSoZdw91DfI7u7LNW1wWbbTu8BsuOhWVEytMUkkhtm9SloOAFNIigcriJpup2urdOSgaPMxDMZ3Y8IlXiEEQJ/HaqktYXTDFZOhhHzB10Ionu1RxsDiVtc34pFluR4UCoJqfjGHumEx7rhx9m3ZG5zDHtrjUnjJhtOhokZbFNyOYd8Y0MupoXWF1B72II9AEHuXuj+O2NWJ/inQzH2c8KvWa6c9ATfSj9ggn5vYMsuiDyiugS9OrV2YVJ5Tc6Zl8+GsfVKDQkzKtlbEHpa794YOHbz1X7pQsPzF96RHulzBRdE+p5pMb2hft21actTMgbtVrsUmAGcSfeMgfcRLJXTMXehwVqLAWIjKtTduKEShHB9k1XanCXIJjTX6WFHe05IuEAAthaL99FF8s2lzYxgcOWDlo2Z7pF9k5aWyBVpmqDvkM9gKWgAg3d0gmfkctmTpmW5NphkvAHX3abkWOZUmki1yM9s9YcPmSt1H5Rxtr5bD2Hrx4vXcuNgwf8wEdkwH22H4+lmtKfvhix3BNK92oeWQpioAXDr3M3L6mBNTeTjmn1FnfCtaCBbV7T17UpgIkO4YAUtcyik8yETRRGiMl/4j/n8ZPzUszc8fz4ZsahEacHXXFQMb/xQQJaPXz45pYcFhNfCTaiqM2+Z8GMFi70thHH4FmSZ8wp7TFWB+t157i5VOvsAbecX5ajDUoHZPwopDp+NmV+CdKHjH3swRTfjF3F9/JrE6fLSoNvzte+RXPRfm15PzA95U1N/BtCDtSg0g9us1Kbbcsg22DshIMS5XpIVB76cuEnoKA2YGlXzr/B1xfDY69nmEBWVmLXibn5IT4uaEfT8Pz6dAEgKBH4UeQsWoVOnmWullkGhnm++ivQeTwAJWieGl15SinLDCADtcKabqvfDCSXYkmVqI7cO3I8HqhDA8bcWVWA2r/Dph8cPyDy" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="DL">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="AMS" DepartureDate="2019-10-16T21:50:00" ArrivalDate="2019-10-17T12:45:00" OperatingAirline="DL" MarquetingAirline="DL" FlightNumber="410" JourneyDuration="P0DT12H35M0S" Class="D" Cabin="C" AirplaneType="76W" FareBasis="DN1H01D1" />
                                    <Segment DepartureAirport="AMS" ArrivalAirport="MAD" DepartureDate="2019-10-17T13:50:00" ArrivalDate="2019-10-17T16:25:00" OperatingAirline="KL" MarquetingAirline="DL" FlightNumber="9607" JourneyDuration="P0DT12H35M0S" Class="D" Cabin="C" AirplaneType="73H" FareBasis="DN1H01D1" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="USD">
                                <TotalFixAmounts Gross="10560.26" Nett="10560.26">
                                    <Service Amount="9286.3" />
                                    <ServiceTaxes Included="false" Amount="1273.96" />
                                </TotalFixAmounts>
                                <Breakdown>
                                    <Concepts>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="4643.15" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="4643.15" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                            </Items>
                                        </Concept>
                                    </Concepts>
                                    <Taxes>
                                        <Tax Name="Tasas Others" Value="636.98" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9286.3" Amount="636.98" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9286.3" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9286.3" Amount="0" />
                                        </Tax>
                                        <Tax Name="Tasas Others" Value="636.98" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9286.3" Amount="636.98" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9286.3" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9286.3" Amount="0" />
                                        </Tax>
                                    </Taxes>
                                </Breakdown>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-01</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="12" Direction="Outbound" LowCost="false" RatePlanCode="lZmAomcqR8KeVwNrCaYbm7YYwekKD4434aJbEwrpVfyzE48fargROzff5Ej7JNfSA55HwRyfqBo7qSz8tdl+Cx1EBbYwVvNrxwNqa8g7i8to0zAE84cwPWZxjFsPdQWk3psAA6pAy25ltc66uRWh2QeIjlCyVdHNDxW3lAHFGcMW1R156FQGhzSFuB1PeFktGWI9890nxi5bZkCozPCNdkdo7O1XBShHStfMFZE1fA52Dya0nZsyRVMvxN+0Q2/YTQZD8sipcsEv8NoxoO50QUpP1C9xg6/3ttB2OjhwKA5Gzz1pUabnYQXiFcVPVHT79lOBed8HEQtD2ve57wbEoFgRG3wkfSIpSvQE7bdV7PlOZF8QcJnx+8c+0WrtsZkrxiMAp3J8n2b6nFd2yOfQWAtWNK/OK41N+Sn3v4oZHTv78dUTOZnG4OGK8H4nHftLsT+kZTid5rXlbhhWF2UQOq/2YxEwAHzxYna1JldvL0W6h7pJPOxjhOXiJxWQVkS7o0zvpcItrSyykZvFAN1wIBwFJQyyu9DdZfr8CjUY1NUJma47GKo9sG+Ahg6RUztsbFU2UeQfzdHmameRhvqr+/2B9k2ca8ofrxlDz6JEm0EYfqsMDxqmVkQnNSFA40jgboHesCrVANf3Wf5Gaa97dtveugPIQ0wlzaHzGeTuV0/H4OJBCMIaHQRaJOJmnZyN1tcerLsnR2vT3CJhiuH9DHjtbYsJd49o064p3rbSwpBy5VpjhBm/6AA0uAUdHwNHWYO8oiAdxb5SXgF6e+xn9zq8IpS8qojfXigXnXm7OodLQJFVfPvU/ISMShDxOE8Q+F1rGkG27nNdde1IIPfZ+wije4XAiECpxlKow5yLDzNFfaruM6mQ6rXnH+XE3QKL6mmwhVjuHKXPhyqVQqBImrLvDaji6x4rD9HgAedk4qcvIpk6B2YKgZk8WDvc19Lh1rAK5PybaWhI54JZ4NxVKgUiQrKP8ykjsfR8bK9Cm11TFRpTlABSolnlm9S/7tze3QFheFZ6PDEy0eQpOYfvUEKWPZxsTfrSJ0sA4r5XRtKq1q1kzwQFGLdV+KqmyY3zrvjaM1Dmg2i3frB5EutiYX6zNXakXAEAmrU2EXhosg6t+NNHRHr9bcEvLnSAhrBCm286QhGqPy+/u9pPLBgOMrSeJ2Y0j1EDZ+hccZknijkFpGx9APzlbM7Xzk2ko8LmA2n6D1sUD5kO/HPGzHPBZ09/vOWbi9pFoqwZ4TsvUzrsKCBY8fSFh/tdmm5JhESHp1Egc2FNsFnoH3+H+nLHUreFgXiXZbnIhVPw9SHu4uc3QS8r9KjZInyvXs3W9XPF" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="DL">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="AMS" DepartureDate="2019-10-16T21:50:00" ArrivalDate="2019-10-17T12:45:00" OperatingAirline="DL" MarquetingAirline="DL" FlightNumber="410" JourneyDuration="P0DT15H40M0S" Class="D" Cabin="C" AirplaneType="76W" FareBasis="DN1H01D1" />
                                    <Segment DepartureAirport="AMS" ArrivalAirport="MAD" DepartureDate="2019-10-17T16:55:00" ArrivalDate="2019-10-17T19:30:00" OperatingAirline="KL" MarquetingAirline="DL" FlightNumber="9449" JourneyDuration="P0DT15H40M0S" Class="D" Cabin="C" AirplaneType="73H" FareBasis="DN1H01D1" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="USD">
                                <TotalFixAmounts Gross="10560.26" Nett="10560.26">
                                    <Service Amount="9286.3" />
                                    <ServiceTaxes Included="false" Amount="1273.96" />
                                </TotalFixAmounts>
                                <Breakdown>
                                    <Concepts>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="4643.15" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="4643.15" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                            </Items>
                                        </Concept>
                                    </Concepts>
                                    <Taxes>
                                        <Tax Name="Tasas Others" Value="636.98" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9286.3" Amount="636.98" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9286.3" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9286.3" Amount="0" />
                                        </Tax>
                                        <Tax Name="Tasas Others" Value="636.98" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9286.3" Amount="636.98" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9286.3" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9286.3" Amount="0" />
                                        </Tax>
                                    </Taxes>
                                </Breakdown>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-01</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="7" Number="13" Direction="Outbound" LowCost="false" RatePlanCode="lZmAomcqR8KeVwNrCaYbm7YYwekKD4434aJbEwrpVfyzE48fargROzff5Ej7JNfSt6ntbrD9PRO7RyB1fXBW/DBFxOtJZAAtSaM8CAsfi35roI6WFp8+dXNS7cdupSyLAJJns79MWe8/Glbgdoj1YnruS92EhAE0UBq94oGw0iRQTzpJWPLNORbWDWhqgSrrGYJTpHyP96MP0xYgxZvdh7fTYBxzuEG/DkPtS0ltzKt156LH97zr8jsyOobh0DdWIt7HQGbRHBT+ahtU3S5sdYE269AamhHB9D2xrFpP6/UaFGOJKwmvWGQTzxjHGMQExRqRovyf37diUVTimoKE7HSdqhxIkNEFFIrIFpzS9rt0NtwA4HkCrz6ljb0lyi9rN6snE+Us4xUGk/PfqFGNzKEPbf+rAgjaPeXoT8UMdACSPycbVTowbUY/YhQuev+xczlFtNDRXaHURQwhDyenu16lKE0OZvNCMm92D+2VyAlY0QBu9hOd+N0BGZKcgv/8jcV2WX5jJl+ui92J2MDgsFnctQ3dJWQMbvdJvb38uGSEh8ftXbwKQAc6MAQFz9K6T2hW2h/K/UF+xHwTrJixMovZVbeSmvZF51LAALU/+ClnrXOBxs5jTmNtdor5vivZWYd/3m7tNAJRgbZFBFsjZaBQraW8f1ljRb7PMHIiXT04pyBYyCuOSo5iV5dP0x0zgf8c/o044csdplCHelKXdxGb1fFVDc8kZi///OVk3Kii8p/QPIQj8EQV1S+qxoufGNLoMtDNhQCZkwq92kGPZYh5E2XJjqKxrcK0VUk8rggfzoEy/mSW0xHJYGhXKgYPPx8FWYVS9oI47pSi2IrUnZN6entOC1PiifQUJ88fJvEuKL417sFw1CL6N3RqAqGubPHZdJP/oWVVxnlsCRk/gKxDYMbOkI18terS/CSLWXRRamidJ9zh/DtXj7BLM+0LMnlRybQBQ7jL8USmx2EaDAEinpNElgGODbgYtG6Z6QtBthDpqa0PhdcpLJMeptRRKMG+Yh2MSffGDA2oDgmOq4yXNZpslnkTfpOTMXC5DRxJgjOHsZobkBaBPw87XIXDHLFQBHzK22Fau1dXvuJQpXTPpVQ3zCzoLQlBBcVGBk/teVfX2iSXuQ5MjsmJ6hdY3zc2cx12Trc7j0cJvqsYYJdEYksN1qCON6A7KCFWYaQlj7OHCHlBVPJDDJBmZ+YE3imalXCqfjtLcV3cDzJAKRYLJ997YrAE1mdkXdmSfliGvSg70sIXwjUahwbXqUCe9sQa217xD0d4TP4wUbD54fIzNTXyjP/nresZoGTSXtFN1LJMnxClWOEUpW8rm2mdx8dnAoC6Z1A7JXBpS/xCKA==" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="AF">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="AMS" DepartureDate="2019-10-16T21:50:00" ArrivalDate="2019-10-17T12:45:00" OperatingAirline="DL" MarquetingAirline="KL" FlightNumber="6123" JourneyDuration="P0DT12H35M0S" Class="D" Cabin="C" AirplaneType="76W" FareBasis="DN1H01D1" />
                                    <Segment DepartureAirport="AMS" ArrivalAirport="MAD" DepartureDate="2019-10-17T13:50:00" ArrivalDate="2019-10-17T16:25:00" OperatingAirline="KL" MarquetingAirline="KL" FlightNumber="1703" JourneyDuration="P0DT12H35M0S" Class="J" Cabin="C" AirplaneType="73H" FareBasis="DN1H01D1" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="USD">
                                <TotalFixAmounts Gross="10679.24" Nett="10679.24">
                                    <Service Amount="9286.3" />
                                    <ServiceTaxes Included="false" Amount="1392.94" />
                                </TotalFixAmounts>
                                <Breakdown>
                                    <Concepts>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="4643.15" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="4643.15" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                            </Items>
                                        </Concept>
                                    </Concepts>
                                    <Taxes>
                                        <Tax Name="Tasas Others" Value="696.47" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9286.3" Amount="696.47" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9286.3" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9286.3" Amount="0" />
                                        </Tax>
                                        <Tax Name="Tasas Others" Value="696.47" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9286.3" Amount="696.47" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9286.3" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9286.3" Amount="0" />
                                        </Tax>
                                    </Taxes>
                                </Breakdown>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-01</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="14" Direction="Outbound" LowCost="false" RatePlanCode="lZmAomcqR8KeVwNrCaYbm7YYwekKD4434aJbEwrpVfyzE48fargROzff5Ej7JNfSt6ntbrD9PRO7RyB1fXBW/EnD2yHITeAx9EYIWASP23Qe/qGA46RMVuBICkDQnOkkOrMUB+c54REy6oeXOxNrTGxZkiC9Wbmw2UwGQjhKZtUdqISG130651U8mWB9PUQwuU/oxCj07crPck6zqJy05wqrsJ8jhsyujB21MVXw2/Z3FevWI4yfraK+prJa2O1MimznuH7FFMX63KboJV81MsYGWOxe6YH6Sn3lcDuQjzBdF2mTgq+WKzdRhW0svLicHau9A2TlclmSOIuuojkIPHt297kFRoRa6YJI66IptZYzoWBLmqeMY7qJrPnIqbKNC69UyUZ1ixj/QTF+bywf07ifw4aY+ljLOSiDVZEhW2zOI5DpRkIsnEVlBZlErZ+U2xJnFIYQaBWdDcGYzKBt+1+Sn4IYneGOhtyPmJd0LyEVjQAR9++QDYvhk6zh+YHlR/HzkNVmUg72nLs3zoE4bCyxqscLMfxjx4plFza1L2H/7q4gjEtA0wKCaJpfIJiojqZBcN5jahNZD26f4fKqvlETEgqZgQliDx7LBCkxqQf5FqxHrkakJDLKFZqa2lBJRKsHIdQp8Hyr4HQcvM/OpgnnxNAsAbly7uv/iTrryAzsWKP6PfYrC3bOipMRj/UMiBxcLzyx9zaGhCvS2UbrD7s8vYHERrvW0EOBDvURCqv5DZfhEwI2yGl9T12vySFQxcrB+mVU6yMyUPir1pXamc6vWfvOl4f8/LXHI6JqD16MYIqdRj41bZX9Dq8yNTD4XuKG3a8nd++w/nH7rxup0Us9mjjoHzwDFIoWFp4UgiTPXcB40SRSXv26AGbUy2oin9VxD+lszhl7145dRT/1n6/+3OXL6Dx7SpfkJEPBLh/2y17Hkkveoqe/9zqDe+gCGYmzvUudo/qDD0KyIyR3nEjDOBH//MwZLGPqUOTpyB0vnYEARts8ZuPw+DwJy39nusbUnflpdb10RJ84UdwxTnZB5N1ki3hZ6BSMT8wwYifUfS+K3T11zv/g8sgE5IV1W3ov70euTJ3OSfMpMeLCJ4UjO30eAVGwJrMuDYm0th7U0Y/icE+Afj7r9He9mZvfsQsQ0tWwZqcbhPJw/yOFFg2FhfT1ZIHmgpkJdynftwhsUlP3LcMhCqCMi1wUQvrjuybdDb7ofF63c0EF3349TrGVa5dK6gCV+5NDoMNYVK7ERTVQ5YPCfAS27F9+WmRe17+Hj/3Kf1qQfNamSaKr7KYvMAmxJcjlfLAD9eZjsIyC7LSpAGmeovjxNldTSNRx" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="AF">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="AMS" DepartureDate="2019-10-16T21:50:00" ArrivalDate="2019-10-17T12:45:00" OperatingAirline="DL" MarquetingAirline="KL" FlightNumber="6123" JourneyDuration="P0DT15H40M0S" Class="D" Cabin="C" AirplaneType="76W" FareBasis="DN1H01D1" />
                                    <Segment DepartureAirport="AMS" ArrivalAirport="MAD" DepartureDate="2019-10-17T16:55:00" ArrivalDate="2019-10-17T19:30:00" OperatingAirline="KL" MarquetingAirline="KL" FlightNumber="148" JourneyDuration="P0DT15H40M0S" Class="J" Cabin="C" AirplaneType="73J" FareBasis="DN1H01D1" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="USD">
                                <TotalFixAmounts Gross="10679.24" Nett="10679.24">
                                    <Service Amount="9286.3" />
                                    <ServiceTaxes Included="false" Amount="1392.94" />
                                </TotalFixAmounts>
                                <Breakdown>
                                    <Concepts>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="4643.15" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="4643.15" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                            </Items>
                                        </Concept>
                                    </Concepts>
                                    <Taxes>
                                        <Tax Name="Tasas Others" Value="696.47" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9286.3" Amount="696.47" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9286.3" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9286.3" Amount="0" />
                                        </Tax>
                                        <Tax Name="Tasas Others" Value="696.47" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9286.3" Amount="696.47" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9286.3" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9286.3" Amount="0" />
                                        </Tax>
                                    </Taxes>
                                </Breakdown>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-01</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="15" Direction="Outbound" LowCost="false" RatePlanCode="lZmAomcqR8KeVwNrCaYbm7YYwekKD4434aJbEwrpVfyzE48fargROzff5Ej7JNfSt6ntbrD9PRO7RyB1fXBW/EnD2yHITeAx9EYIWASP23RV6ZydPvzsWh0FBwbFwjQtNvG9gPqzrf4RR86xO6oJIgmP9qrz/bXxh02pHkNBeqmPB+ZRtz/Lwzya/yCcQawSaiuUv/zAZbHYJ6Nc242VlQRjAwF0PjO28X3tTCjsg6qAX5eyFDTHIEUYDHjNgrZQreH3B0b96y/XDyFi5rcFQrCfq7T6DGcoAcbuTQp6n0aOl1psBih9jaN2eXHGam/lup3jhQuEwBGCuN46ExMkWspNU8vDRCPj8Xf5b/L8YdSsSt4o+UFbQNSpS13PGwonZG+IR1WDMP1+GrCXIY5MrZ36av39PkuQvAoLbmhJKcdrOJzLqsmOyBcBzMWq6+H5Fg1ho0nRvwFpC817K0pChZNgr6pfPUZYjXgOMycOG8B1MzhqQyzg8KRtPtFwrURadgCu0Oj1zN8HhEfYRM5h/UZwv9HyB6j3DNN3XvoFijqIdK6Bukka9dVWZqyK2uIg509HMc/u2BypXVEz4n6SOQsZIhpD11+SIaYvFzm7dZq2UmqTWgAtiUCX74pk8AjvT0QYnE6uGB8aGtk76swhaoxfU/RZKjmlRytH7CwsFyWE4gLBWUR454RZWeesf99f2e7fvnqmGCmorPAFlNn+KRQv/h8hOEHfI90CHJAoF/U2pPbx6v3BDpD0bLP62amGB7rG4SUuAQKNXz0XFl5A0u3ljBLPI5M9M6epYe3U7HjzGMuKrJEu2sm2FK/XBiuHZ3KeFlIc80NNXh7qC4g2zgmPv0P9IiS5CALq01S7Muo3mvrCOwy4yHpLiDzl5vGg417DZLM/yOol4nKfZBHUpMqzJ/mXg4uIO1vW654SpC+H+C30zLt3VBXVtznUmdPsb86LvfM3CF4uKbBZ92QBi7IJJwPiKSw70d3KbQJTX03ubXOrPkW3I96iVI4sLyMPhsrXRFDk4wqU473jn96cU5iDook7Rqt0+vXdg9uBjHSAcXlgt6C9IiF/l2W9Ba+nwHAzdU0GrMehsMUFKk5QKY4T9F0/BbkUw2E3dSvHiVXMpVbWRtecgEnk7uMgyC9IX+Ty6+2n0MVXMfDa+/IsF1gyjT2nXGSQxd3lkJjNM3rY+RS3Tpsjx5a/GNBfwvGhROo8HmIu0NVNA9LtaTT+Cc2Pt0dbP9zTqyncA9ZqYKyleX/nyI363z/FcKtYQ+Ps9/TEjkSP7oe+IY0hRu2DIFvKsBDzeOSI/Sqd9+q2I6mzkjBOc3IrIvhujdaJjcmQLkVoX+QDfefVIjD5MrWgbw==" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="AF">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="AMS" DepartureDate="2019-10-16T21:50:00" ArrivalDate="2019-10-17T12:45:00" OperatingAirline="DL" MarquetingAirline="KL" FlightNumber="6123" JourneyDuration="P0DT15H40M0S" Class="D" Cabin="C" AirplaneType="76W" FareBasis="DN1H01D1" />
                                    <Segment DepartureAirport="AMS" ArrivalAirport="MAD" DepartureDate="2019-10-17T16:55:00" ArrivalDate="2019-10-17T19:30:00" OperatingAirline="KL" MarquetingAirline="KL" FlightNumber="1705" JourneyDuration="P0DT15H40M0S" Class="J" Cabin="C" AirplaneType="73H" FareBasis="DN1H01D1" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="USD">
                                <TotalFixAmounts Gross="10679.24" Nett="10679.24">
                                    <Service Amount="9286.3" />
                                    <ServiceTaxes Included="false" Amount="1392.94" />
                                </TotalFixAmounts>
                                <Breakdown>
                                    <Concepts>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="4643.15" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="4643.15" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                            </Items>
                                        </Concept>
                                    </Concepts>
                                    <Taxes>
                                        <Tax Name="Tasas Others" Value="696.47" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9286.3" Amount="696.47" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9286.3" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9286.3" Amount="0" />
                                        </Tax>
                                        <Tax Name="Tasas Others" Value="696.47" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9286.3" Amount="696.47" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9286.3" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9286.3" Amount="0" />
                                        </Tax>
                                    </Taxes>
                                </Breakdown>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-01</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="4" Number="16" Direction="Outbound" LowCost="false" RatePlanCode="lZmAomcqR8KeVwNrCaYbm7YYwekKD4434aJbEwrpVfyzE48fargROzff5Ej7JNfSQnMmT5Gt5s0Pr1vXtPIK8rOVXfiPaHIz+9c/N71VqaAtYOKoRoKRNd/96ctSpz6h/9UCiZ3nlSRl5RfWdGxV+jMMOJpFKU/xeFjm2dT/hgnqj3EPL0Y0kkA+hUE/EkX1y5MO+VpJUb5JuOaBQOlO+OntSBEqIFmWKOoozQM+pWtavu03ck227HwhDKAG24b3nvULO/79xyZqfLM1aM+m/9Z7NwI4b/VouMkS+WAxSAix1ek0S/gHM8wbwbHHE9mCN4+tY/3tVXH1FPZavEG3LO4ND8GvalR+T5xwb++X50zFfBjGUpv1URfTO1Dlx+qvsiTAe83ydulPwixyGqMpKvApYJzduJWe7b9xvwwS5N1DEXjP/qw6vYASptuoNfV9fcq0mWG7iigtdojIRNSi2+5hQSJ0pQ4jPjGAerfFTVbo1iOnACcnWOuzjYhikdusyfjrJeedJIpEXbcB020uPQhWCyoOx20V0crQ4w66vmIZIkJCHU3sY+VO+OKG1muP1IuDgACkepePnsxOOCtoM4lRnzQuK7AYxQJpOKCrBS1vDLgRzGWJtPPtAvZi7fgSSXXqqBwd57w5YWOpYkutSAMZhJNwXqupv5kSoUouRuvMhyqJiBvMsOtg7jk4LqPHujTqVA2ahOh9NJ4Xvx5vMEQpT7x4gIppFYyJVO8NKxPCstpAYldyCQjEhT40h3Thj5cLRXPoD67/A2uCnmnsMXE0Wys8YwiqnC2j+X2BNtUWpSnUMnqK7KHEmIKLWsDur0cqm52rAVyYNdPiHtV1fY4DLI7zZlHyiv7PGQaxP5YeWvMXfm0dWV/wDiYbMspe7WqhWtFmzowf0XUjGql9ZqO4935fNgg+hC77gUTGrG8VQU+yw7rXIlXHzAnYCAD9F5GsSOXofItXU2jhYD6hTLLYOGxh7O4azv0Gfp+YnjBT/9gPCnbHGwsu/900UW8Sa46Bg5lmNdqG23xnfILvkpm/GtW1JAASgAFmqPBv6o+ddkPjUkiv6IxPNoqVDX1loy7MlF3th6jj2buWH/LD8Ae3fSwa2kH3IpOY0BPtkGyYusLl9UD9ptXTkCAbQOXzJeu03+wRkFrO3Q1lMuvt9KG5RZuhsEbMFjSk8L5mN/6OH5X8Lcz0nmzBD4ton5FDPkgakyWVsDaQs5bXtcMsBP/8Maz8v3AKVGOs9PyBRpTO4G9zo44ScK8hFekP6luGf1/cB9MAfp1SMqJApGHW90IIK5V04HnCKL9CCdf8CqZYmiMCsp6uMXJpt+6lDCsIvRrLpZXRloW3dEM+3oLKVJYBDO9Z76CCvqS2Mc0XUsXC6tFgKso94YftYiPMfIywsXu5D4g8srgBHSongW23bLbHaXXfmSfz3I51DUZwPVUnCXZ+s36rXpTN/ngro96gSCPDjwrtIS/UOSXGMu/Uh+kB+hf82W562WbBYdOvEegiQ1/XIJfzwbm0xlEqfZqWRGi3osfwpsvRIsgBoLzyTFmvjwPcAaexO0IqRZdnqviiR6WoRBO1HGa5Sl41J1cjKzBqwbSsuh//vJe8ChYQTBCWI3AHCrVyBJmsbyvO/GTIewFmtoBG4jv7A/uZBpjvy+sH8hlqZpTY68l6wzPULA==" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="AZ">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="JFK" DepartureDate="2019-10-16T11:57:00" ArrivalDate="2019-10-16T14:30:00" OperatingAirline="DL" MarquetingAirline="AZ" FlightNumber="3338" JourneyDuration="P0DT17H28M0S" Class="E" Cabin="C" AirplaneType="321" FareBasis="EN1H01D1" />
                                    <Segment DepartureAirport="JFK" ArrivalAirport="MXP" DepartureDate="2019-10-16T17:55:00" ArrivalDate="2019-10-17T07:55:00" OperatingAirline="DL" MarquetingAirline="AZ" FlightNumber="7603" JourneyDuration="P0DT17H28M0S" Class="E" Cabin="C" AirplaneType="333" FareBasis="EN1H01D1" />
                                    <Segment DepartureAirport="MXP" ArrivalAirport="MAD" DepartureDate="2019-10-17T09:10:00" ArrivalDate="2019-10-17T11:25:00" OperatingAirline="CT" MarquetingAirline="AZ" FlightNumber="22" JourneyDuration="P0DT17H28M0S" Class="E" Cabin="C" AirplaneType="E75" FareBasis="EN1H01D1" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="USD">
                                <TotalFixAmounts Gross="11036.68" Nett="11036.68">
                                    <Service Amount="9735.92" />
                                    <ServiceTaxes Included="false" Amount="1300.76" />
                                </TotalFixAmounts>
                                <Breakdown>
                                    <Concepts>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="4867.96" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="4867.96" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                            </Items>
                                        </Concept>
                                    </Concepts>
                                    <Taxes>
                                        <Tax Name="Tasas Others" Value="650.38" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9735.92" Amount="650.38" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9735.92" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9735.92" Amount="0" />
                                        </Tax>
                                        <Tax Name="Tasas Others" Value="650.38" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9735.92" Amount="650.38" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9735.92" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="9735.92" Amount="0" />
                                        </Tax>
                                    </Taxes>
                                </Breakdown>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-01</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="6" Number="17" Direction="Outbound" LowCost="false" RatePlanCode="lZmAomcqR8KeVwNrCaYbm7YYwekKD4434aJbEwrpVfy2CJXsMlg8AZ8QWudXdQvR9kB8RTt8XqUXB6MVcS+Yk5gowgUrx96qgPtoA5OYl9gIMY+VbYEsomATRIAmxx1nlQTZMvoQORFisnHWnf4XHiU3CjE4BWKVgDVL/cVoVdyoCbzZNPYTK3Wx4Kx1EGVueDOtqN6EtN2Y2sYP2ZNFQFIqkxu8onxgxCK7T7X3aSbha1DNyReqxuUpdCt6VOW37TZUXncuEHMQdOuY5/nWMndup1cedBe3hNBwz11mgx46twPpW5b7S9po3ZV0WFToKdjfi0LQ5rFGPBUqYoRtdBdtb7DSzPPjdu6OL6e/uG0qm9zRFEAzP+2fMzQhGWUNINCypTjlRNvW3EX4JRnx7mEyFfYF+Arpvs3axQq2upsyuWg/t5AmOKKN9f/R6xMTvUA+Oq8WXo67evNTpPjDuOaLUB56dywxrTkjc0GRCZLkiOECcJ6CTNqeksU2LqwfCKvTCxHc7tFPLwwFdQtwRRuyv+u27iztDnPaUa8lYT0qqqpThUoKrNoW6cz0bpwaR7x1E04Jj5CSNE/wLZ7vJIsQO8/AA8qmspeIjqFu4BLXHP4hsy48S1ufPyZAETCI/oYezH4TVgfL/nup+nJgu3DRExLKs4r8HC0w7g5+QJ3dOZTVuH9P3d9nGzNyfbqbpRCoqeXkmhlAcvrqy/5TCrx9frIbUGPztkBCI0KYxJGpZ6h45pemc6HYPDK/xU48P6kLODGTATCbqFkzB299r9w+xhQRmAVWjC7CjNO1LoHMTPe6fG5uf+q+Kspgq30NM8TP/sQw9CLQeAfMG5NG7bmb003Z3lDj5JHtx2oMSaqkTXTDq1AdqzJGgiFtgkwLnTJbg9Pj9Aq0pT3ESX55ktcvBLGJMWx7rKz0h1ohiyM8RL34phd27JXyz2ARGabqBV0bQIy1cpMVH0LJtvnjSpXsFakzpTGQlpHBZ/6Ij84KuVcioKgNM2onhmMa31Wnvx+a6lKg45kn39J7aQLjEP5SQmIx0mHCWTN89zGHNXKIqoJUzGRkfzZWPqqSuhhs7axD1ezo2nLf8aYjFWD4AadLNUAVXKSIZYR54w8CC6OOeahWGjRhR7nKoP9JWyRHig92PumeSVUBbIoV5xPlaIsSbMy3EqWF/3gJCPSWr2FNmEPYbYdAG9WB30k5q3mI9cUqIzb3A4RSYHHj8MU/f5sPhT5xoTq3HuHST4lE8nMagL5Rg7wKaa0e9pdi2QIrQow7e6gH5BoeOFnBOOonr5RkT1YBi50MVgZ3bbUNt39mutrwh5WuVxnMS/vs3MPngSWnCOvxQiTQz++abtqVxA==" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="UX">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="JFK" DepartureDate="2019-10-16T11:57:00" ArrivalDate="2019-10-16T14:30:00" OperatingAirline="DL" MarquetingAirline="UX" FlightNumber="3394" JourneyDuration="P0DT15H18M0S" Class="J" Cabin="C" AirplaneType="321" FareBasis="JYYOAE" />
                                    <Segment DepartureAirport="JFK" ArrivalAirport="MAD" DepartureDate="2019-10-16T19:38:00" ArrivalDate="2019-10-17T09:15:00" OperatingAirline="DL" MarquetingAirline="UX" FlightNumber="3392" JourneyDuration="P0DT15H18M0S" Class="J" Cabin="C" AirplaneType="764" FareBasis="JYYOAE" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="USD">
                                <TotalFixAmounts Gross="11827.4" Nett="11827.4">
                                    <Service Amount="10675.24" />
                                    <ServiceTaxes Included="false" Amount="1152.16" />
                                </TotalFixAmounts>
                                <Breakdown>
                                    <Concepts>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="5337.62" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="5337.62" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                            </Items>
                                        </Concept>
                                    </Concepts>
                                    <Taxes>
                                        <Tax Name="Tasas Others" Value="576.08" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="10675.24" Amount="576.08" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="10675.24" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="10675.24" Amount="0" />
                                        </Tax>
                                        <Tax Name="Tasas Others" Value="576.08" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="10675.24" Amount="576.08" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="10675.24" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="10675.24" Amount="0" />
                                        </Tax>
                                    </Taxes>
                                </Breakdown>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-10-16</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="4" Number="18" Direction="Outbound" LowCost="false" RatePlanCode="lZmAomcqR8KeVwNrCaYbm7YYwekKD4434aJbEwrpVfyzE48fargROzff5Ej7JNfS58krbGDpU2KukyWhbOjyOJESjP9hkGVjG1BsyPDXFYrCWhcAKctjnUq98aM0TymiSSskNxp/RvNJPZ/FrY/xENCiD3PG14XBpaqG+lVfuTZilKzpQiwbf+fv7+fo9F8ap0o8vdexp1ZXSVWnB9u1kzeBcqzNpMUVynJfx4HGEvhD+4tmURhmdI0+SUKVlD9Enu5VKyrRK7R2SqVQvrY3YfU0TdLOTBpkAVMJ6YewiJMjDAtpS7Fw558hlb3/s7OcQzhkwJdANxL9rk8HQSD+rhqoT+SP1PTsXOKxqRY6BN+uQesMu8d6QFojdZbH6MZymUdw/rMAwfbF6cf404MnHlCX8MKKznwnu6wS5Qj6Gc5afCXDw7PrHSBfRo+7+GC2FV4QtlOeWa0MaUSfUMy+fOkk0kCFmR8t5knmp7LIq/+aRtjMqMPh5Q3EqRJRNYZLqDg8wAFb4njjCdWxFXZEBB3FmH/HZJNp1d8YlKa8cP+QOz5uvcH+mKFTSrcWevGSDycd0MhWBMl3N1/5U5grQt9f8zneS+ekUGNGg0Z5iBO/ULyK4Kt7ywOniA6AkJbfPraYeLiPhdGd3O8xTOPYxdu9j199Qs9JyO8Xsgu5VUOiaU3VBw7vbI+Dv9hgcRhze2w9MvobfLPjne5cCrqXdYDOY+zieBE1cCZtE0N8CCbatFY2iyzndzBrGcwNGDXSHWJbKuB+PrhVre+Ec4zahuf9i6fRSOraBFC+fQXNzLGSylP+errBsNHRx82mcXWDXsbp2b5k104Xi+BNjClh4iV1siObOJUWc/pvlR46kpUp+ZCvaTX7sT2XOjiw3KR5PdXdThaDzwXYOSvRBESpkCyn/+eXdU4bAJpQTcZTTT1XZ4/pP40w+sMOum+tn8WdXQc87/ucd4f+YXi4AE1RTGxWyB2jNeUgfKiP3RGK5WurKbx8CZEKR1ZS1xImUQGK8Vz/wDV3JsfxJmKGBgLsyNWW2x3cBp144ARLJgzn/vD9OaWRg8/R/LPfmrYz6Q5YvUDR64OpOSnTsTdV+rP1Up6AoiBOshQ8gXXRFJPNC691tMeYGWSPIkNf8zqMFi/cR82u/jPzCmQDUXzpIAscxbOBntkqN8OCaBpWQ6RUtWgG6u7PjbTrX4UQNYv/NpGs3oDToy9eU/pwTsxG6Wfn4GgmHqs6SPsa8fWCowJOtjjKFwMALNVb4f79j7RnSOkaePJE0stDwsD5gDSRPH9Ao17590VBNA3/AffOmDOhancg2zqY6zE7Ga+MsZz5h/wAb2NA+tdt6GRjYQSjbrTKj3q7q46guIVm9O8MWJDO207nGBIKbg/z7dVdypk7SbT1tu/k5MAw/TBAnJ/U3ES2Kafwm1i0AySNe4u1XT5W1qtwvK9131qpxchRt+gxSv8/PkFaDxxFhj6xNrJ5Ay4Crk9Vo0z3sTN1mRcoH9BPUcajZYbkKVPdC7JNobw8yPdc6OFpjTN7ovTTD4FyWn++hXEcEAFuv1Rch/wMS6N5KkcSBj8iuBsxuUjwqoYpdxpkYOP0NjAFkB4nB25bCGuIwWzn7Tlhvtm0GZAFFm9m6yJimwTS7GefbPRpTf3PXDO8LWXWT0rMefV8gXgr8hmSoA==" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="AZ">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="JFK" DepartureDate="2019-10-16T11:57:00" ArrivalDate="2019-10-16T14:30:00" OperatingAirline="DL" MarquetingAirline="AZ" FlightNumber="3338" JourneyDuration="P0DT16H48M0S" Class="E" Cabin="C" AirplaneType="321" FareBasis="EN1H01D1" />
                                    <Segment DepartureAirport="JFK" ArrivalAirport="FCO" DepartureDate="2019-10-16T16:25:00" ArrivalDate="2019-10-17T06:50:00" OperatingAirline="AZ" MarquetingAirline="AZ" FlightNumber="609" JourneyDuration="P0DT16H48M0S" Class="E" Cabin="C" AirplaneType="77W" FareBasis="EN1H01D1" />
                                    <Segment DepartureAirport="FCO" ArrivalAirport="MAD" DepartureDate="2019-10-17T08:10:00" ArrivalDate="2019-10-17T10:45:00" OperatingAirline="AZ" MarquetingAirline="AZ" FlightNumber="58" JourneyDuration="P0DT16H48M0S" Class="E" Cabin="C" AirplaneType="32S" FareBasis="EN1H01D1" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="USD">
                                <TotalFixAmounts Gross="11950.84" Nett="11950.84">
                                    <Service Amount="10666.34" />
                                    <ServiceTaxes Included="false" Amount="1284.5" />
                                </TotalFixAmounts>
                                <Breakdown>
                                    <Concepts>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="5333.17" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="5333.17" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                            </Items>
                                        </Concept>
                                    </Concepts>
                                    <Taxes>
                                        <Tax Name="Tasas Others" Value="642.25" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="10666.34" Amount="642.25" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="10666.34" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="10666.34" Amount="0" />
                                        </Tax>
                                        <Tax Name="Tasas Others" Value="642.25" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="10666.34" Amount="642.25" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="10666.34" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="10666.34" Amount="0" />
                                        </Tax>
                                    </Taxes>
                                </Breakdown>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-01</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="19" Direction="Outbound" LowCost="false" RatePlanCode="lZmAomcqR8KeVwNrCaYbm7YYwekKD4434aJbEwrpVfwzLsKeZLMKL0hyu0QN68NsCOrT1ZePOk53LQTTRfBMre8ff73aWb6B8rJGWdIp/fOkV8InlwpzjamqMP9nTwAooMAvAYbQwUEzFbUoL8lQdiS4eh+rPKt32B7ojvTXbcf9tXacx3AacPGz/CqF7MwmUyzbzFhBD1xju2LPgWB5HafJwdA1hqAEb05NrAjShu/bpe3/MVc7K/R2EFKtMvwY1Vyg8PuJGzzaqyMMRT9umy+HYRjpG2cwh80aBFzkN2Y4QbB6G+ajgFqfrHelI5vuZNLvHJWjPHDAWnNF4oNfI6B29+79HZ+A817Kc5ZLzbxtEP/JAiISrAogpswezV2uBBQur8CvUJfkC3jZK6O9GcXgw1uH7bAxZvqIja9VFO6lDq40J8LqBpR+Y3qYonOcrQPhJn4UbhTf30WZLGSTooF9UJdYnaebAmRETryzmha/p1KYEISPFO+UECfd2l0s844fh6++siUdlDfLfhNEuZNkbVNkzuEtlGwBvEILx7+hgVe5zTqTbViqEf3CLPa36Y01WiTw0XXjZZpfOr9Lq1v+U0Md6kKcMGAe6LhBN9kU19J8tbXqpR6hAagjs6tpx/vDlg/sdbT32WbQux0/TBBGB4wiCYKB6ArAlOy/ntuWa1lDrrbcVlP8ACYqviW8rsqpARONMtPPvuvitAFGMfZt/RYvVvdMXrAb/21unBIZEel1FHr+/4/ioXckHAMRJ81DMeg7/BcVSlCHoCZSFl150PchcezRh2qLWjkr6l8zjI3yDwpa2jx8TxNah+qS90kOOV91DYa85iJJgXcsVwMfZF8LK5bZ+dbH5NJIoRsRR9aIKYJJ1mjFiq5C7mgGcIdoxXhGiZIrPqAm8YRvCJj7QZb9i4mH3Ph68zUUtGK+meF4ugNg737b6fN8VGq9OSvskyFmCUvZCcXEdRpyHqgt0R5zazadyJFVU4FtaCxQD6URuoHqd+9/fADvGQdRuOM9PBKZ6wt4S0Fk43cYQ0Y6MSft8s3i37f29XBRlYbRI5rtMfRfLLj2dKQTd2NKWj+TC1Xm/gxlHI40WVsdlG0oNRRaaFFmsRnlkwOSrqdXSMJNfnr6yHYbyjRrmBEcRctshOmdek+F8Y04arthBYfIWMdgRvrEtWtm/h2NjDpQ5w4+NmDtpP4jukmD+PZEHVbO/4f07pWMvKxH1w2YeleJk9EMiInmZccuab3PxAgP8th4xyc1dWwcFm0uMBZwHfFfYjsKql0esI7Mi+EVb1gVdW1Dybw1fveZvdWqB5q+tWg4T1ThmXZ/fzlWGJ/A" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="AC">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="YYZ" DepartureDate="2019-10-16T12:00:00" ArrivalDate="2019-10-16T14:41:00" OperatingAirline="AC" MarquetingAirline="AC" FlightNumber="1673" JourneyDuration="P0DT13H20M0S" Class="J" Cabin="C" AirplaneType="763" FareBasis="JEF" />
                                    <Segment DepartureAirport="YYZ" ArrivalAirport="MAD" DepartureDate="2019-10-16T18:10:00" ArrivalDate="2019-10-17T07:20:00" OperatingAirline="AC" MarquetingAirline="AC" FlightNumber="836" JourneyDuration="P0DT13H20M0S" Class="J" Cabin="C" AirplaneType="789" FareBasis="JFFEO" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="USD">
                                <TotalFixAmounts Gross="14013" Nett="14013">
                                    <Service Amount="12760.88" />
                                    <ServiceTaxes Included="false" Amount="1252.12" />
                                </TotalFixAmounts>
                                <Breakdown>
                                    <Concepts>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="6380.44" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="6380.44" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                            </Items>
                                        </Concept>
                                    </Concepts>
                                    <Taxes>
                                        <Tax Name="Tasas Others" Value="626.06" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="12760.88" Amount="626.06" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="12760.88" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="12760.88" Amount="0" />
                                        </Tax>
                                        <Tax Name="Tasas Others" Value="626.06" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="12760.88" Amount="626.06" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="12760.88" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="12760.88" Amount="0" />
                                        </Tax>
                                    </Taxes>
                                </Breakdown>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-07-30</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="4" Number="20" Direction="Outbound" LowCost="false" RatePlanCode="lZmAomcqR8KeVwNrCaYbm7YYwekKD4434aJbEwrpVfwzLsKeZLMKL0hyu0QN68NswuJYxDufFljophY7ODvpXshLQaeb4XgHxVjfnH30Gpt/daYWDPsLlL2Av1Gzm1RoyNWtJ1PBE2NZsDkfpDq7JedDY3LKSVDjunYBy4+kI0h/BY0MC+X3VkA1V5r7j1tGH9VkxiUNMMLGDaj5cKwVA+cDG+nLQemJbuJWqwUqWFnsKqQnMD1P7Z1tL7PXVDTR3kMUVCVA7sPI2lrtYaHYpjQhchQ+aMvd0dLb2D4uTFtT+ahMtTvFQ+gEbKit7YFcC9IuhtIkBPsvSFVlwbVBcNpQm2e5NOPl4XhHVxwn3r6/QdkG71m0puhsWr4BiKbkYfKNRo+HxTnPjrMW9o+rgrXbFvF8wwNU5B4uvpblIjnafIBQV6TRVS4++WBC2YuqpYmjYHhY99fP9/JbPNuvWzgAPLVPGAcJqqGyAEgWbaXCidBGJWRuDxcqKePu7ii6Y2DA1ZFmN2WFyj38B3wOKLeiQszfuR39WA57zGjUSMasyMjwjBjBydgQvooK7i3aS11ZYKE6t1gCfq2F+MTI1I4Ik0Ied1lbP8vEVh/4AKXXg97vOWPiMUdmOrAhhrxcmg6yraGV1dW4JB1GheRQ1B5SHwTAYlfVZjZvRQJ2Zpa/LQfNYoI0dnsHVOveWWl+Xy+jz5O1xf7MY22hw4rljaSZETiYhwO8dBucv8lugjjpdR0COhpMOWoSPyxN/VkcuRo1NI5BRLE6sDHGv5BDoVaupZn1R5XMXplIGGz8/75ZBrp4n9ZqTPdgxF9dHE8usNElHtWyIiZnHmPBxUXrNt3nipl94D3IGbMlmGCPKD2Y/Xd6JTX0z4kmcd/ZE6xiNntBq2eC8B3hVsR5q0lZlffh7iYgmrxnNsCslgZc1V9W0yvwcW7ONVPA7YOr7w6AdV5nQMe7+Aa697eTQjOQK45kp6pV62v+hE1fFUFJdyxaX4RMtZppESnXZ8TjKlr8NXNIsm9+tLTyUq3DcF9Io6FXdblg7VLmuFFaE7z+29Or+MNnKSbpnS+u7P58MJmKrmWYEECv7X8bRJuIgYT+zg/3nE6/7mToppWBLVeDPeuYB2Q4ZLyYdnC9iP4IqRh12jM/RPrfyATJgeuOMBlTdnSKh8hKWleINH3M1tgxzIDvD52vYS9D7moY57Bd0F1qkJIjI1iLcrBi+WjqS3KHvUiNBEFRxvXK+0lkLpLBuzQrAtVB6ctnyUVVwlMpiTwEZqGoGb50gbImt/lFJsKnQ/iblXp4E6PSHO2PafJdmp8U3CarjkNnCjP09U1nayiS" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="SN">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="YYZ" DepartureDate="2019-10-16T12:00:00" ArrivalDate="2019-10-16T14:41:00" OperatingAirline="AC" MarquetingAirline="AC" FlightNumber="1673" JourneyDuration="P0DT13H20M0S" Class="J" Cabin="C" AirplaneType="763" FareBasis="JEF" />
                                    <Segment DepartureAirport="YYZ" ArrivalAirport="MAD" DepartureDate="2019-10-16T18:10:00" ArrivalDate="2019-10-17T07:20:00" OperatingAirline="AC" MarquetingAirline="SN" FlightNumber="9628" JourneyDuration="P0DT13H20M0S" Class="J" Cabin="C" AirplaneType="789" FareBasis="JFFEO" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="USD">
                                <TotalFixAmounts Gross="14047.68" Nett="14047.68">
                                    <Service Amount="12760.88" />
                                    <ServiceTaxes Included="false" Amount="1286.8" />
                                </TotalFixAmounts>
                                <Breakdown>
                                    <Concepts>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="6380.44" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="6380.44" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                            </Items>
                                        </Concept>
                                    </Concepts>
                                    <Taxes>
                                        <Tax Name="Tasas Others" Value="643.4" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="12760.88" Amount="643.4" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="12760.88" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="12760.88" Amount="0" />
                                        </Tax>
                                        <Tax Name="Tasas Others" Value="643.4" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="12760.88" Amount="643.4" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="12760.88" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="12760.88" Amount="0" />
                                        </Tax>
                                    </Taxes>
                                </Breakdown>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-07-30</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="6" Number="21" Direction="Outbound" LowCost="false" RatePlanCode="lZmAomcqR8KeVwNrCaYbm7YYwekKD4434aJbEwrpVfyzE48fargROzff5Ej7JNfSZha9o1Vr5sMrVAr3+P/fNC5F4TegvFqWzb/kzDOelBFnC33QM/+BQzOfFIDzww6DuvODzFwGSjgG9TtHYsfYe2uEkLvQAZdRHjFQFG5skWWXqk30kNyvpczhmIYHVmgYT3KQTxE6N4Ni2vW4hvFKwhRJS5auF+Zzt7iUBysxML+YPhlU6EtPNU5kHLlQdT/6lC8kXqwj4y+MJ5tkaItz+m6ncLNm/BlF+UQ4sv1SphUQLUHyXoyue1GcCsbt3MK6gEypkN0D6TLjfhCAiBN9VaqaLzBBMlL5CUFdgs/qmYy2hUf3/NwtQ3KNRYK+GdRg8f/4U0S7hUFixuIsOROLY/lelwVCHO4670+Ltc0lbDTDSbBeutpTJFaoNsD5o8gdej1FMavUoqKsNwTxs4lsO9b/7JH45xKUIQ7G8+IXXuegfM+uCN70HzDmZJDcOSSSqcAhbHnwVjN3JmmAarqvpobP96BiOS+bsB2p154+fEWv7eeIyytgMx1tG4u+UkX3/QJAXaNGVowdp5phmar7MjW94Z+eUlvJBn9JgUGjASOAiVeIgumXuqZHImMJFGSV/UMGiwpnONVV/gmGKjhfyGgLjR+3xirBl92gJ8E7TtUbnnlULa2egGbrlA8qCvxJinzvu6jkq1fACwZn0K/U8sy574cvjDh0Nej+txPqqA7L/Ykgnwp2NOhlokJailNf3/uw8NjMtEZS95HZOntN8e//p4RQYi9TVkXiAnW4OZI0QvTHaK9QZBJ79s7GZt3t6XJvqALYAgUqJYSDbsVO+Cjj3nev74yVaEC1T97qIQl6B5Q+vwCeno8X0nw7948mswh2DF78QoQtb3RN2CBmXcNhE3sd/4evqzodZMs2MO91uyWbQFJhS52JKSN9GTm3OWp/TDqMRMlyX0Cz8umv44VgMQy8lFpfH391CfeTYr5mXBEgG3M0Nbih61PwT7S4m/lcLwpHyn2bsu7TTtNanCVnZ2pvb5T1OO8I7runK6pgbAXG3mSndgDKFdBld31RyOw0B44mg51qqcZHp7mswx2zV9Ih/EnZAMZYz+WCdsJQvQTmnL7uC7Y4kwjDmtmNaxqkM4EWJh62pMld0eblAhOSvKsEfzhXnrw3WhiTTORbNx3DBH9sGrI69SesuaokHB8IyPO7hbaViAuSyHR9pFMxurH4U92GNlQ25q0JzpjktSUGfg/+Q662V7xzKpgH0QEY608kmF1QS1DmbmKLdmtZ0ccjgJhfVzW95Tpc5P88AWDBAj3TJZgUNQeMDXeS" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="AM">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="MEX" DepartureDate="2019-10-16T14:40:00" ArrivalDate="2019-10-16T17:35:00" OperatingAirline="AM" MarquetingAirline="AM" FlightNumber="435" JourneyDuration="P0DT21H15M0S" Class="D" Cabin="C" AirplaneType="7S8" FareBasis="DKNN0XOB" />
                                    <Segment DepartureAirport="MEX" ArrivalAirport="MAD" DepartureDate="2019-10-16T23:55:00" ArrivalDate="2019-10-17T17:55:00" OperatingAirline="AM" MarquetingAirline="AM" FlightNumber="21" JourneyDuration="P0DT21H15M0S" Class="D" Cabin="C" AirplaneType="789" FareBasis="DKNN0XOB" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="USD">
                                <TotalFixAmounts Gross="14449.32" Nett="14449.32">
                                    <Service Amount="14392.44" />
                                    <ServiceTaxes Included="false" Amount="56.88" />
                                </TotalFixAmounts>
                                <Breakdown>
                                    <Concepts>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="7196.22" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="7196.22" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                            </Items>
                                        </Concept>
                                    </Concepts>
                                    <Taxes>
                                        <Tax Name="Tasas Others" Value="28.44" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="14392.44" Amount="28.44" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="14392.44" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="14392.44" Amount="0" />
                                        </Tax>
                                        <Tax Name="Tasas Others" Value="28.44" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="14392.44" Amount="28.44" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="14392.44" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="14392.44" Amount="0" />
                                        </Tax>
                                    </Taxes>
                                </Breakdown>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-01</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="7" Number="22" Direction="Outbound" LowCost="false" RatePlanCode="lZmAomcqR8KeVwNrCaYbm7YYwekKD4434aJbEwrpVfwWiHLAPFyfZvOKmaRks7sPjLOuEObV/y480ihJbqjgQKa5yGgaFLBZ8YCCzTiyHFGgy5fsoDkToMKxQ8c/jL83KaGgwlE8kFX3S1r5/rDpQKDe+aOwRMqdg/vMuxZW/A5IUk4yD8po1EYcMfoLuKhxcjRsKWGkGtSii7d4l3XtCTWqxgaYLdfwiOuHeUbYvShg+RJ10t+a3+KSta+kCPNi7tYItt/Df6ZXEhKmIvCiL5R9xzRMRxnQey6Gh6DZrAHf5bp2SfFwelXBEfLIBDKyTqYT7TVEbnqHTAjWmGLRxhnrORIeiKk6AAGGxhJOb1wIZJbymT8OayVcnmw7C/+i1UdvVtkmm0IbgRUc1jl6cIZBGivr0tKFTqJParnFHMjeYIiRU4sodhomlzT1b1OIohfCrni1TR5ZQPwX/c++3zFRmdz2wSs8P9jy8FCgR/VOpXhZNABid9euQ4PtKRx2+FpVeAh5u8yvvKZigAGoOrbT0BxvAkGvRUPNPAEdp60yKCG3GwOp+5NSlY7p8/R7bDOSOsogRlA9mIQA+0JSl5dIzFAFUJKln/BMiv8bu7Wb1wplyLg/TlVJesRBmuvwBkYUMBxlMJsXkmsDV9qOkylyXEewhh9npnz7ZAkhb0y2QsRfpbPcKPbgljWqRs8YLg1WCdZy+fm3y8nm3UkSiXMjXkFqMcWM2JIl+Yh6aHRPPVERdfnLHn9y0kGL67cQ1QgK/YqDoDYS30f7OcBd61UcVGla1i5bKP0+E6Bn3YO5bmTGcoQiP3SnWPFbhvTQ2hzvjeAwDp8PPv5LUC35Ew1OeFBK013rgnPt4wP6VKYN7ojYS19Ww+wy1sx4abGymJK9a6DcwEb3DsJ2SSf/lHRwvn6a1BoJ4hBne+62Bo8NLWCBjFuvisbXzwATG2/0vSp+6i8o8Tp1l0dNliCqj4P8j9QZiPEXc54JMLk4Df+KVGiQJGpNk5+a05ixsmod/58HNega5RKp8D0MvpippFjEDc59bV4Gy1AvWNL6+ikzksON7OhR5XivwOL/Jnh53qcjXZs1JagIDpdYPPMSeSeO0PQ1OE7RwIHkZDFCLrvYYk4uLtupyabDal6mbwuafw/JDIiM2eBnHvDw63Q0KJhQ1Saqvam0r289yL0TPPRtboATykKifow4itmqgdz3hNj23B4f8ZPrx2V9qgGkdPP6PQpBSwKohwG+g80NnYexSFMCFDh4+y7JPdZaOuMGel4DuS6RDyhv3R2YYVytxQbrEUEcMKRyk6TrQIPW1sU3Y7yBC2IU9n5vXMJvUMJBcE5ym3B6mCUToQOIYgFelQ==" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="BA">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="MIA" DepartureDate="2019-10-16T19:35:00" ArrivalDate="2019-10-16T20:46:00" OperatingAirline="AA" MarquetingAirline="BA" FlightNumber="1672" JourneyDuration="P0DT12H20M0S" Class="J" Cabin="C" AirplaneType="738" FareBasis="J1N0C9S1" />
                                    <Segment DepartureAirport="MIA" ArrivalAirport="MAD" DepartureDate="2019-10-16T22:55:00" ArrivalDate="2019-10-17T13:55:00" OperatingAirline="IB" MarquetingAirline="BA" FlightNumber="7260" JourneyDuration="P0DT12H20M0S" Class="J" Cabin="C" AirplaneType="333" FareBasis="J1N0C9S1" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="USD">
                                <TotalFixAmounts Gross="14976.6" Nett="14976.6">
                                    <Service Amount="13731.36" />
                                    <ServiceTaxes Included="false" Amount="1245.24" />
                                </TotalFixAmounts>
                                <Breakdown>
                                    <Concepts>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="6865.68" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="6865.68" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                            </Items>
                                        </Concept>
                                    </Concepts>
                                    <Taxes>
                                        <Tax Name="Tasas Others" Value="622.62" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13731.36" Amount="622.62" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13731.36" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13731.36" Amount="0" />
                                        </Tax>
                                        <Tax Name="Tasas Others" Value="622.62" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13731.36" Amount="622.62" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13731.36" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13731.36" Amount="0" />
                                        </Tax>
                                    </Taxes>
                                </Breakdown>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-26</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="7" Number="23" Direction="Outbound" LowCost="false" RatePlanCode="lZmAomcqR8KeVwNrCaYbm7YYwekKD4434aJbEwrpVfwWiHLAPFyfZvOKmaRks7sPjLOuEObV/y480ihJbqjgQKa5yGgaFLBZ8YCCzTiyHFGmFRSJEU1jjPd4t+FzC9DAmN5qwQ3kbcZDFZViLzKj1d3KvibJAHL8TLGXvIZruj2h8VA0kEky3DIWlMd/mRZm6D8IHK3zO5C5nb5hUjSsDCQoN7U1rT6Qv6ZmASN6nwtGDLeBZzFqzI2VL8KomnfBmRLCQMFHAGch17vYOmGRIoZXT1yp+gibI+hUoNfuPVRiI+gjQljB8QZ0CO1p8d3/eZtVcEIHBS8kM7Qc+/lN8QSa0Br8Q/KiFqNIX2KBYhSNMYgz611rwI328DquEtzJ49BKBvoNZYj27vd2Oeh1XUFT1n6rW82hTDMrD1muPZQDEr85uEy/UAB88RmBd4wvK/aig5wCi30H1nptLLygZ6LM7xZrvoCrVnolQBMc8bQBt8AFTCPvEA6mXiVY9RA6MbkLurlmviX0sCPZ/kBs6v9Md2mInx/ZXzC4v4N3OTc83IvpxgOhssv6EEzsqZfPsDrLD4kwtcsQHI39WiTk955PJFL8WzkAit/za07q7WaGufijI6u6kNhzYx/8jmG2M6fE1UoAnfEeF9dYKs6X4pdRxDuoyQvIq5XEyNfejB3QYpu7bVxeHSWcnPcFdNGOO/VUlgkVtQn0xDZuuOqgR0RPVnRL/SyQSxcc0dBRG3AF6OCjiE0e4hr5MvztqhN2NT7Ng1iQY+22OyqODnRXShnUnkcuGgvoxAb19X0Paj56JL6FzYj6MS/wM5cyFkJ6hsx+DneqkzYS9lRs+IT39FdpSbP0KUHN0b0uGrkbfPDH4WQL6cs9tWJeAh5IZ8fQS/gTrSHoHc51pqXRYv/JmXBWguFgEQ0ApzEgEYRPVmTRfMPjmuFx74/AfnhmiW8E3h33SQie5WfEN9ZvLlbxJasEdZf36BjjWFrH8FyJK/WZkVq5Yt239zlrGsBHhyY+twyzuBvvnfSU4Rz0sEMxlsGc4hhKgEIztXWD3d1yIuOjNO96eb0PyZGyqWBSRW+fs7LVuZq1mGdHzlrpTt674iuAhpI2xl6Lb/gpGquX/xpsQT5pKDS7VXWba/40A0iXwmWv77fq2rzOoiRCq/vb8HWpmu56TX/sO4qUpWVWJt6v1EhVvjHGMrQMSSq97JrIAipodhCj4hzQXiXHGJcOnysXMrSA0Q7+PslWJNf3mFkDh2kVatH37Gikh1y7yiBTBXSAhxh4Q58NeoP1bJfO2VNWjdXgSQ0ZnbcfTT9yPhWOTjxPqNrpbzkMm52HsUI+9ePi7X8eHonHy+CWozwgZw==" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="BA">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="MIA" DepartureDate="2019-10-16T17:40:00" ArrivalDate="2019-10-16T18:54:00" OperatingAirline="AA" MarquetingAirline="BA" FlightNumber="4320" JourneyDuration="P0DT14H15M0S" Class="J" Cabin="C" AirplaneType="738" FareBasis="J1N0C9S1" />
                                    <Segment DepartureAirport="MIA" ArrivalAirport="MAD" DepartureDate="2019-10-16T22:55:00" ArrivalDate="2019-10-17T13:55:00" OperatingAirline="IB" MarquetingAirline="BA" FlightNumber="7260" JourneyDuration="P0DT14H15M0S" Class="J" Cabin="C" AirplaneType="333" FareBasis="J1N0C9S1" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="USD">
                                <TotalFixAmounts Gross="14976.6" Nett="14976.6">
                                    <Service Amount="13731.36" />
                                    <ServiceTaxes Included="false" Amount="1245.24" />
                                </TotalFixAmounts>
                                <Breakdown>
                                    <Concepts>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="6865.68" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="6865.68" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                            </Items>
                                        </Concept>
                                    </Concepts>
                                    <Taxes>
                                        <Tax Name="Tasas Others" Value="622.62" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13731.36" Amount="622.62" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13731.36" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13731.36" Amount="0" />
                                        </Tax>
                                        <Tax Name="Tasas Others" Value="622.62" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13731.36" Amount="622.62" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13731.36" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13731.36" Amount="0" />
                                        </Tax>
                                    </Taxes>
                                </Breakdown>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-26</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="7" Number="24" Direction="Outbound" LowCost="false" RatePlanCode="lZmAomcqR8KeVwNrCaYbm7YYwekKD4434aJbEwrpVfwWiHLAPFyfZvOKmaRks7sPjLOuEObV/y480ihJbqjgQKa5yGgaFLBZ8YCCzTiyHFETg5PVj4+3N0HlTbUuNCrgmd4iXK279JJ0OQzsjQTPpum0ybI48NXImAeUlgtD21MeKN63FpTtK24rWcY844AkoQ2fZQOYys/iEgTo9bwFg10sKeB5TFi6/usSzKvvXls1+rmzsiWfsMKofls49X7P4exE93dWcsvrvJJ2zGAIN4kO+GUV03AzWUkG2Vsk0SYDPg4xK5GPxRXXnZCff1qkuU2WTVuoLd3psNiln+KrDpPc0xurTedc4579nTL1Q+AzPNvIBVXy3Vq7SH6zI9/0wJoxl+TTilTon/6BFsMydL8b6SMUIOpZvCCG+bBtl31RqmYDeGGkYN/kzbC5HkZQ/MEQTSN9XGzI1lFs+VGlyXYfxyaGVnIokkNcHfiUaByKw4BMO2l+iXJ971R42UDIjadNvGNNdEw8XEgSOYOS6Yii19CzwImN5KAQ/CymzxOWfZC2iSRZspoj/PzuBtyuKm/n/fBiY2nQlVnvKZRYeKMBbCKMKLFCW0VyRV+dvPoGQoJGduUEEB8QBknm90kwCR5w77moj2+YoBNs3KpNct1x5rBv/KK9wYkwzET/PhpS//K+OBGVuRExGhPeaHj+liI1rJW267YH8lDpMzYB7IdWbs6Mf5sytS4SaX2RWHvv2Xj4ANYALGyIMakyIq5FT1DR1xDpvXkZQs2gb5KWBYboNnAquRwnvZBEEtxJM+LSPwUYoNeC02FSfIQDwZHo1ZIog35sh/R4V3UNQqR/kyswDtgxcvz1LreE/npQRf3vhSQASEiwqTQnX4DfU7gAwJphdHrYDZlhCxHD6Rjdj02ycTomQnkDnZd/idLQpcImSFWQ48sVOnRR/x+d+LB07xGjmE34Av3jg5UX7kyL0hTdRqJE+GhZUUcHoWr/CY+tj1gGun9lRD/fRO56m0D5pdOZa+UToCohnC7CLt+ed4E+fhelHdYBNmGxR+YwVNt4McpcaVkT9qRkDSqqok5QytGw82mXDnFfcz7b45RGkqg0k/BmI6EQnn4Ur6dHda08SIZXpQbMpKc3ahpNxtplV6jvj4dyqnwBnMwa5fd8fA8bVDijYS3dqoHxrV42YdR3XZOlpr2Hb0hTOWFYbkV2MrDYUxCBojO9YcLRH6GrU88Gh8I+SW52VznZ0u5/HP1wHg9fih5Sb6inUQbzyfKUjWItB553Lw2zCb5nYMEfml7mWifERbosVG17ZN9lLIdKGtFQ3Tzfn3cIsbriqnt43uqiMbw1yJjgu7RIHCmarQ==" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="IB">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="MIA" DepartureDate="2019-10-16T19:35:00" ArrivalDate="2019-10-16T20:46:00" OperatingAirline="AA" MarquetingAirline="IB" FlightNumber="4692" JourneyDuration="P0DT12H20M0S" Class="J" Cabin="C" AirplaneType="738" FareBasis="J1N0C9S1" />
                                    <Segment DepartureAirport="MIA" ArrivalAirport="MAD" DepartureDate="2019-10-16T22:55:00" ArrivalDate="2019-10-17T13:55:00" OperatingAirline="IB" MarquetingAirline="IB" FlightNumber="6118" JourneyDuration="P0DT12H20M0S" Class="J" Cabin="C" AirplaneType="330" FareBasis="J1N0C9S1" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="USD">
                                <TotalFixAmounts Gross="14976.6" Nett="14976.6">
                                    <Service Amount="13731.36" />
                                    <ServiceTaxes Included="false" Amount="1245.24" />
                                </TotalFixAmounts>
                                <Breakdown>
                                    <Concepts>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="6865.68" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="6865.68" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                            </Items>
                                        </Concept>
                                    </Concepts>
                                    <Taxes>
                                        <Tax Name="Tasas Others" Value="622.62" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13731.36" Amount="622.62" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13731.36" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13731.36" Amount="0" />
                                        </Tax>
                                        <Tax Name="Tasas Others" Value="622.62" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13731.36" Amount="622.62" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13731.36" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13731.36" Amount="0" />
                                        </Tax>
                                    </Taxes>
                                </Breakdown>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="3" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-26</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="7" Number="25" Direction="Outbound" LowCost="false" RatePlanCode="lZmAomcqR8KeVwNrCaYbm7YYwekKD4434aJbEwrpVfwWiHLAPFyfZvOKmaRks7sPjLOuEObV/y480ihJbqjgQKa5yGgaFLBZ8YCCzTiyHFEIv3BpMQVrSQPSg2kt8QoYGnmIsMOIRlAvM6nKIp8vnFRg2wXyB/C6TDL275Mor+CTLW/sFTeNRUOyTy5ZqrWvqC1CkFYE9qFFvHC/AWGSE+WLvfmjhYfOJ7cLSEnvZa8jbWUY0zJlC/RgLa7ojC2kg2AwI0JZtY34PfMN/uNBENu1mb7zEwSeYo3Cz5rh/gjqcDgAn8KD1LrzbFioNXjPsg44sqduG3C/48tA16rFPnIdiANjbVCu4Yo9i7RuTSBgeUvUSRfYRD1P9UeIEUJuyz6/DZqrNodyQ5C4pV8ItXLKtLEh5/vUFEMsQmLINEZhHP3NijP0VET98/uvVPr8Rm05xM3cE2Y0xI+SaX6Bj98LgmPVfQbeQxS5gBmGTqMreghynbDIqlTobMyXA4B/hMdfQZ4JzBeEWcJbL7nmm+VaV/zxHMX8fAikCLsMXTC9EFQ8lxejXKcMp+PhJnxsWaF0Bu1wL5CDKj29X6vMeOiTe5uIyQYbUM4mnswT1bIi4UAGMX84vr3eol9AiFq3Q6kNHdx6/kdNaaJJ4yG1buykkv8RydSLch0yX7C4UIl16doiKnfOLT4K629DCmPn/yyeRYjaYqoWpUdmBxCYmjF5YVB9qT856pFgEQI8H5MPnOCyYc3He8xn29at0f+DIPi0vOJ7brPR45AtFvHmj/QC2uKFbAE1vB+SCMmVyKWGpjXAPEqN1/PfkNXHhTPOM2rPWhEY0zb681bEvjQy++QJ7rgy8yLnZw2Dim1Er6Tm75tFSHttXSxv1JgF6poIFDvtZISE2S8BlvmckKHwakIIkmwTNm5Ffq28DOSlVRNCyh+EgEybEWBCeYDQA6FXV66rLw4xUEZTv7DZMTGkJf0SamoqrlSNQyzFvp/UZqMVOf1ZqhK9NXlgtAuxCeCcozx5DTzmixdiCMTKcH6qQrK8CJhjJM8Z+8Fnxv44fSA2JTW9Ki/o5eoWenIrJSFiW+JUkMp4JAGtukwqupmTVRv4OQdzbmqJr1I/8VaXUgczBt5fy9C4pR3Z0nGAreN/hIms4VePr0tk55pGqsRL9aAPZp03h2kGOaeary9JzP5y3geikUzaGC17W1NWRlaEC33EaLApOGlqiDPYVEV28qliRs7K7iOcfhtmoh+uigGKJ98EoBzNwcUhaYde6D164jLPyE/d9beNCxrknSEKHQaAA4MbvDrdx9DHRTpu+e20XWPWdnsoTxQaAwpcuGBosqKwFoxZQf8Q5lnufiwGtw==" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="IB">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="MIA" DepartureDate="2019-10-16T11:25:00" ArrivalDate="2019-10-16T12:38:00" OperatingAirline="AA" MarquetingAirline="IB" FlightNumber="4532" JourneyDuration="P0DT13H20M0S" Class="J" Cabin="C" AirplaneType="32B" FareBasis="J1N0C9S1" />
                                    <Segment DepartureAirport="MIA" ArrivalAirport="MAD" DepartureDate="2019-10-16T16:15:00" ArrivalDate="2019-10-17T06:45:00" OperatingAirline="AA" MarquetingAirline="IB" FlightNumber="4610" JourneyDuration="P0DT13H20M0S" Class="J" Cabin="C" AirplaneType="772" FareBasis="J1N0C9S1" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="USD">
                                <TotalFixAmounts Gross="14976.6" Nett="14976.6">
                                    <Service Amount="13731.36" />
                                    <ServiceTaxes Included="false" Amount="1245.24" />
                                </TotalFixAmounts>
                                <Breakdown>
                                    <Concepts>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="6865.68" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="6865.68" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                            </Items>
                                        </Concept>
                                    </Concepts>
                                    <Taxes>
                                        <Tax Name="Tasas Others" Value="622.62" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13731.36" Amount="622.62" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13731.36" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13731.36" Amount="0" />
                                        </Tax>
                                        <Tax Name="Tasas Others" Value="622.62" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13731.36" Amount="622.62" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13731.36" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13731.36" Amount="0" />
                                        </Tax>
                                    </Taxes>
                                </Breakdown>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="3" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-26</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="7" Number="26" Direction="Outbound" LowCost="false" RatePlanCode="lZmAomcqR8KeVwNrCaYbm7YYwekKD4434aJbEwrpVfwWiHLAPFyfZvOKmaRks7sPjLOuEObV/y480ihJbqjgQKa5yGgaFLBZ8YCCzTiyHFE+ZDQPdO+6O8vLT/4OZaSClGR7NM7ZN6VHdkT0hokA3g8HvmuMpebhByi2XZKtTVmsEjbop1uBLSubprSK/iR1kBMdJU6DIUvLIIV4DyLaWPf/EdTOXKiLsnG0i8cFg75Hww04h7V8FFaN+9aph6XqsPaC0qpBhFfOpCUi+KFc1wIxR1Udd6TGDWy09MvMurbIdFtsQcBhS9h1ZDS8tjoPhnYf2Rg9Z571oZdcY3hb/rGlf/Ss6T/qdEGBmD8CIJRXVqrqR5ybn124hn4VpxagANA46yxFYnfFUmBTwUU/p+DTnNo9oNR+fIcduP7Fv8RLnHPqOyEwxop+DNmtFpW5xwjxmbp9u663Julc6hGHJQa/++THYIZMBduC1WdbFkvedWrcggO0HTOq4WTWCXIhy+8oo6i3iv8FQhhaiHhirc/OmPhhzaEzi09MYs1GJ4A76kGODvZDxEMC7BEEjn40x+0G29ILXkh32bJn2Td/lLUZrehXCaLfr0ybk2eNClXmf1+J9yN0NBRMsbqw/cfb3a2mx9YcJeABej7//v0vq6YkO2pVj6tCijWl/m+ymwwXm2P27df8fkIgTzQ1HpX2QkNMEH8j1qVJUb8SEarEIdB1FAKO82WK5lPUcG1FtVMk6vYrFeLjugzFZ3NHTSwxHmtdbOqbvVzhWdSlzJqY5zysqEcikdiuwfcI2N2ihY46uX8vAzBmAy3tOANvuGy7OkJrkHuqE6ta8ygH9mpShttjH9oLXQrHUlcGKtaqtLybUPrSrDqFQ1r2Z4NAwIHNg0SQo7yT2aLjg+5sPEO7KRSap+aT4pchKDMofeE3qx4rj4EDE/QsCVBJeJYaHj46kbOUkJFN6SGlBt+cvcUo5Ab+4xK7KCLRH2ah1dRaA9gjuMMmoFm05+EhiFb7IaalmgEGyYRtaevMOG1BFwo5qSD4FimqRcK0x1Qj7tRufdgzbmXlEBgRd6FTHcW2C457MQN91GnPxX6Cx8oNgk00/pQeFn00CGijWJC1rCL3NuIhqWnt7zIM3vUFHJ28pcOBIlYnKJVuD+bJtR8yGmabiz13TlpcGRAgarrQFKvM1SSRWp2KBkRzcMeKPawNM5m+dN3FAq+uLacK2yUvVt9kaZkVjsPQC072+lIpuLlkC/7qS1nMfturRAYQGjr1hEeRd14brKbEkFDCvhXllMhovftKjrNEMeqKMHzmKn2ndZxfI0HeV1Ha2OgeOIGcG+p3VofBTXLn9KBnwo64WBzXtA==" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="BA">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="MIA" DepartureDate="2019-10-16T11:25:00" ArrivalDate="2019-10-16T12:38:00" OperatingAirline="AA" MarquetingAirline="BA" FlightNumber="5130" JourneyDuration="P0DT13H20M0S" Class="J" Cabin="C" AirplaneType="321" FareBasis="J1N0C9S1" />
                                    <Segment DepartureAirport="MIA" ArrivalAirport="MAD" DepartureDate="2019-10-16T16:15:00" ArrivalDate="2019-10-17T06:45:00" OperatingAirline="AA" MarquetingAirline="BA" FlightNumber="1558" JourneyDuration="P0DT13H20M0S" Class="J" Cabin="C" AirplaneType="772" FareBasis="J1N0C9S1" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="USD">
                                <TotalFixAmounts Gross="14976.6" Nett="14976.6">
                                    <Service Amount="13731.36" />
                                    <ServiceTaxes Included="false" Amount="1245.24" />
                                </TotalFixAmounts>
                                <Breakdown>
                                    <Concepts>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="6865.68" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="6865.68" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                            </Items>
                                        </Concept>
                                    </Concepts>
                                    <Taxes>
                                        <Tax Name="Tasas Others" Value="622.62" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13731.36" Amount="622.62" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13731.36" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13731.36" Amount="0" />
                                        </Tax>
                                        <Tax Name="Tasas Others" Value="622.62" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13731.36" Amount="622.62" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13731.36" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13731.36" Amount="0" />
                                        </Tax>
                                    </Taxes>
                                </Breakdown>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-26</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="4" Number="27" Direction="Outbound" LowCost="false" RatePlanCode="lZmAomcqR8KeVwNrCaYbm7YYwekKD4434aJbEwrpVfyzE48fargROzff5Ej7JNfS/b3ISIY5l2vE+rDqwRc/lm7ZAStDnZbpGlBHGJbsMCTt/DUHAogRTKZ3FV1L2bXJJ5ujiLviyGQ90HJWwjkhD9ZCnjbfrTU/s/6k2wpejxf1EmjeDJBS0qzLM3TfSMnF5Bz/RthGrE7hpq8Bz4sSeDJ4N9WzGS52NCHgCd01D2iecOFX23MHv3s8G0oXCTu2I3Fq3HvdGPkXXOe/csxdOniMprYZae6vjWr3G2SaZzpB0KNNi3Js9slnExFaecExHOB/hAtNYQX8ylGvaTF75KpNCSdtwRdDm8Tpghlhelpi1nKN4OTqER3M0oCvjnZ2wm5KAo1JfcwbkECeksdweQSErS3qRAoo+NoitYA48oNN5GzTgZWUGd0TPX0kj5vdQ0pYZ/Qd5W9j7VEy/yIai3haoZa+6pCwJurgtETHnnLOb7gQ0+W3ENzHixrub+RHSsC9aeE33YBPcxgQ/Bpacu7SgVe8dxGFWgN0qSdr7FJxt3PahKi5o+ZUbfBN3zNOq2CJ/ZLHmP+IN2G7k3zLPtT0dKk6llavl4XQ0k8g4ntatr6Vk2WbO2hDqV1fwvAxdyqjXqaGG+3HNTQPn5+b6mNSxSXbDzGjEbMNSezFGXnvkXyk8Elu5C2DXefXtmnSCA3llMNFVnGoEiwynGlQ/AqP71FURctxmnb/5MHHvEYoDyd/zUx0RYmd5uV1qWo264q4s/ugXY7lQ5Tex2owL7C4yNvc86qKgrr5JGgEKnprKr+bWscK1RBZR5FUzY+T8we4KBeGMJA7fD/0v5nPoYXHwlKk/9JjSorY3mDAsICaEMJJxE4beqq2NqG9+D+2R7XC4kqg9Dd7C/53OH9ihcDdtGCP3UYMckWQSUkcUA6SIz8A+Te1z5vFfmtrhhknMwDtAIj0PRmQxCkmS4LGW1HIstROKEMNL7uB8dCwi1kEV73o2I03TQVVHJZYFcB8fd+F+w9gXhifzVj0Mt39PBB6Yi/x4OvYPt0ISPCUPTCWzDJUtzRVup1K01u9zKvO7q1IGOKe2FRgFqIVnjV0rI9tKm+KPmXjbEJDfGWPGN7OZew4UKqiXXR8BRaOSkFZcs2UuKNk1GvMQuRxe/INEUMfRl89sEQXUT7AmoFE9Gc2MiKDMgu6ULaranqcgTaHIjf8M0WV+i6EbA4j3LJekhSisYQ63j7Ht1MsHw+phIhk/c0pBLx5cLkFttxao7dRTUGws9wW+vcjxsl07Bi8Ib3yyPEHLpO6eWX7q+u3YVo1UqtphxfhNRRgApKZYkEHjIQSqZKVf4YSg09YcYGCow==" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="LH">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="EWR" DepartureDate="2019-10-16T15:12:00" ArrivalDate="2019-10-16T18:00:00" OperatingAirline="UA" MarquetingAirline="LH" FlightNumber="8746" JourneyDuration="P0DT12H8M0S" Class="C" Cabin="C" AirplaneType="752" FareBasis="CNY00EFF" />
                                    <Segment DepartureAirport="EWR" ArrivalAirport="MAD" DepartureDate="2019-10-16T19:55:00" ArrivalDate="2019-10-17T09:20:00" OperatingAirline="UA" MarquetingAirline="LH" FlightNumber="7970" JourneyDuration="P0DT12H8M0S" Class="C" Cabin="C" AirplaneType="764" FareBasis="CNY00EFF" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="USD">
                                <TotalFixAmounts Gross="14984.56" Nett="14984.56">
                                    <Service Amount="13704.64" />
                                    <ServiceTaxes Included="false" Amount="1279.92" />
                                </TotalFixAmounts>
                                <Breakdown>
                                    <Concepts>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="6852.32" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="6852.32" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                            </Items>
                                        </Concept>
                                    </Concepts>
                                    <Taxes>
                                        <Tax Name="Tasas Others" Value="639.96" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13704.64" Amount="639.96" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13704.64" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13704.64" Amount="0" />
                                        </Tax>
                                        <Tax Name="Tasas Others" Value="639.96" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13704.64" Amount="639.96" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13704.64" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13704.64" Amount="0" />
                                        </Tax>
                                    </Taxes>
                                </Breakdown>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-01</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="4" Number="28" Direction="Outbound" LowCost="false" RatePlanCode="lZmAomcqR8KeVwNrCaYbm7YYwekKD4434aJbEwrpVfyzE48fargROzff5Ej7JNfS/b3ISIY5l2vE+rDqwRc/lm7ZAStDnZbpGlBHGJbsMCRJSGbtabBQwmIZjKRUUtd1XtbwY0Aky2cC/AfMmsB9XdNNiC5V/Hew+ZXjqu8awNIltBMKLXN7XWUMbiLAltTS3NwfYoh0uqTEurZcJN9mIztP1xA/nR1vMClBAlqmILfxcjmp/9DGqp5cXobPturgfkBcE77Lnc+0i8Mpchm3Uyz4VcAykKvYvC87Dwmumh/CtgSvzE65gr7wY9HYASGEjkpW3NAgQgAn66anA+vgwcAgj4dYRL/T/Kyn04oz9AFbeYugcEUVkilesekIJN98EaKGGRAw4jjwq59FcAO4ahamFrSSV6eFc6YiZ4ylAQLjpHYCwkFFHaKuJNFeUrlYNZD8oeIIzJtB6taQCDmRrr9TkDnsoboATUtueTIgnH7IdLgrcs14N14d92qRHZXQCtFl22SWEccbzJ03PfnixMm67BYjp28jQF2soXMT6DSLc8r0v3ju1cnvLf/YYURA7v8pYWtHdahVFb07ChmF8ncPatv24zyao/BpnBsiPiQQpWPTww0M60omwfBUoFmxG0aVukXs3wdtx6xbVAps2SHmUXZXVKwVKdit01Q7FKhImHh6fJYsSZWb7SqBrOIQVChl8dNWWPEeBYKbHsAltri1LXfQJOiUS53QwNAE+CDZfIv58cb12tb1UTrNzRmCqCUZ81ws+Ae1ZQKGUcA2EiE97Uy2abqPNtrygc2RfnRkpbrwmcoItFYWckHkDq3oGkcshIMS4QryqSQLyHuVmgvMvOw1WKPo8OimlORDvg9pnIeFiy9P0i6RJm2Qz2mOlM05OViQvx4ZT/mmJuDnrU4ITNXXTKB563uZs5wycRBUDJXsfOSwa+zMpZWpcSN8DKXf95tKAtOG4dSMLQYxD5gZI143dL7icvFFu51hpL5ZjnwRHDoYmHJpY70KsWVQqKVS/XV8ZSudGMaayos1nkI6p+P2UNPoktxe3j2Oxj4OQA8brKZZbOnaewcrVfqshluTsV7w3GETVreW/5f3aZLtjyV3ta79mAnKa8lQ8QjVX5MLlx1eQ9oIjm9SeYI4ERD/LqXiB50Hx1mfWnIcrngSzVvQV6inOtSYTOM1XFVhkOlqyneDwheD4zrdvNxNQXQlDSDxAZaUvVhGIIQo3/wG5gtzXjhoAZ2tnla4XTj2wZHhUqVYkTIERB2lRGMT/Zl3gnfqqQPwDkvLh8FTMuOzjOVx7EVPEsqBnj51NSPOOA+AdSQV9P3avMA3XptoVEpNzlm+NKc9qD/5r0Mzzw==" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="SN">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="EWR" DepartureDate="2019-10-16T14:21:00" ArrivalDate="2019-10-16T16:59:00" OperatingAirline="UA" MarquetingAirline="SN" FlightNumber="8867" JourneyDuration="P0DT12H59M0S" Class="C" Cabin="C" AirplaneType="739" FareBasis="CNY00EFF" />
                                    <Segment DepartureAirport="EWR" ArrivalAirport="MAD" DepartureDate="2019-10-16T19:55:00" ArrivalDate="2019-10-17T09:20:00" OperatingAirline="UA" MarquetingAirline="SN" FlightNumber="9027" JourneyDuration="P0DT12H59M0S" Class="C" Cabin="C" AirplaneType="764" FareBasis="CNY00EFF" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="USD">
                                <TotalFixAmounts Gross="14984.56" Nett="14984.56">
                                    <Service Amount="13704.64" />
                                    <ServiceTaxes Included="false" Amount="1279.92" />
                                </TotalFixAmounts>
                                <Breakdown>
                                    <Concepts>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="6852.32" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="6852.32" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                            </Items>
                                        </Concept>
                                    </Concepts>
                                    <Taxes>
                                        <Tax Name="Tasas Others" Value="639.96" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13704.64" Amount="639.96" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13704.64" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13704.64" Amount="0" />
                                        </Tax>
                                        <Tax Name="Tasas Others" Value="639.96" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13704.64" Amount="639.96" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13704.64" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13704.64" Amount="0" />
                                        </Tax>
                                    </Taxes>
                                </Breakdown>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-01</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="4" Number="29" Direction="Outbound" LowCost="false" RatePlanCode="lZmAomcqR8KeVwNrCaYbm7YYwekKD4434aJbEwrpVfyzE48fargROzff5Ej7JNfS8TXoii5RAViUzCpNcWT1Id5TD+sm7sQ8g9ZzZ3hQIFuGY3fyT9f3zCzsWwLfWRaJrxVE3ik1TnxI59xHbXa7DCQc+GuUPfAm1hejCgo4ozJRksOnBmQiv1ecjnu01vC1tcmhHQCrRTXa2GvN0bsKIvntCXnK8kc65brFbI1QlRklEBKeg1dQNw/ljrEOlCHmRqRJTcc2tZEpZAGE8J47hlfLv5JIujHtLKg5ZW9YJpxe0YIO0lwmtL2BzHxEAEXM9fGfVGplkFFU0mdMKB5i5Qz3HhzPIpkBLPKFIHYLf+SOWx0uCXcHPdk6v257hQO3ZzuNhkoLQv2uphY4SF38EjoEhZLVM6t3lkCoT+Wl9jTQT+8KyUdDHl+IugU5j9Q8UABP1ma6IVJw3m4tZjcakyN0DpXSjyH+PYT0XcxyCGbxkDnowlZYSau973YRgmCCb6KJ1OmjFCkSXSzpbxoRGveAuWp7qDiaSV04dGSjrbVgj3YJVFYwfueKjTmypDCz8noqZriWlGkboFjKXp8HC7qPhFVL/WIcSSudi8j/B1oTYf3+wZoWOOaJCix6+DwTBI7gy48aDOh9dTOJQdTSTEBR4oVDx6LVl9DjJU1FPvY6x28FMKV7r3R9M0WbWykWw9p9zvzPPIYOLD4j8DCW1o8yxDf6P1+KFdeHF5QRQQ+eTnEH8FDc2n30idJUO1xN3+vTAwalLqNBMrutqiQYjnU20rMNMjagmeUo0cSZWa06DKsCjBWLs4Hc/AZAhA4HacU51ycPjTV7ZhjmmVEN+5+s8XdXJGiqRsqNxcS2mkHsrtrmufJ+Hhaag/ZkxstyWayn0MsmfFNL2su1xICceJflxX/C46prPiqZloLZrfJTxNK2ziUV3h8ludS8pdfemWn0O91CK+SF57gmy61PQPYk+Tx1xT2SGeDWNlVWkt2BhH31hJahumoVLQ6/2Wvx05YNGp4eBKEdBj7dLJdapKMHHMbWteoU4q3EHHFVyvsuj4ENRxL71loxx6vfRjmL7JnYwNina2G6OPm8vQMM15qDfgrRMYLHN6aGbVaHdX//mIrjb/YGq45yoFPIF4D5VogSziGW7kqiq9rQbO6oJyxskgnw3M3p8MW8fjSrWAX8j9uipwVgIYsxHo0EMdgaMXd1/sseQEGA4Wl6+fWS1qHBYkZPh+abX7jGQsCZ1yXZ/XuKNS0YgZWQQg5DdJ4pRQYQCbGmF/4ECwoyB/Rc0G3vdu9nY3z+hMyliBFXXj5UVjkSDz3sOCDKaIbTfQeGX5SlOiUivgIao4Q5gT66GJsztbRRQNh9QxItQKQYVdanKEYkVTcv7w83PRjNzcNLcOUSwcjTGgCxAR6ksyXjMoMtmnc868YzV2znorqLf7wgHZEPigR+8Xm1PBI+hew39L402B81ur+xvb4N6FiHbS3A3FlpC1/nIYgiSMdHFfBCeVayS//YzQTOGz0bEOvOHXV5kB65JEl093H+O0tIz637wW4Uw3vgrEIrSbAHG4v5snhD0Fq3N+es20GflVfbnRSJO3aV5exLSq9TqGXav0mH1lQ9FkeDUbzO6DItiGtQY1h5c6goSR+kDWGo3p95EaJFAIXQgQZFHlT5zDPaJg==" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="LX">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="ORD" DepartureDate="2019-10-16T14:45:00" ArrivalDate="2019-10-16T16:47:00" OperatingAirline="UA" MarquetingAirline="LX" FlightNumber="3291" JourneyDuration="P0DT18H5M0S" Class="C" Cabin="C" AirplaneType="739" FareBasis="CNY00EFF" />
                                    <Segment DepartureAirport="ORD" ArrivalAirport="ZRH" DepartureDate="2019-10-16T19:10:00" ArrivalDate="2019-10-17T10:30:00" OperatingAirline="LX" MarquetingAirline="LX" FlightNumber="9" JourneyDuration="P0DT18H5M0S" Class="C" Cabin="C" AirplaneType="77W" FareBasis="CNY00EFF" />
                                    <Segment DepartureAirport="ZRH" ArrivalAirport="MAD" DepartureDate="2019-10-17T12:25:00" ArrivalDate="2019-10-17T14:50:00" OperatingAirline="LX" MarquetingAirline="LX" FlightNumber="2026" JourneyDuration="P0DT18H5M0S" Class="C" Cabin="C" AirplaneType="CS3" FareBasis="CNY00EFF" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="USD">
                                <TotalFixAmounts Gross="15016.74" Nett="15016.74">
                                    <Service Amount="13704.64" />
                                    <ServiceTaxes Included="false" Amount="1312.1" />
                                </TotalFixAmounts>
                                <Breakdown>
                                    <Concepts>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="6852.32" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="6852.32" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                            </Items>
                                        </Concept>
                                    </Concepts>
                                    <Taxes>
                                        <Tax Name="Tasas Others" Value="656.05" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13704.64" Amount="656.05" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13704.64" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13704.64" Amount="0" />
                                        </Tax>
                                        <Tax Name="Tasas Others" Value="656.05" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13704.64" Amount="656.05" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13704.64" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13704.64" Amount="0" />
                                        </Tax>
                                    </Taxes>
                                </Breakdown>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-01</Rule>
                        </Rules>
                    </FlightResult>
                    <FlightResult FareType="PUB" AvailableSeats="9" Number="30" Direction="Outbound" LowCost="false" RatePlanCode="lZmAomcqR8KeVwNrCaYbm7YYwekKD4434aJbEwrpVfyzE48fargROzff5Ej7JNfS8whG8hnyLlfBBSUQFzfCB3HraFOldE7NH1OzAjTVW7gF+S9iJIdFyjcNNlplEnT7xizjBe4M8X2DiObSVZSDRJPiMQlqidyznpR2lU3ZYrn8i4+xBwPVLwl9to1xkWJz7FzVLZV4kaMlaiWxTP8q9Dof0f4vYdhO8hG8Hjx+ET9WZB3AIe+uHZ/GEAELPmTEKa4i7UFPJnoCDnr0ZnLqWskfWNM9gIrX0xdzPC8zEzAeXYAuOJ0vn+PEGE4mAQXGOT18aLNthkLWJ8ow0w5sBx/I7rfDOTz6lXqEUHDyGdz/K8AzlAavCxYgpUy1f7P6vxS5fgKWpigvDegM9MDh2/SykG8A2Bovd8o7f5pyn6dmRkx8x8uakmTFF7AGl5Y5nKrdj13YwuTuuyvsa+JO949CBntXWaA1CREzO+M1RZZRyk64Q3F7hnOyB6uM3YWRIR1Isj8kCQYOc77k234A6jCQ1iCASovKG+EAXEdI2+Zn7Zq53i67pJNx1ZkqMcZvovpp7HxfYTNR2yLshhWRAnWi74BXQnwJEEv0Qyc92rxj1yhSA69U/6acOjUpWrTVolgPILbASOSUKTGytniT9oiYl/gKRQkNc0L2gwgHaJ2+AxbnoYM8f+HRYsj1im0DJvvJ0FMNcOT1UTASZLCE5yLtphJEkSsxZ07ywaeGpc7nlwbF6Eb4J7zHnzyY2zAAyVXuVgIY1wCVP8VQdib68LRgpktj1UkAMMCDL2QMFev1jGuXU+AwryMubirP0qoXs23Y+IRkS3EiuhMLRsN92nPfIkmrCQnAJOhHb0Oj6qfHYVvtn4ehN0xsalXUlARvcKfW84YQm2IHIddqb6LpQvN+b4SeKMtfpnYT/+h0bk2M0oXVwEtj7XAkvmdis1GimeLdOEcRQO3+4HqK0mhElliFjARB2q9naXSq4QdP+0rqL0RCsixbShYO51GKpc5z5/MqLDUoX25HMVAan1Urh1KbQGNKpCUox7jEAhhTbLf8dDOcvsV2G6XtUPBF+5Cv81ZVpi0PhncPPnXgw9zym4AVKxZkYFr2jNdmrgfxGbWb12gID79nrcyUCEPs7Gp4XFtzyvtUTpvXdAYY3jiufodrG4iW9Kq51K9anPMHKQvXIbBrpIgivqFUvsGcdljWyy5P2gRkAqIuD2KTN6HLe4Wu+jxhkInZmrO2ZuGG1vXEDkYGwI2w6f3UrvalGyHXLBry+GbEIb0oNrWDA1bwhKYxM2Fv+fXjATeCS8A+YspzEERXzZsVGMAZF47Az7MYSdItxEIN9NZzHmuTfiwTIw==" Status="OK" Source="Amad">
                        <Routes ValidatingCarrier="UA">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="FRA" DepartureDate="2019-10-16T19:59:00" ArrivalDate="2019-10-17T10:55:00" OperatingAirline="LH" MarquetingAirline="UA" FlightNumber="9054" JourneyDuration="P0DT13H41M0S" Class="C" Cabin="C" AirplaneType="744" FareBasis="CNY00EFF" />
                                    <Segment DepartureAirport="FRA" ArrivalAirport="MAD" DepartureDate="2019-10-17T13:10:00" ArrivalDate="2019-10-17T15:40:00" OperatingAirline="LH" MarquetingAirline="UA" FlightNumber="9229" JourneyDuration="P0DT13H41M0S" Class="C" Cabin="C" AirplaneType="32A" FareBasis="CNY00EFF" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="USD">
                                <TotalFixAmounts Gross="15018.5" Nett="15018.5">
                                    <Service Amount="13704.64" />
                                    <ServiceTaxes Included="false" Amount="1313.86" />
                                </TotalFixAmounts>
                                <Breakdown>
                                    <Concepts>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="6852.32" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="6852.32" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                            </Items>
                                        </Concept>
                                    </Concepts>
                                    <Taxes>
                                        <Tax Name="Tasas Others" Value="656.93" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13704.64" Amount="656.93" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13704.64" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>200</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13704.64" Amount="0" />
                                        </Tax>
                                        <Tax Name="Tasas Others" Value="656.93" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13704.64" Amount="656.93" />
                                        </Tax>
                                        <Tax Name="ServiceFee" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13704.64" Amount="0" />
                                        </Tax>
                                        <Tax Name="ServiceFeeIVA" Value="0" IsFix="true" ByNight="false" Commissionable="false" Included="false">
                                            <TtaCodes>
                                                <TtaCode>201</TtaCode>
                                            </TtaCodes>
                                            <Total Base="13704.64" Amount="0" />
                                        </Tax>
                                    </Taxes>
                                </Breakdown>
                            </Price>
                        </Prices>
                        <AdditionalElements>
                            <Bags>
                                <Bag BaggageType="holdBaggage" Quantity="2" />
                            </Bags>
                        </AdditionalElements>
                        <Rules>
                            <Rule Name="LastTicketDate">2019-08-01</Rule>
                        </Rules>
                    </FlightResult>
                </Results>
            </AvailabilityRS>
        </FlightAvailResponse>
    </soap:Body>
</soap:Envelope>
```