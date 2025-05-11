# Facebook Group Delete All Members Script
If you want to delete a Facebook group, Facebook requires you to delete **all** members of the group (except yourself) first. However, Facebook provides no method to remove multiple members at once; you have to delete each member individually.

For small groups, this is no problem. But for for large groups with hundreds or thousands of members, this can be almost *impossible* for the group admin.

The `facebook-delete-all-members.js` file uses Javascript via your web browser to delete multiple group members for you. This script will not work unless you have administrator privileges in the group.

# Usage

1. Locate your Facebok ID number. If you don't know it, use a tool like http://findfacebookid.com/ to find it.

1. Click on the `facebook-delete-all-members.js` script above then click the **Raw** button. This will make sure you don't copy any additional information (like line numbers).

1. Copy and paste the raw script into a text editor.

1. Edit the line of the script that starts with `var excludedFbIds = ['1234567890'];` and put your Facebook ID number inside the single quotes. If you don't do this, the script will *technically* work, but will potentially remove your account from the group.

1. If you have more than one group member you'd like to exclude (i.e. keep in the group after the script is finished), enter it in the `excludedFbIds` array with a comma and its own single quotes, like this: `var excludedFbIds = ['1234567890','987654321'];`. You can enter as many Facebook IDs as you'd like in the array and the script will ignore them.

1. Open the **Members** page of your Facebook group. **This script will not work** unless you're on the group's **Members** page when you run it.

1. Access the Javascript console in your browser. In Firefox and Chrome, right-click on the webpage and select **Inspect**, then find the **Console** tab and click it.

1. Locate the `>` prompt in the console, then copy and paste the **edited** version of the script (which has your Facebook ID in it). If you paste the script without first editing your Facebook ID, it will not work.

1. Hit `ENTER`, sit back, and watch the script start deleting members. Check back occasionally to see if the script has timed out (very common) and needs to be restarted.

# Troubleshooting
If the script doesn't work:
* Make sure you entered your Facebook ID properly
* Make sure you have admin privileges to the group
* Make sure you are running the script from the group's **Members** page

If the script times out or starts to run too slowly, you'll need to restart it. Simply:
* Close the Javascript console
* Refresh the **Members** page
* Re-paste your edited version of the script in the console.

If Facebook is running slowly, the script will also work slowly. Normally, it deletes about 1 user per second. For a group of 10,000 members, that would take between 2.5-3 hours... assuming the script doesn't stop. However, the script will likely need to be refreshed and restarted periodically, so check back often to make sure it's still removing members.

If **This user is not a member of the group** pops up, you can ignore it and restart the script if needed. This usually happens when a Facebook account has been deleted, but Facebook hasn't refreshed the group membership list yet.

# Use At Your Own Risk
I make no warranties about this script. I don't guarantee it will work for you. If it's not working, either you're doing something wrong (see **Troubleshooting** section) or Facebook has changed something. If Facebook changes something, you're out of luck until the script gets updated. You're not paying *anything* for this script, so no whining allowed. :)

# Acknowledgements
The original version of this script is located [here](https://gist.github.com/michaelv). It stopped working after Facebook updated their groups pages, so various fixed versions (including this repo) are now available.
