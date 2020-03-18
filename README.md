I've had this idea for a website that could help, perhaps just a little, to control the spread of Cov-19.
I'm calling it Handshake for now.

This repository is the location of a bare-bones version of Handshake, described below.

# Brief overview:
 - When 2 people meet, one person goes to [Handshake Generator](https://coda-coda.gitlab.io/handshake/Generator/) and generates a Handshake QR code by entering their email address and optionally a privacy passphrase.
 - The other person scans this QR code which takes them to [Handshake Reader](https://coda-coda.gitlab.io/handshake/Reader) they also enter their email address and privacy passphrase.
 - They then are redirected (or can click the link) which takes them to a pre-filled Google Form which they simply submit (no need to log in).
 - The publicly accessible [Google Spreadsheet](https://docs.google.com/spreadsheets/d/11LaeMly8CQdM7R7MsvE2GSdWZLySA4hNaQ9GrBg53TE/edit?usp=sharing) then has a record of this interaction (recording the date/time and the SHA256 hashes of the two people's email addresses concatenated with their privacy passphrase)
 - People can report their status, e.g. healthy, suspected, or confirmed to Handshake by filling out [this form](https://forms.gle/DWQRNfaeBrwB3oD58), the responses are available publicly [here](https://docs.google.com/spreadsheets/d/1hcjN_L62VK7hPSIKkfc0YRdFE8ULYG-ebpGgSw3kxgc/edit?usp=sharing)
 
 - Handshake data can then used by anybody for purposes related to stopping the spread of Cov-19. For example, when someone is reported as having confirmed Cov-19, the data from Handshakes can be used to warn those who might have been exposed while the person was contagious to be careful (due to the current setup this would require people to regularly check a Handshake page that has not yet been created to check their risk).


# Further thoughts:
 - This website/set up was simple to create, it wouldn't be too hard to create an improved version or for anyone with some resources to do so.
 - It does not rely upon users installing any apps, making it easily accessible
 - It replaces the somewhat dangerous practice (in these times) of physically shaking hands.
 - Privacy is still an issue that would need to be tackled. Using a unique privacy passphrase and then hashing people's email addresses with it is possibly a bit helpful, but it does nothing to protect you from people you Handshake with that might want to reveal your identity. Plus, I'm not a cryptography or privacy expert so can give no guarantees around the privacy of this system whatsoever.
 - People do not need to log in to Handshake every time to generate a QR code, they can generate it once at the [Handshake Generator](https://coda-coda.gitlab.io/handshake/Generator/) then keep their static unique QR code for future use.
 - The use of Google forms and sheets as opposed to a database, while unorthodox, does make it easy to publicly share data in an append only manner, is free, and seems appropriate for this bare-bones version.
 - This does rely on trusting that people don't mess with Handshake by adding fake entries, but I am hopeful that this would not happen. Fully featured versions of Handshake could mitigate this in various ways I'm sure.

 # Future work ideas:
 - It could also be able to generate QR codes for events with groups of people. Then everyone attending just needs to scan one QR code instead of n(n-1) codes.
 - Possibly also you could have QR codes for locations such as at each coffee table or train seat, this could even work with the current set up by treating locations as people but would require additional thought.
 - Taking research into how Cov-19 is spread into account. E.g. how useful is tracking meetings between people vs tracking interactions with physical places.
 - Looking more technically into how best to preserve privacy balanced against usefulness.

Lastly: Feel free to take this idea and make it better - whether by forking this repository and making changes or by taking the idea and building on it :)