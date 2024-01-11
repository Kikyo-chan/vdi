# VMware Horizon 8 customize the login page


For the basic customization or removal of "Help" or "Download" links in VMware Horizon Web HTML Login Homepage, please follow the official VMware website guidelines or refer to the expert blog for detailed instructions:

https://nolabnoparty.com/en/vmware-horizon-8-customize-the-login-page

Let's talk about how to customize or remove "Help" or "Download":

Navigate to the installation directory of VMware Horizon, typically located at:

C:\Program Files\VMware\VMware View\Server\broker\webapps\portal\webclient

Locate a file named app-htmlaccess.XXXXXXX.js within this directory. The XXXXXXX represents a version-specific string of numbers. Be sure to backup this file before making any changes.

Open the app-htmlaccess.XXXXXXX.js file with a text editor such as Visual Studio Code or Notepad++.

Use the "Find" feature of the editor to search for the following keywords to locate the links you wish to modify or remove:

privacyPolicyLink: (privacy policy link)
downloadLink: (download link)
help-link: (help link)

Once located, you can comment out the respective lines or modify the link destinations to remove or change these links. For example, to remove the privacy policy link, find the corresponding line and comment it out。
Take searching for privacy-policy、privacy-policy、help-link as an example:

Pay attention to what's in curly braces
searching  "privacy-policy"
![image](https://github.com/Kikyo-chan/vdi/assets/18164716/2849a590-53b9-4222-b8cb-9df1f84b15a7)

searching  "privacyPolicyLink"
![image](https://github.com/Kikyo-chan/vdi/assets/18164716/45be1e54-a463-4119-9682-205663b2057c)

searching  "help-link"
![image](https://github.com/Kikyo-chan/vdi/assets/18164716/13b81018-c985-4688-95e5-2ab6cd5c5998)

![image](https://github.com/Kikyo-chan/vdi/assets/18164716/8a8cb00c-125f-497a-a290-414499425325)


According to this method, look up all the XXXX-related content, then cut or delete it, and finally save it.
![image](https://github.com/Kikyo-chan/vdi/assets/18164716/ea90ac61-d469-4daf-818e-6da5932aea5b)

Alternatively, you can remove the vmware_logo:

C:\Program Files\VMware\VMware View\Server\broker\webapps\portal\webclient

Edit and modify the style.app-htmlaccess.xxxxxxx.css、style.css file:

searching  "bottom-logo" ,and delete CSS
![image](https://github.com/Kikyo-chan/vdi/assets/18164716/2ea181ed-c4f9-4089-8109-b01cedfa7d0c)

![image](https://github.com/Kikyo-chan/vdi/assets/18164716/2cc60857-4717-4cc5-b68a-280964838d37)

The final result:

![image](https://github.com/Kikyo-chan/vdi/assets/18164716/9a0a3f7c-e6a2-487a-a1e5-03c2bd836789)


The above content is only for reference and learning of technical exchanges, and is not recommended for use in the actual production environment, if you have any questions, please consult VMware official technical support.
