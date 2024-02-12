## Total Discharges 
                        Total Discharges = COUNTROWS(hospital_discharges)
Counts the total number of hospital discharges.

## Total Hospitals
                        Total Hospitals = DISTINCTCOUNT(hospital_discharges[facility_id])
Counts the total number of distinct hospitals represented in the dataset.

## Average Cost per Discharge
                        Average Cost Per Discharge = DIVIDE(SUM(hospital_discharges[total_costs]),[Total Discharges])
Computes the average cost per discharge by dividing the total costs of hospital discharges by the total number of discharges.

## Average LOS Days
                        Average LOS Days = AVERAGE(hospital_discharges[length_of_stay])
Computes the average length of stay (LOS) days for patients across all facilities.

## % Var Average Cost per Discharge
                        % Var Average Cost per Discharge = 
                                                          DIVIDE(
                                                              ([Average Cost Per Discharge]-[Average Cost per Discharge ALL]),
                                                              [Average Cost per Discharge ALL]
                                                          )
Calculates the percentage variation in the average cost per discharge compared to the overall average cost per discharge across all facilities.

## % Var Average LOS Days
                        % Var Average LOS Days = 
                                                DIVIDE(
                                                    ([Average LOS Days]-[Average LOS Days ALL]),
                                                    [Average LOS Days ALL]
                                                )
Calculates the percentage variation in the average length of stay (LOS) days compared to the overall average LOS days across all facilities.
                  
