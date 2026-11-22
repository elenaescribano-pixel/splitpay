# SplitPay

A shared-expenses app for students who share a flat. Theme: **shared household**.

Splitwise tells you who owes whom. SplitPay also splits bills by the days each member actually lived in the flat, supports splits by item or by income, keeps a shared pot that predicts when it will run out, and builds a payment plan with due dates.

## Problem

Students who share a flat or travel together split rent, bills, groceries and trips informally, in chat threads and spreadsheets. Mid-month move-ins and move-outs, uneven incomes and shared purchases make "who owes whom" hard to agree on, and arguments about money follow.

## Target users

Flatmates, couples and small groups of friends who share recurring household costs, such as students at IE.

## Goals

- Record members and the days each one actually lived in the flat.
- Split expenses equally, by percentage, by item or by income.
- Split recurring bills (rent, electricity, water, internet) in proportion to days present.
- Keep a shared pot and predict when it will run out.
- Track budgets per category and month, with pace alerts.
- Produce a payment plan with the minimum number of transfers, due dates and overdue payments.

## Scope

In scope: one API, one database and one web frontend covering the six modules below, deployed on Azure.
Out of scope for now: real payments between members, bank integrations and mobile apps.

## Team

| Member | GitHub | Module | Main entity | Calculated result | Shared job |
|---|---|---|---|---|---|
| Lorena Marie Selman López | @lorenaselman | Members (users) | Member | Days each member stayed per month | Continuous integration |
| María Elena Escribano Arranz | @elenaescribano-pixel | Expenses | Expense | Each member's share of every expense | Documentation and board |
| Mads Myklebust Frafjord | @madsarne8-sketch | Bills | Bill | Each member's share prorated by days | Cloud deployment |
| Luis Felipe Christopher Haubold Giménez | @felipehau | Pot | Pot movement | Balance and predicted date it runs out | Database |
| Juan Patarroyo Rodríguez | @jcpatarroyor | Budgets | Budget | % spent, pace and forecast | Frontend shell and dashboard |
| Alejandro Jiménez Gómez | @alejimenezg99 | Settlements | Settlement | Minimum transfers and overdue payments | Containers and configuration |

## Cross-module feature
Settlements uses Expenses, Bills and Pot to calculate who owes whom, and the dashboard combines all modules.

## Conventions
To be agreed for Milestone 2.
