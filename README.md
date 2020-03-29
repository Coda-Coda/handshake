![Image of Handshake - Track your proximity to Covid-19.](docs/title.png)

I've had this idea for a website (or app) that could help, perhaps just a little, to control the spread of Covid-19. I'm calling it Handshake for now.

To try it out visit: https://coda-coda.github.io/handshake/Generator/

For an overview of the Handshake _idea_ see: https://coda-coda.github.io/handshake/

This repository is the location of a basic working version of Handshake, described below.

# Brief overview:
 - When 2 people meet, one person goes to [Handshake Generator](https://coda-coda.github.io/handshake/Generator/) and generates a Handshake QR code by entering their email address and Handshake password (or alternatively just a unique phrase).
 - Alternatively, [locations can generate their own QR code](https://coda-coda.github.io/handshake/locations/Generator/) which can be displayed and then be scanned by people visiting.
 - The other person scans this QR code which takes them to [Handshake Reader](https://coda-coda.github.io/handshake/Reader) they also enter their email address and Handshake password (or just a unique phrase).
 - They then are redirected (or can click the link) which takes them to a pre-filled Google Form which they simply submit (no need to log in).
 - The publicly accessible [Google Spreadsheet](https://docs.google.com/spreadsheets/d/11LaeMly8CQdM7R7MsvE2GSdWZLySA4hNaQ9GrBg53TE/edit?usp=sharing) then has a record of this interaction (recording the date/time and the SHA256 hashes of the two people's email addresses concatenated with their Handshake password - or just the hash of their unique phrase)
 - People can report their status, e.g. healthy, suspected, or confirmed to Handshake by filling out [this form](https://forms.gle/DWQRNfaeBrwB3oD58), the responses are available publicly [here](https://docs.google.com/spreadsheets/d/1hcjN_L62VK7hPSIKkfc0YRdFE8ULYG-ebpGgSw3kxgc/edit?usp=sharing)
 
 - Handshake data can then used by anybody for purposes related to stopping the spread of Covid-19. For example, when someone is reported as having confirmed Covid-19, the data from Handshakes can be used to warn those who might have been exposed while the person was contagious to be careful (due to the current setup this would require people to regularly check a Handshake page that has not yet been created to check their risk, or it could be implemented so that the check could also happen automatically whenever they next Handshake).

# Further details

For further thoughts on this Handshake implementation see: [this pdf](https://coda-coda.github.io/handshake/Documents/Handshake-Implementation.pdf). It includes a few comments about design choices, privacy, and other thoughts.

To view all the Google Docs/Forms/Spreadsheets associated with this Handshake project go to: [this link](https://drive.google.com/drive/folders/1QyTqI0OCHrU2mA-SdoL0u5QEfasWZZ8h?usp=sharing)

# Visualisation

There's a [visualisation of the recorded connections](https://graphcommons.com/graphs/a150a176-fd30-4830-a5df-a1c655bd8185). Note that this needs to be manually refreshed by me so may be out of date. To generate an up to date version yourself see [these instructions](docs/Generate_Visualisation.md). For readability it only shows the first 8 characters of the hashes/unique IDs. 

Here is what it looked like at 3pm on the 29th of March 2020:

![Image of Handshake Connections as at 3pm on the 29th of March 2020](docs/Visualisation&#32;at&#32;2020-03-29&#32;at&#32;2.57&#32;PM.png)

In this image, green denotes a person reporting as healthy (and never as sick or suspected), blue denotes the locations, and grey denotes people that have never reported their health status on Handshake but have used Handshake to connect with someone.

For a description on how to use the visualisation see: [this link](https://coda-coda.github.io/handshake/Checker/)

# Want to get involved or have feedback?

[Report an issue on GitHub (publicly)](https://github.com/Coda-Coda/handshake/-/issues/new)

[Get involved on GitHub](https://github.com/Coda-Coda/handshake/issues)

[Send an email to get.involved.handshake@gmail.com](mailto:get.involved.handshake@gmail.com)

# Please take this idea and make it better - I am not in a position to do so
Lastly: please feel free to take this idea and make it better :)
