# Example usage when Weechat is running on a remote PC and you want
# want to use port 4321 for the connection.
#
#     On the "client" (where the notifications will end up), host is
#     the remote host where weechat is running:
#        python2 location/of/pyrnotify.py 4321 & ssh -R 4321:localhost:4321 username@host
#     You can have a second argument to specified the time to display the notification
#       python2 location/of/pyrnotify.py 4321 2000 & ssh -R 4321:localhost:4321 username@host
#     Important to remember is that you should probably setup the
#     connection with public key encryption and use something like
#     autossh to do this in the background.
#
#     In weechat:
#        /python load pyrnotify.py
#        and set the port
#        /set plugins.var.python.pyrnotify.port 4321
#
# It is also possible to set which host pyrnotify shall connect to,
# this is not recommended. Using a ssh port-forward is much safer
# and doesn't require any ports but ssh to be open.

# ChangeLog:
#
# 2016-**-**: Changed escaping and made it more dunst (http://knopwob.org/dunst/index.html) friendly 
# 2014-05-10: Change hook_print callback argument type of displayed/highlight
#             (WeeChat >= 1.0)
# 2012-06-19: Added simple escaping to the title and body strings for
#             the script to handle trailing backslashes.
