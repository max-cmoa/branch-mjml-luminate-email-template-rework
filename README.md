# mjml-luminate-email-template-rework
  Reworking of the Luminate BlackBaud email template using the Mailjet Markup Language "MJML" which compiles to html
  and works with email clients that follow weird rules like using table tags/elements

## Getting Started
  Download [Visual Studio Code](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) to edit the files in this repo.

  Read [MJML Documentation](https://documentation.mjml.io/) for writing mjml

  If you are wondering what will work with email clients, I suggest [caniemail.com](https://www.caniemail.com/)

  In Visual Studio Code goto -> View -> Extensions -> MJML Extension -> Click Install

  Open up a terminal Window by clicking on the bottom of the screen "ⓧ 0 ⚠0" and click the tab that says TERMINAL

  Now you are good to start editing input.mjml and if you want to turn it into html type 
  ```$ npm run compile ``` then press enter in the terminal below and you will see a file named output.html in the
  same directory. That is the html you want for the Luminate Newsletter E-Card. 
  
### Workflow

  Create a directory with the date of the newsletter like 8_6_2022 or ```$ mkdir 8_6_2022 ```
  then ```$ cd 8_6_2022 ```

  Create an mjml file like last_change_gordon_parks.mjml
  or you could type ```$ touch last_chance_gordon_parks.mjml ``` on the command line then
   type:
  
  ```$ npm run compile --input=directory_to_file/place_your_file_name_here.mjml --output=directory_to_file/place_your_file_name_here.html ```

  For example

  ```$ npm run compile --input=8_3_2022/last_chance_gordon_parks.mjml --output=8_3_2022/last_chance_gordon_parks.html ```

  Or if you aren't viewing this in markdown, you can copy this

  npm run compile --input=8_3_2022/last_chance_gordon_parks.mjml --output=8_3_2022/last_chance_gordon_parks.html

  Where --input= is a directory to your mjml file aka "last_chance_gordon_parks.mjml" that is to be compiled as --output= html file aka "last_chance_gordon_parks.html"

  At this point, the compiled "last_chance_gordon_parks.html" will open up automatically in a browser. This is so that you can see your compiled html.

  To test your versions for dark mode and light mode, I suggest swapping light and dark in css.mjml near 
  @media (prefers-color-scheme: swapThis) {

  To save your files to the cloud aka Github,
  ```$ git status ```

  ```$ git add --all ```

  ```$ git commit -m "good commit message here" ```

  ```$ git push ```

  #### Creating include files
    Include is a file that can be reused. This is so that you don't have to place this in every template you make.
    goto the folder "includes" and create a file. Example - footer.mjml and you can include it in a main mjml file
    by following the format <mj-include path="./../includes/filename-here.mjml"/>
    You can find in the file <mj-include path="./../includes/footer.mjml"/> for example.