##########################################
#               G-Heberge                 #
#              G-Heberge.fr               #
##########################################

# Configuration du port du serveur
endpoint_add_tcp "0.0.0.0:30120"
endpoint_add_udp "0.0.0.0:30120"

# Limite de slots du serveur
sv_maxclients 128

# Nom d'hôte de votre serveur
sv_hostname "Votre serveur G-Heberge.fr"

# Protection L7
set sv_requestParanoia 3
sv_endpointprivacy true
sv_forceIndirectListing true
sv_useDirectListing true
sv_authMinTrust 4


# Clé API Steam Web, si vous souhaitez utiliser l'authentification Steam (https://steamcommunity.com/dev/apikey)
set steam_webApiKey ""

# Clé de licence FiveM (https://keymaster.fivem.net)
set sv_licenseKey mm8d019ah81a39hdau7vm0j7o87cy2jp 

# Ressources
ensure mapmanager
ensure chat
ensure spawnmanager
ensure sessionmanager
ensure fivem
ensure hardcap
ensure rconlog

# Cela permet aux joueurs d'utiliser des plugins basés sur le scripthook, comme l'ancien menu Lambda.
# Mettez cette valeur à 1 pour autoriser le scripthook. Notez que cela ne garantit pas que les joueurs ne pourront pas utiliser de plugins externes.
sv_scriptHookAllowed 0

# Mot de passe RCON
#rcon_password ""

# Tags de votre serveurs.
# Exemple:
# - sets tags "drifting, cars, racing"
# Or:
# - sets tags "roleplay, military, tanks"
sets tags "default"

# Langue de votre serveur FiveM
# Exemple : "en-US", "fr-CA", "nl-NL", "de-DE", "en-GB", "pt-BR", "fr-FR", ...
sets locale "fr-FR" 

# Bannière de votre serveur
sets banner_detail ""
sets banner_connecting ""


# Administrateurs
add_ace group.admin command allow # allow all commands
add_ace group.admin command.quit deny # but don't allow quit
add_principal identifier.fivem:1 group.admin # add the admin to the group

# OneSync
sets onesync legacy
