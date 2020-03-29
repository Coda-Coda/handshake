# How to generate a simple visualisation of Handshake data

Here's how to generate an up to date version of: https://graphcommons.com/graphs/a150a176-fd30-4830-a5df-a1c655bd8185

Similar to:

![Image of Handshake Connections as at 5:40pm 22nd March 2020](Visualisation&#32;at&#32;2020-03-22&#32;at&#32;5.42&#32;PM.png)

1. Go to https://graphcommons.com/ and sign in
2. Click "Start a graph" or go to https://graphcommons.com/graphs/new
3. After the tutorial, or skipping it, click "Import" on the left hand panel
4. Paste in the following link under "Import Edges": https://docs.google.com/spreadsheets/d/10y7cufEh8_1pYc0X4VwJ-5uBc5ztbrQABjTVg9BF_ag/edit?usp=sharing (leave "Import nodes" blank)
5. Click "Continue"
6. Click "Save"
7. Name your graph and choose any option, then click "Save"
8. Consider changing the node type colours to red for Confirmed, yellow for Suspected, green for Healthy, grey for Unreported and blue for locations. (see https://vimeo.com/125936064)
9. Done!

You've generated a graph with the latest data from what has been reported on the Handshake forms.

Feel free to [make a copy of the Google Sheet that helps implement this](https://docs.google.com/spreadsheets/d/10y7cufEh8_1pYc0X4VwJ-5uBc5ztbrQABjTVg9BF_ag/copy).

It currently includes only the first 8 characters of the unique id, for readability. This could be changed by altering the value in the Variables sheet after [making a copy](https://docs.google.com/spreadsheets/d/10y7cufEh8_1pYc0X4VwJ-5uBc5ztbrQABjTVg9BF_ag/copy).

You may also be interested in trying out a [very simple Google Sheet Handshake Checker](https://docs.google.com/spreadsheets/d/19uqjzeGC0XvTuJnZVDC6QBUW_lNB_MtgqZVO_JdUlsQ/copy). Make a copy by clicking the link then enter your ID e.g. "Person_57136aa8". It will show you whether any people up to 3 degrees away from you on Handshake have reported as Confirmed. It uses up to date data.
