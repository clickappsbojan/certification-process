### Request
```xml
<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope" xmlns="http://www.juniper.es/webservice/2007/">
    <soap:Header/>
    <soap:Body>
        <FlightAvail>
            <FlightAvailRQ Version="1.1" Language="en">
                <Login Password="xxxxxxxxx" Email="xxxxxxx"/>
               
                <Paxes>
               	   
               	    <Pax IdPax="1">
               	    	<Age>28</Age>
               	    </Pax>
               	    
               	    <Pax IdPax="2">
               	    	<Age>28</Age>
               	    </Pax>
               	    
               	    <Pax IdPax="3">
               	    	<Age>5</Age>
               	    </Pax>
               	</Paxes>
                
                <FlightRequest>
                    <SearchSegmentsFlight>
                        <SearchSegmentFlight>
                            
                            <CountryOfResidence>SA</CountryOfResidence>
                            <Routes>
                                <Route Origin="39681" Destination="37786" Date="2019-10-16"/>
                                <Route Origin="37786" Destination="39681" Date="2019-10-16"/>
                            </Routes>
                        </SearchSegmentFlight>
                    </SearchSegmentsFlight>
                    <RelPaxesDist>
                        <RelPaxDist>
                            <RelPaxes>
                                <RelPax IdPax="1"/>
                                <RelPax IdPax="2"/>
                                <RelPax IdPax="3"/>
                            </RelPaxes>
                        </RelPaxDist>
                    </RelPaxesDist>
                </FlightRequest>
                <AdvancedOptions>
                    <ShowBreakdownPrice>true</ShowBreakdownPrice>
                    <UseCurrency>USD</UseCurrency>
                </AdvancedOptions>
            </FlightAvailRQ>
        </FlightAvail>
    </soap:Body>
</soap:Envelope>
```

----
----
----

### Response

```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <soap:Body>
        <FlightAvailResponse xmlns="http://www.juniper.es/webservice/2007/">
            <AvailabilityRS Url="http://xml-uat.bookingengine.es" TimeStamp="2019-07-28T13:53:42.0599487+02:00" IntCode="GJoNof2rTYMCLw0JtENsGG0RgArOGr88tZ0To1nD+qU=">
                <Results>
                    <FlightResult FareType="CHA" AvailableSeats="18" Number="1" Direction="Inbound" LowCost="false" RatePlanCode="LF6j9ndyo/zlz9tkRLu5T4vcqg4Y3XWeGauWGUmxxJy33kAWihQpwFONCEgQgZ8jh2qgNLr3UUIh1pN4HhPScroL38KdGk2VoMaAFRpQ2UW05L1/XEaDj1FmG9l9D/hwKSuyhNJ2T0O0HcLz9ifhf0hdoihQthapHvHg5Zds3vtrEmgY/FNIUr+8F65VS2G2ZfVjGq5Cq6GcwROErkp1QmmV16nDR/1W70yzcWwKKS3OFyo7okugrkFLVkH5rN04EYLrcBcAJMDzaqJ5nE3BX7VRAukKTGniHJCcyGu/Nt10eJEjlmgLAOl/uPAe6FTfl6TIkxa1/M+M2uEaSb25zysKmKeTu8u/n8etfKy140Vv8ThRbObss7oozn0sqlhJ+1Hco+vwLKB00y6XyTVacTq+yn9RTNcgjVSHduJjFiLUE2COBVZ3FtwXBjfunKqam6cjcFiKCvAY74ffQ+t30+el8zmO4fdhNGeGFexKTkoaWk9Q9m+FTYPF5jWsImmH0mkPijtSeXXEaDsB6g4I7f+y3uE4i+PgnvHPzyl6UPddn0AbOuoJ1/8/LviVAgKpfuGR9mnnSAj7fA7H4RQxazphHaVjNO8Oy/G9qGZFMSlu3Igei8275GrsB3rQtWS9hhXwt87/wyBKXrXmsIDgym6VLuXWSgD1S6OrpRaVjwABA4CQczq8fowOGhmpXrzwxK10h12oRh8c3Gozg2Au01e96pXDizVlscsCu/lAtp5Sw2+XpMS108vj+iDHKSyOBqjkH516VzqNiEeshLCPxq5xyHJAasEY+l198aPG4HiC8aUjgNf2lNFC1mOedjykDDVoKOWm8pkgJ8+Ehzv6+kpZxi052oyNmaPKA5AlRxcYvYZHVe2CCUOxm6EZ8BvKdHQLUtE/RM5OlYDmM67q4m724JKHeBqAhurML5XVMBJDsozgq4MgvnbmV/Cle8jcbGh+BAsFE22bITKxQdzBMvBkU0z2I8rG+Tg1Qdg0+2g=" Status="OK" Source="ChV2">
                        <Routes ValidatingCarrier="EI">
                            <Route Origin="37786" Destination="39681">
                                <Segments>
                                    <Segment DepartureAirport="MAD" ArrivalAirport="MCO" DepartureDate="2019-10-16T10:00:00" ArrivalDate="2019-10-16T17:00:00" OperatingAirline="EI" MarquetingAirline="EI" FlightNumber="1234" JourneyDuration="P0DT7H0M0S" GroundDuration="P0DT7H0M0S" Class="B" Cabin="Y" FareBasis="200" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="USD">
                                <TotalFixAmounts Gross="115.78" Nett="115.78">
                                    <Service Amount="115.78" />
                                </TotalFixAmounts>
                                <Breakdown>
                                    <Concepts>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="52.63" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="52.63" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="10.52" Date="0001-01-01" Quantity="1" Days="1" PaxType="CNN" TtaCode="302" />
                                            </Items>
                                        </Concept>
                                    </Concepts>
                                </Breakdown>
                            </Price>
                        </Prices>
                    </FlightResult>
                    <FlightResult FareType="CHA" AvailableSeats="10" Number="2" Direction="Inbound" LowCost="false" RatePlanCode="LF6j9ndyo/zlz9tkRLu5T4vcqg4Y3XWeGauWGUmxxJy33kAWihQpwFONCEgQgZ8jha1LDJevHlAGRLYYg+22TUknevGUpCpto7S5CZ+pjWeWlH4E7kz3ANGe4ZMpMgcNfaKWwFWG4aCUswCwKLR4LMjTBIbi8l3G5lWJbLtAGNn6Nii5XBWuIAArZgF9KvvNmi9wxn3CMGa+/Qvq4/d9a1WJOyI5R6/CEr09z1AHpG/oV0yIu/n82zHQ+a9MR01UF/EippZXBRwp9c+Ucu8HQRCCz8kYfoP2Uozi1II0nAzPO3zKJSz/5/9pRFoedgD+C8cMpukUzeu1JW3fLI+k8+D+AOiuOHcmK1MloidQ0Kkr0vwUzFPECT0cHaMXirw0UZbEbuDz4k2guo8i1UDshbL8k3IrxbN0VB6DAqa2d5dl6U5VppDL0Y1goz5kyfJMaPnPx0PAUjwBBzWAtnpkgGMVL8luOnhqtsUdSdBQpXnunlJAG46OIXCd54ePnYM6LvW2hdEu7gs+M+614yDQLrFB+Cpurz+FwLeQU67Mg2g5h3R6yiXfiUWLTETdAIKBXFApRr+lnRWygNT42lhJqII7go1kt0yXfjSOGvr84rl5N6JyH7NqrmRuGtDu+tvh6Z8PtoF18KCM1br0emEeRzIeqcIvKGAbWADW9xr/6qRJHma0kWt2LvZHdy4XngXwSS6SKEo1Abhb/aJj/7TMAZaAqg5kqXqoo7uh3dURwD/QThiOZjopNqEd6cw8CGQEFL8UIaNogkXn05lXLwg7d+sY6xBBS3zZlMNQDYTT5hIRzoO4rkOlbxgyD1JYh/H8GJZd1pcsMOYaGT9eVufJkFzXGGhYUPacGJo6vZ9sGsRCvMYjANgY1blEGCyWBS22vXajjTVKeBilpu1Stry+EVPqKIz9N6CVTGErZa9dU4J40lQ+IDKkZ7c1cd7IO637DZfcnpb0q3TPqMzwFW/SLi1Mz8zgiV39fAIXunlj1cs=" Status="OK" Source="ChV2">
                        <Routes ValidatingCarrier="EI">
                            <Route Origin="37786" Destination="39681">
                                <Segments>
                                    <Segment DepartureAirport="MAD" ArrivalAirport="MCO" DepartureDate="2019-10-16T10:00:00" ArrivalDate="2019-10-16T17:00:00" OperatingAirline="EI" MarquetingAirline="EI" FlightNumber="1234" JourneyDuration="P0DT7H0M0S" GroundDuration="P0DT7H0M0S" Class="A" Cabin="F" FareBasis="300" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="USD">
                                <TotalFixAmounts Gross="231.57" Nett="231.57">
                                    <Service Amount="231.57" />
                                </TotalFixAmounts>
                                <Breakdown>
                                    <Concepts>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="105.26" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="105.26" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="21.05" Date="0001-01-01" Quantity="1" Days="1" PaxType="CNN" TtaCode="302" />
                                            </Items>
                                        </Concept>
                                    </Concepts>
                                </Breakdown>
                            </Price>
                        </Prices>
                    </FlightResult>
                    <FlightResult FareType="CHA" AvailableSeats="95" Number="3" Direction="Outbound" LowCost="false" RatePlanCode="7Vor0/GRKZ31Va+BuE1WMFvq/9heAul4psoTS3hesB97bKcS8vVV8I7otP/319flLlmLEjZ/RA1OgALYkI4zwhRMYiJGGBG09ebHNn25IThn3xtSgBx3O80ZAA03A9dJlLWnm/Sgm511lz+tCHdxlyPcDK6T0I7D6PDQg9nG/3GObEpB2zUA4FmB6nHIYVR6NFL76tLltPQshNNcrbn2wHXZQZqlAxkKuzlCH4+4LJgDqt+QfVGwvcw0yPt4n6RMxUXJHkm+ki/kxkuZyTVkjBRCYUnuUOYV6Szo5HBi3JSZ137QRhBH1CwvBLU9/tlLNrQhxBilDBSNhx2vC5PGLM3cg0YcDueTMCb2Of1fvztajX1YYMLvceGTL9195WENv79MCskcN6Zms58yPeD2KJT98HRYGydzHkbRxF2955PaZHegtbIUnRaS+GQWX94iipFkguq7Imz0fIkmAd9+3FPFuF+YjU71ZaQLvvxXO8q9KxZQM62G4tjbvdvdSWD/X0SM2vRp2o7my2KAB1wceirYHpVwCXP1xP/AT+wI1HTtCt/0QD7ly+zQs56zymMjecdIeWdcMzz9EFs8vOOoqGM3bFwxdkoIJrD2z1TFNuXjRK3UUMnMwXOECfF5PX3DkWqazSiGhIXzCM/ruEi8qx45DqpZo5MAKVm6e9kCTsFXgVnPMzWtik7O7IOBMERx4An3xHU8PgLOdWaKZC2E1nDO0nbd+1GFG9BmDeNtHGVvcYvNoO6aTzjcAblkYuKASy+TBiQeB8Bj3lgL5Q1ouvlb+JvYVExVdcrwOqQcKe8xL8t7vLM7ZJlGQiTjAc0/cBGKCVS45TMz4WlFyX6gWr+vO7OG39gH44Uf0+VnYozpmvkCh8voBAA/EoqnAHmHUtxEHaJLG7Kwed6RE6Hdl/aUdomp7MllokfqSFBRSpJERKfX+jh0WkDGnJ7Acx9pkg+cb9cV46cRXNW7aAVPPQ==" Status="OK" Source="ChV2">
                        <Routes ValidatingCarrier="EI">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="MAD" DepartureDate="2019-10-16T10:00:00" ArrivalDate="2019-10-16T20:00:00" OperatingAirline="EI" MarquetingAirline="EI" FlightNumber="1" JourneyDuration="P0DT8H0M0S" GroundDuration="P0DT8H0M0S" Class="FT" Cabin="F" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="USD">
                                <TotalFixAmounts Gross="611.1" Nett="611.1">
                                    <Service Amount="611.1" />
                                </TotalFixAmounts>
                                <Breakdown>
                                    <Concepts>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="222.22" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="200" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="222.22" Date="0001-01-01" Quantity="1" Days="1" PaxType="ADT" TtaCode="201" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="166.66" Date="0001-01-01" Quantity="1" Days="1" PaxType="CNN" TtaCode="302" />
                                            </Items>
                                        </Concept>
                                    </Concepts>
                                </Breakdown>
                            </Price>
                        </Prices>
                    </FlightResult>
                    <FlightResult FareType="CMB" Number="4" Direction="RoundTrip" LowCost="false" RatePlanCode="7Vor0/GRKZ31Va+BuE1WMFvq/9heAul4psoTS3hesB97bKcS8vVV8I7otP/319flLlmLEjZ/RA1OgALYkI4zwhRMYiJGGBG09ebHNn25IThn3xtSgBx3O80ZAA03A9dJlLWnm/Sgm511lz+tCHdxlyPcDK6T0I7D6PDQg9nG/3GObEpB2zUA4FmB6nHIYVR6NFL76tLltPQshNNcrbn2wHXZQZqlAxkKuzlCH4+4LJgDqt+QfVGwvcw0yPt4n6RMxUXJHkm+ki/kxkuZyTVkjBRCYUnuUOYV6Szo5HBi3JSZ137QRhBH1CwvBLU9/tlLNrQhxBilDBSNhx2vC5PGLM3cg0YcDueTMCb2Of1fvztajX1YYMLvceGTL9195WENv79MCskcN6Zms58yPeD2KJT98HRYGydzHkbRxF2955PaZHegtbIUnRaS+GQWX94iipFkguq7Imz0fIkmAd9+3FPFuF+YjU71ZaQLvvxXO8q9KxZQM62G4tjbvdvdSWD/X0SM2vRp2o7my2KAB1wcei/5OtACQjfssBiWK9mjOr5Y7ZeqVhNwyfFGYetQaLPpPQttuVkQijrEtTIIppIF9Ha5MDzKhZ0ezGfroDMcduE+AIxRMGqx3Y/qqr/wpKVUbpTV6m+r1SNc8OUv18SVVVA1NCr2KWEjTfUaYM9AWBRsdJObCvSEeg3qty82dUAZFkpvEx+hDljdArqxwHh8/v0D6/Z2j1WMQ7JZxcsb+7dOIJYmJTcrmpUvjMJ2ZACGHsag2tAqHSHlqEm3hm67qW3j3EDxbkktRIV/yswy7mKAXNHa1Wuv4mEfakDL+ZV9zJ/OK08j4yv6MOiLe30pqvdqIdY5ah8oH/ftXiMF5D5vYCVE3Nqckda7q7EbK6Wia/6iwAemBJ+Rykz3qyP3XaQ5CIR6TTzWqne5d+JzHONDxegCeggN4k/xLXHrUhuMxYXSP7Rzp3mzYRYQRcRpV6A2xy0vly8JgXyb7DJ8+DM6bddK6sqH64MQDjmhARVe8Uoceqffr7EQbKRPMsDKUbPXpz69spZBN5XeHN7pWfCvuwIxmC6DXj6HxNC4qas/Pbo67uzsyIe//3hhdiZPSa3K+UJ59Pfz3bxoJCHZUp/r5Eraie+xIcao1mdVl0Xb0XzfVwL9ORK3STY7BpalC1Ho50St4NDPb1rYbHmMskzLuIYYfjpKM2rdno7bZSe/qzYA9f7ARBjYLM/q/4hs7vAZk+IgEuoOUTBjbr4OVHRYGV7TvUNhuuSQ7zrrz2FsSkOJ04pbNvJ/XruqgBtMz0dZTN3aJL54ZJjyXFqeox+n03Fn3EhsBVvOv57aEuL+jJyZfDKUx3K0etPDIEvS044eOEzn591ajGvVByEyJLWulM1BVxhl49zGIBMyiBXQzEGr8SinfqI/eO+mxcDLO9j6VL6kqpVgOV2Drqx8iLe/H7nNDChpeUNcUb3e2+hkMmTx3qPtxoQEK57O5xjOnaMs/COQdKpZ9kHJh5FQxadYgBz2BwP0wpU0BKYjBfS03Hau2ydm6Htoa0UGn8pKHSyXSwVoOHGoJ9hPGHhah+ubjI3/WKxgEoDyPdnBf5KKSFNiktkgKQdHVgNvodVqEHAma3tmXEoSk3qhQZnk2VgdjU6l923w+n9wEgQkrGjF60OA82tvc7g9ShOSED38u4KZImggWBttO/pdGomqf7sKKmsZxOucJOca24Zet2iduIe/Dw1fCXJagT5QMQCR1nh6u6H9lxOFIEIX2VVvFF2pnxDUz59AdNRG03pIf2OqsInre51dFjvNCMbEo1UEX2FKAyg/SyzQuV6PiqSWXc75APMYZXPmppO1jebzsnvsnl+3HfTvjZl1LSzWjKmcu8x59Mpp02D6elMdMy25XC6f4kS2TzPjC1dOKlRrMvXaESocc/WlzZDBjyI7LqWudfU3Qy3ovE4OxeQYG3lEkJWFuwGtG8POsn/pCzqXtedT" Status="OK" Source="ChV2">
                        <Routes ValidatingCarrier="EI">
                            <Route Origin="39681" Destination="37786">
                                <Segments>
                                    <Segment DepartureAirport="MCO" ArrivalAirport="MAD" DepartureDate="2019-10-16T10:00:00" ArrivalDate="2019-10-16T20:00:00" OperatingAirline="EI" MarquetingAirline="EI" FlightNumber="1" JourneyDuration="P0DT8H0M0S" GroundDuration="P0DT8H0M0S" Class="FT" Cabin="F" />
                                </Segments>
                            </Route>
                            <Route Origin="37786" Destination="39681">
                                <Segments>
                                    <Segment DepartureAirport="MAD" ArrivalAirport="MCO" DepartureDate="2019-10-16T10:00:00" ArrivalDate="2019-10-16T17:00:00" OperatingAirline="EI" MarquetingAirline="EI" FlightNumber="1234" JourneyDuration="P0DT7H0M0S" GroundDuration="P0DT7H0M0S" Class="B" Cabin="Y" FareBasis="200" />
                                </Segments>
                            </Route>
                        </Routes>
                        <Prices>
                            <Price Type="S" Currency="USD">
                                <TotalFixAmounts Recommended="0" Gross="726.88" Nett="726.88">
                                    <Service Amount="726.88" />
                                </TotalFixAmounts>
                                <Breakdown>
                                    <Concepts>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="222.22" Quantity="1" PaxType="ADT" TtaCode="200" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="222.22" Quantity="1" PaxType="ADT" TtaCode="201" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="166.66" Quantity="1" PaxType="CNN" TtaCode="302" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="52.63" Quantity="1" PaxType="ADT" TtaCode="200" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="52.63" Quantity="1" PaxType="ADT" TtaCode="201" />
                                            </Items>
                                        </Concept>
                                        <Concept Type="BAS" Name="Base Coste">
                                            <Items>
                                                <Item Amount="10.52" Quantity="1" PaxType="CNN" TtaCode="302" />
                                            </Items>
                                        </Concept>
                                    </Concepts>
                                </Breakdown>
                            </Price>
                        </Prices>
                    </FlightResult>
                </Results>
            </AvailabilityRS>
        </FlightAvailResponse>
    </soap:Body>
</soap:Envelope>
```