# Data Engineering Zoomcamp - Homework 02

## Assignment

For the assignment to extend the existing flows for the 2021 year, I have used [this yaml flow file](./extended_scheduled_flow.yaml) which is an extension to the existing 06_gsc_scheduled_flow.yaml file. The new flow file as discussed during the lecture, removes all the unnecessary tables created during the entire process. I used backfills to run the flow for the 2021 year.

## Quiz

### Question 1
Ans: `128.3 MB`


### Question 2
Ans: `green_tripdata_2020-04.csv`


### Question 3
Process: `SELECT COUNT(*) FROM 'datatalks-de-zoomcamp-447709.zoomcamp.green_tripdata'`;

Ans: `24,648,499`


### Question 4
Process: `SELECT COUNT(*) FROM zoomcamp.yellow_tripdata;`

Ans: `1,734,051`


### Question 5
Process: `SELECT COUNT(*) FROM zoomcamp.yellow_tripdata WHERE filename = "yellow_tripdata_2021-03.csv"`;

Ans: `1,925,152`


### Question 6
Process:
```yaml
# Reference: https://kestra.io/docs/workflow-components/triggers/schedule-trigger
triggers:
  - id: daily
    type: io.kestra.plugin.core.trigger.Schedule
    cron: "@daily"
    timezone: America/New_York
```

Ans: `Add a timezone property set to America/New_York in the Schedule trigger configuration`
