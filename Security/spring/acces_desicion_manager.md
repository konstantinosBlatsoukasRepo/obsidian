determines whether a user is granted to access a resource (e.g. a rest endpoint)

By default spring uses votes to determine whether a user has the right or not to access an endpoint.

Built in voters

1. WebExpressionVoter // @PreAuthorize
2. RoleVoter // decision based on the role
3. AuthenticatedVoter // whether a user is authenticated

You can develop a custom voter.

The final decision is made usign the following strategies:

1. _ConsensusBased_ : grants access if there are more affirmative votes than negatives
2. _AffirmativeBased_:  grants access if any voter grants access 
3. _UnanimousBased_: grants access if every voter grants access or abstains


https://www.baeldung.com/spring-security-custom-voter