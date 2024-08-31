---
layout: page
title: Schedule
permalink: /schedule/
---
  <div class="posts">
    <div class="table-container">
        <table>
            <thead>
                <tr>
                    <th>Date & Time</th>
                    <th>Opponent</th>
                    <th>Location</th>
                </tr>
                <tbody>
                    {% for game in site.games %}
                    <tr>
                      <td>{{ game.date | date: "%B %d, %-I:%M %p" }}</td>
                      <td>{{ game.opponent }}</td>
                      <td>{{ game.location }}</td>
                    </tr>
                    {% endfor %}
                </tbody>
            </thead>
        </table>
    </div>
   </div>