= Invitation

A Rails gem to issue scoped invitations. 

Allow users to invite others to join an organization they are a part of. Plenty of gems
can issue a 'system-wide' invitation, but few offer 'scoped' invitations, giving an invited user access to
a particular organization/resource.

Invitations are issued via email. You can invite users new to the system, or invite existing users by giving
them access to a new resource.


== Overview

To issue an invitation:

* a user can invite someone to join an organization by providing an email
* if the user already exists, that user is added as a member of the organization, and a notification email is sent
* if the user does not exist, the app sends an email with a link to sign up, and creates a membership for the
new user when they sign up
* the invitation grants the invited user access to ONLY the organization they were invited to


== Prerequisites

* An authentication system with a User model and current_user helper. I use https://rubygems.org/gems/authenticate.
* You user model must include an :email attribute
* An second model for an 'organization' that groups users in a many-to-many association.

A example user-to-organization system you might be familiar with: Basecamp's concepts of accounts and users.


== Implementation




== Thanks

This gem was inspired by and draws heavily from:
* https://gist.github.com/jlegosama/9026919
* https://github.com/scambra/devise_invitable



Future additions:
* accepted flag
* expiration date
* move all view text to locale
* issue many invitations at once
* generators for views, controllers, configuration


=== License
This project rocks and uses MIT-LICENSE.
