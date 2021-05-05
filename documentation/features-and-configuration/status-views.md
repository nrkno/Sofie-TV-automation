# Status views

## System Status



{% hint style="warning" %}
Documentation for this feature is yet to be written.
{% endhint %}

System and devices statuses are displayed here.



{% hint style="info" %}
An API endpoint for the system status is also available under the URL `/health`
{% endhint %}

## Media Status

{% hint style="warning" %}
Documentation for this feature is yet to be written.
{% endhint %}

This page displays media transfer statuses.



## Message queue

{% hint style="warning" %}
Documentation for this feature is yet to be written.
{% endhint %}

Sofie Core can send messages to external systems \(such as metadata, as-run-logs\) while on air.

These messages are retained for a period of time, and can be reviewed in this list.

Messages that was not successfully sent can be inspected and re-sent here.



## User Log

The user activity log contains a list of the user-actions that users have previously done. This is used in troubleshooting issues on-air.

![](../../.gitbook/assets/image%20%2815%29.png)

### Columns, explained

#### Execution time

The execution time column displays **coreDuration** + **gatewayDuration** \(**timelineResolveDuration**\)":

* **coreDuration** : The time it took for Core to execute the command \(ie start-of-command 🠺 stored-result-into-database\)
*  **gatewayDuration** : The time it took for Playout Gateway to execute the timeline \(ie stored-result-into-database 🠺 timeline-resolved 🠺 callback-to-core\)
* **timelineResolveDuration**: The duration it took in TSR \(in Playout Gateway\) to resolve the timeline

Important to note is that **gatewayDuration** begins at the exact moment **coreDuration** ends.  
So **coreDuration + gatewayDuration** is the full time it took from beginning-of-user-action to the timeline-resolved \(plus a little extra for the final callback for reporting the measurement\).

#### Action

Describes what action the user did; e g pressed a key, clicked a button, or selected a meny item.

#### Method

The internal name in core of what function was called

#### Status

The result of the operation. "Success" or an error message.



## Evaluations

{% hint style="warning" %}
Documentation for this feature is yet to be written.
{% endhint %}

When a broadcast is done, users can input feedback about how the show went in an evaluation form.

The evaluations are listed here.

{% hint style="info" %}
Evaluations can be configured to be sent to Slack, by setting the "Slack webhook URL" under Settings/Studio
{% endhint %}



