# Members only
This project is focused on authentication systems so users can only access areas of a site they are authorized to.

If user is logged in he/she can see the name of the author of a post.
If not - they see the story but not the author.

## Features

1. Used devise
2. Used some commands, so I log out and add a name parameter to sign up form.
```
    <%= button_to "Sign out", destroy_user_session_path, method: :delete %>

      
      before_action :configure_permitted_parameters, if: :devise_controller?

      def configure_permitted_parameters
        devise_parameter_sanitizer.permit(:sign_up, keys: [:name])
      end

```