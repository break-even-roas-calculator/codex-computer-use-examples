# Prompt templates for @Computer

Each prompt names one app or flow and ends with a boundary sentence.
The first two are quoted from Jason Liu's article; the rest follow the same shape.

## Native app (sourced)

Use @Computer to open Spotify, find my Discover Weekly playlist, and start it.
Do not change my account or subscription settings.

## iOS flow via iPhone Mirroring (sourced)

Use @Computer to open iPhone Mirroring, reproduce the onboarding bug in the
iOS app, and take a screenshot of the failing state. Fix the smallest relevant
code path, then run the same flow again.

## Slow polling task

Use @Computer to watch the open support chat window. Check it every five
minutes; once a human agent joins, check every minute and answer their
questions from the order details in this thread. Do not agree to any charge
or account change; if one is proposed, stop and tell me.

## System settings

Use @Computer to open System Settings and turn on the setting I describe
below, then take a screenshot of the final state. Change nothing else and
stop if a password or security prompt appears.

## Last-mile step in a structured workflow

The Slack plugin already posted the message in the channel. Use @Computer
only to click Add file in that thread and attach the rendered video from the
project folder. Do not send any other message.
