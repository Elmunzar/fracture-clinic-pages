# The invitation download

`index.html` takes a code, hashes it, and looks for the app in a folder named
after that hash. The code is never stored here and never compared against
anything — it *is* the address. A wrong code leads nowhere, and reading the
page source tells you nothing about where any file is.

## Putting a build here

    ../../FractureFlow/scripts/where-does-this-code-go.sh "YOUR-CODE"

prints the folder name. Make it, drop the notarised `.dmg` in as
`Praxia-Clinic-Manager.dmg`, commit, push.

## What this is and is not

It stops the app being found by anybody who has not been given a code. It does
not stop somebody passing their code to a colleague, and it is not a login.

The thing that decides who can actually *use* the app is inside the app: an NHS
email address, and an administrator approving the account. This page only keeps
the download off the open web.

To withdraw a code, delete its folder. Anyone still holding it then gets
"that code does not lead anywhere".
