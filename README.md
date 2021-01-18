# Citizen Browser - Political Group Recommendations
This repository contains code to reproduce the findings featured in our story, "[Facebook Said It Would Stop Pushing Users to Join Partisan Political Groups. It Didn’t.](https://themarkup.org/citizen-browser/2021/01/19/facebook-said-it-would-stop-pushing-users-to-join-partisan-political-groups-it-didnt)" from our series, [Citizen Browser](https://themarkup.org/citizen-browser/).

Our methodology is described in "[How We Built a Facebook Inspector](https://themarkup.org/citizen-browser/2021/01/05/how-we-built-a-facebook-inspector)".

## data/
The `data/` directory contains several spreadsheets.

`top_100_groups.csv` contains the top 100 groups recommended to our 1,917 panelists in December 2020.<br>
`top_groups_political.csv` contains the subset of 11 political groups from the top 100 recommended groups.

We also have the same spreadsheets for Biden (N=1,214), Trump (N=508) and non-voters (N=155).<br>
`top_100_groups_{X}_voters.csv` contains the top 100 groups recommended to X-voters in December 2020.<br>
`top_groups_political_{X}_voters.csv` contains the subset of political groups from the top 100 recommended groups for X-voters.

Each of these spreadsheets in formatted similarly, containing some subset of the following columns.


| column                     | description                                                                                                      |
|:---------------------------|:------------------------------------------------------------------------------------------------------------|
| rank                       | The index of each csv file is the rank of how many panelists were recommended the Facebook Group                 |
| group_name                 | The name of the Facebook Group                                                                                   |
| n_user_recommend           | The number of panelists who were recommended this Facebook Group                                                 |
| n_user_timeline            | The number of  panelists who were broadcast this group on their timeline in December 2020                       |
| posts_per_day              | The max number of daily posts by the Facebook Group                                                              |
| n_members                  | The max number of members in the Facebook Group                                                                  |
| n_user_recommend_by_friend | The number of users (subset of `n_user_recommend`) who had a mutual friend in the Facebook Group                 |
| n_panelists                | The number of panelists in this bucket of users                                                                  |
| %_user_recommend           | `n_user_recommend` / `n_panelists`                                                                               |
| is_political               | Whether or not the Facebook Group was determined to be political based on the name, rules, and discussion. |
| political_lean             | The political orientation (L or R) of the Facebook Group based on the name, rules, and discussion.                  |
| group_slug                 | The unique identifier for the group. `https://facebook.com/groups/{group_slug}`                                  |

## Licensing
Copyright 2021, The Markup News Inc.

Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:

1. Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.

2. Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.

3. Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
