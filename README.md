# Zydeo*
A Ruby on Rails app to consume Zype REST API, display some videos and do some cool stuff. :)

![Zydeo Logo](https://www.squadhelp.com/story_images/visual_images/1594159828-zydeo2%20image1.jpg)
_____________________
### Running up project externally
A working demo of this project can be found at [`https://zydeo.herokuapp.com/`](https://zydeo.herokuapp.com/)

Plus, a video of the author presenting the website and describing the application can be seen 
at [`https://www.loom.com/share/b6cc8eafb8344ef898970c0e6d796ac8`](https://www.loom.com/share/b6cc8eafb8344ef898970c0e6d796ac8)

### Setting up project locally
  * Clone this project
  * Setup project: `rake db:create` -> `rake db:migrate`
  * Start server: `rails s`
  * Execute it on base url [`localhost:3000`](http://localhost:3000).

Now it's possible to sign up using any email address but only users with a signature (a valid token within 
Zype platform) are able to see all the videos, including the ones marked as `subscription_required=true` 
_____________________
## Project Structure

### Controllers
```sh
Name            Description
Registrations   Inherits behavior from controller Devise::Registrations and overrides it to include TokensManager
Sessions        Inherits behavior from controller Devise::Sessions and overrides it to include TokensManager
Videos          Implements actions to display all of the available videos and a single one (index | show)
```
### Models
```sh
Name            Description
User            Persists users information used to log in the local system and access tokens to
                communicate with Zype API
```
### Managers
```sh
Name            Description
Tokens          Implements logic that consumes Zype API and deals with all tasks related to user authentication
Videos          Implements logic that consumes Zype API and deals with all tasks related to video retrieving
```
_____________________


##### * COPYRIGHT
- Zydeo Logo was a curious coincidence in this context: I named the project as Zydeo (Zype video) and when typing it
on Google Images I happened to find this logo, which was exactly what I meant for this context. The original can be 
found at [`https://www.squadhelp.com/name/zydeo`](https://www.squadhelp.com/name/zydeo) (as it's being sold, it means
probably copyrighted...)

- Template: [`http://uxart.io/downloads/metavideo-html/index.html`](http://uxart.io/downloads/metavideo-html/index.html)
