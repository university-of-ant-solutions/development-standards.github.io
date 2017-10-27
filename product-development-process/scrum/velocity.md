---
description: Velocity
keywords: velocity, scrum, product, development, process
title: Velocity
---

## Definition of Velocity

The velocity of a team is a measure of how much work that the team can handle within a specific time period, i.e. how much of the product backlog can be completed by the team in a sprint. Velocity can be calculated on the basis of story points, business value, hours, issue count, or any numeric field of your choice

![pivotaltracker analytics](/product-development-process/images/pivotaltracker-analytics.png){: width="60%"}

## The velocity calculation formula

```
velocity_per_week(iteration_1, ..., iteration_N) =
    SUM(iteration_i.points / iteration.team_strength) /
    SUM(iteration.length_in_weeks)
```

For example, if your iterations are two weeks long by default, Tracker will multiply the per-week velocity by 2.

> Ví dụ, nếu như vòng lặp của bạn độ dài mặc định là 2 tuần, velocity sẽ được tính là tổng số points 2 tuần / team_strength / 2 (số tuần)

## Reflecting accurate capability with Team Strength
Iteration Team Strength allows you to tell Tracker about variations in your team from iteration to iteration. This helps you account for things like holidays, sickness, or other temporary team fluctuations.

For example, if half of your team leaves for a conference during one iteration, you might set the team strength of that iteration to 50%. Likewise, if your team works all weekend to prepare for launching your product, you would set the team strength to 140% (since they worked seven days instead of a normal five-day work week).

## Resources

* [Wiki](https://en.wikipedia.org/wiki/Velocity_(software_development)
* [Understanding velocity](https://www.pivotaltracker.com/help/articles/understanding_velocity/)
* [Planning with velocity](https://www.pivotaltracker.com/help/articles/planning_with_velocity/)
