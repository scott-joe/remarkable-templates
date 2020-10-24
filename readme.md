# reMarkable templates

Thanks for checking out the templates I've put together. A good place to get started is the [reMarkable wiki](https://remarkablewiki.com/)

## Disclaimer
You should be comfortable with using the Terminal commands below. If not, consider an installer like [this](https://www.einkpads.com/products/remarkable-template-installer-apple-computers).

## Getting Set Up

1. Plug your reMarkable into your computer.
2. Tap the Top Left **Menu** button.
3. Tap **Settings**.
4. Tap **Help**.
5. Tap **Copyrights and licenses**.
6. Note the locaL IP address of your device.
   - Something like `192.168.1.77`.
7. Note your password.
   - Something like `8EeAOUlwbs3`.
8. Open a Terminal on your computer and use the following commands to move your files around, substituting your IP and Password for the ones you just found. You'll need to enter your password each time you make a transfer in either direction (the password won't show up as you type it).
9. Add whatever templates you want to this directory and upload them to your device.
10. Update your `templates.json` file with new entries (in JSON format).
    - You'll probably want to use the "Blank" `iconCode value` of `\ue9fe`. You can find the other codes available on the [wiki page for custom templates](https://remarkablewiki.com/tips/templates).
    - Note the `filename` property doesn't include the file format
    - Adding `categories` not already present in other entries will create a new category tab in the Templates menu on the device. You can make these as granular as you want, but I'd recommend keeping it simple and putting all your templates in "Custom".
11. Upload the updated `templates.json` file to your device.

## Commands

### Download `templates.json` from your reMarkable

`scp root@IP_ADDRESS:/usr/share/remarkable/templates/templates.json ./templates.json`

### Upload your new template to your reMarkable

`scp ./NEW_FILENAME root@IP_ADDRESS:/usr/share/remarkable/templates`

### Upload `templates.json` to your reMarkable

`scp ./templates.json root@IP_ADDRESS:/usr/share/remarkable/templates/templates.json`

## License
This repo includes a [license file](https://github.com/scott-joe/remarkable-templates/blob/main/LICENSE). Github gives you a nice little summary when you view it on here. Here's the summary it provides.

>**GNU General Public License v3.0**
> 
> Permissions of this strong copyleft license are conditioned on making available complete source code of licensed works and modifications, which include larger works using a licensed work, under the same license. Copyright and license notices must be preserved. Contributors provide an express grant of patent rights.

