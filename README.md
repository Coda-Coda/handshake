I've had this idea for a website (or app) that could help, perhaps just a little, to control the spread of Covid-19.
I'm calling it Handshake for now.

For an overview of the Handshake _idea_ see: https://coda-coda.gitlab.io/handshake/

This repository is the location of a bare-bones version of Handshake, described below.

# Brief overview:
 - When 2 people meet, one person goes to [Handshake Generator](https://coda-coda.gitlab.io/handshake/Generator/) and generates a Handshake QR code by entering their email address and optionally a privacy passphrase (or alternatively just a unique phrase).
 - The other person scans this QR code which takes them to [Handshake Reader](https://coda-coda.gitlab.io/handshake/Reader) they also enter their email address and privacy passphrase (or just a unique phrase).
 - They then are redirected (or can click the link) which takes them to a pre-filled Google Form which they simply submit (no need to log in).
 - The publicly accessible [Google Spreadsheet](https://docs.google.com/spreadsheets/d/11LaeMly8CQdM7R7MsvE2GSdWZLySA4hNaQ9GrBg53TE/edit?usp=sharing) then has a record of this interaction (recording the date/time and the SHA256 hashes of the two people's email addresses concatenated with their privacy passphrase - or just the hash of their unique phrase)
 - People can report their status, e.g. healthy, suspected, or confirmed to Handshake by filling out [this form](https://forms.gle/DWQRNfaeBrwB3oD58), the responses are available publicly [here](https://docs.google.com/spreadsheets/d/1hcjN_L62VK7hPSIKkfc0YRdFE8ULYG-ebpGgSw3kxgc/edit?usp=sharing)
 - These are the links to the [Generator](https://coda-coda.gitlab.io/handshake/handshake2/Generator/) and [Reader](https://coda-coda.gitlab.io/handshake/handshake2/Reader/) of handshake2, which uses a unique phrase instead of an email address and privacy passphrase. The two versions are compatible and use the same Google Forms and Spreadsheets.
 
 - Handshake data can then used by anybody for purposes related to stopping the spread of Covid-19. For example, when someone is reported as having confirmed Covid-19, the data from Handshakes can be used to warn those who might have been exposed while the person was contagious to be careful (due to the current setup this would require people to regularly check a Handshake page that has not yet been created to check their risk, or it could be implemented so that the check could also happen automatically whenever they next Handshake).


# Further thoughts:
 - As an overview of design choices: this basic implementation uses a hash of a user's email and a passphrase to aid privacy (or just a unique phrase), a centralised data store (Google Sheets), decentralised 'logins', is a webpage and uses only free tools.
 - This website/set up was simple to create, it wouldn't be too hard to create an improved version or for anyone with some resources to do so.
 - It does not rely upon users installing any apps, making it easily accessible.
 - It does not rely upon users sharing their location history.
 - It replaces the somewhat dangerous practice (in these times) of physically shaking hands.
 - Privacy is still an issue that would need to be tackled. Using a unique privacy passphrase and then hashing people's email addresses with it (or hashing a unique phrase) is possibly a bit helpful, but it does nothing to protect you from people you Handshake with that might want to reveal your identity. Plus, I'm not a cryptography or privacy expert so can give no guarantees around the privacy of this system whatsoever.
 - A privacy passphrase is added to the users email before hashing so that a person with a lot of email addresses can't just hash all the email addresses in their directory to match with publicly available data.
 - The alternate implementation [handshake2](https://coda-coda.gitlab.io/handshake/handshake2/) uses just a unique phrase that gets hashed and it is hoped that no two users come up with the identical unique phrase but it offers slightly more privacy as users don't need to volunteer their email address to the Handshake webpage. And it makes very clear that users _won't_ get email notifications (as in this particular implementation of the handshake idea, email notifications are not possible - though other implementations with different approaches to privacy could). To generate the same hash using Handshake2 a user with the email "test@test.com" and privacy passphrase "OneTwoThree" would use "test@test.comOneTwoThree" as their unique phrase.
 - This idea would still work if the information volunteered was stored privately rather than made publicly available. The onus would then be on the organisation that controlled the data to properly analyse it and make that analysis available to the people who it would be helpful for.
 - People do not need to log in to Handshake every time to generate a QR code, they can generate it once at the [Handshake Generator](https://coda-coda.gitlab.io/handshake/Generator/) then keep their static unique QR code for future use.
 - The use of Google forms and sheets as opposed to a database, while unorthodox, does make it easy to publicly share data in an append only manner, is free, and seems appropriate for this bare-bones version.
 - This does rely on trusting that people don't mess with Handshake by adding fake entries, but I am hopeful that this would not happen. Fully featured versions of Handshake could mitigate this in various ways I'm sure.
 - The Handshake idea was partly inspired by [Co-Epi](https://www.coepi.org/).

 # Future work ideas: (just ideas, I am not in a position to work on them)
 - It could also be able to generate QR codes for events with groups of people. Then everyone attending just needs to scan one QR code instead of n(n-1)/2 codes.
 - Possibly also you could have QR codes for locations such as at each coffee table or train seat, this could even work with the current set up by treating locations as people but would require additional thought.
 - Taking research into how Covid-19 is spread into account. E.g. how useful is tracking meetings between people vs tracking interactions with physical places.
 - Looking more technically into how best to preserve privacy balanced against usefulness.

# Please take this idea and make it better - I am not in a position to do so
Lastly: please feel free to take this idea and make it better :)
