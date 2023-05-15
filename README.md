<!-- Overview of the analysis: Explain the purpose of this analysis. -->
identify get the tempretures of months 

<!-- Results: Provide a bulleted list with three major points from the two analysis deliverables. Use images as support where needed. -->
there is no much of a defference in mean of tempretures of each month
there is no much of a defference in max of tempretures of each month

<!-- Summary: Provide a high-level summary of the results and two additional queries that you would perform to gather more weather data for June and December -->
result = session.query(Measurement).with_entities(
    Measurement.prcb
).filter(Measurement.date.like('%-06-%')).all()
result

result = session.query(Station).with_entities(
    Station.elevation
).filter(Measurement.date.like('%-06-%')).all()
result

