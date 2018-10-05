---
title: Créer un profil Outlook en utilisant MFCMAPI
ms.date: 05/18/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 85581bc7-2d81-46af-8836-adef39c933fc
description: MFCMAPI permet d’accéder aux magasins MAPI pour faciliter l’examen des problèmes Exchange et Outlook et pour fournir aux développeurs avec prise en charge pour le développement de MAPI.
ms.openlocfilehash: 8a300ad53918b22cc3de5554a1e3c29289cd9365
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397876"
---
# <a name="create-an-outlook-profile-using-mfcmapi"></a>Créer un profil Outlook en utilisant MFCMAPI

MFCMAPI permet d’accéder aux magasins MAPI pour faciliter l’examen des problèmes Exchange et Outlook et pour fournir aux développeurs avec prise en charge pour le développement de MAPI.

**S’applique à**: Office 365 | Outlook | Outlook 2016 
  
Pour les non-développeurs, il est recommandé d’utiliser l’interface utilisateur Outlook pour créer des profils pour Exchange 2013.
  
## <a name="configure-an-outlook-profile-using-mfcmapi"></a>Configurer un profil Outlook à l’aide de MFCMAPI

1. Ouvrez [MFCMAPI](https://mfcmapi.codeplex.com/), puis dans le menu du **profil** , cliquez sur **Afficher les profils**. 
    
2. Dans le menu **Actions** , cliquez sur **Créer un profil**. 
    
3. Créer un nouveau nom pour le profil, puis cliquez sur **OK**. 
    
4. Cliquez sur le nouveau profil, puis, dans le menu **Services** , cliquez sur **Ajouter un Service**. 
    
5. Désactivez la case « Affichage de l’interface utilisateur des Service », puis cliquez sur **OK**. 
    
6. Double-cliquez sur le profil nouvellement créé, puis cliquez sur le service **MSEMS** . 
    
7. Recherchez la section profil Exchange.
    
   This can be difficult in Outlook�s MAPI, since in 2010 and above there is no longer the global profile section. To find the Profile section, find the property PR_EMSMDB_SECTION_UID (0x3D150102). The value will be the GUID of the profile section persisted in binary form, which will be used in the subsequent steps. Vous aurez besoin de cette valeur à l’étape 9.
    
8. Double-cliquez sur le service **MSEMS** . 
    
9. Recherchez la section de profil **Exchange** à l’aide de l’UID de l’étape 7, puis cliquez pour sélectionner la ligne. 
    
10. Dans le menu de la propriété, cliquez sur **Propriétés supplémentaires**. 
    
11. Cliquez sur **Ajouter**, puis ajoutez les propriétés suivantes : 
    
    **Pour Outlook 2016**: `PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W (0x6641001F)` et`PR_DISPLAY_NAME_W`
    
    **Pour Outlook pour Office 365**: `PR_PROFILE_UNRESOLVED_NAME`, `PR_PROFILE_UNRESOLVED_SERVER`, `PR_ROH_PROXY_SERVER`, `PR_ROH_FLAGS`, `PR_ROH_PROXY_AUTH_SCHEME`, `PR_PROFILE_AUTH_PACKAGE`, et`PR_ROH_PROXY_PRINCIPAL_NAME` 
    
    **Pour Exchange 2013**: `PR_PROFILE_UNRESOLVED_NAME`, `PR_PROFILE_UNRESOLVED_SERVER`, `PR_ROH_PROXY_SERVER`, `PR_ROH_FLAGS`, `PR_ROH_PROXY_AUTH_SCHEME`, et `PR_PROFILE_AUTH_PACKAGE`. 
    
12. Cliquez sur **OK**, puis configurer chaque propriété en fonction du tableau ci-dessous, en fonction de la version que vous vous connectez. 
    
13. Dans le menu **Session** , cliquez sur **ouverture de session et afficher**, puis sélectionnez le profil (si elle n’est pas déjà sélectionné). 
    
### <a name="outlook-2016"></a>Outlook 2016
  
||||
|:-----|:-----|:-----|
|**Propriété** <br/> |**Tag** <br/> |**Description** <br/> |
| PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W  <br/> |0x6641001F  <br/> |Adresse SMTP de l’utilisateur  <br/> |
|PR_DISPLAY_NAME_W  <br/> |0x3001001F  <br/> |Le nom complet de l’utilisateur  <br/> |
|PR_STORE_PROVIDERS  <br/> |0x3D000102  <br/> |Configurez la valeur de cette propriété, dans la section **EMSMDB** et mettre à jour de l’UID correspondante de la propriété correspondante  <br/> |
   
### <a name="outlook-for-office-365"></a>Outlook pour Office 365
  
||||
|:-----|:-----|:-----|
|**Propriété** <br/> |**Valeur** <br/> |**Description** <br/> |
|PR_PROFILE_UNRESOLVED_NAME<sup>1</sup> <br/> |alias de boîte aux lettres  <br/> |L’alias de la boîte aux lettres cible ; par exemple, administrateur  <br/> |
|PR_PROFILE_UNRESOLVED_SERVER<sup>1</sup> <br/> |id du serveur personnalisé  <br/> |La valeur est récupérée à partir de la **découverte automatique**. dans le format <guid>@tenant.onmicrosoft.com ; par exemple, F5FA2827-5978-43cd-8FA8-E07BC3BB5591@contoso.onmicrosoft.com  <br/>  *Nœud de découverte automatique* : réponse/compte/protocole/serveur (EXCH)  <br/> |
|PR_ROH_PROXY_SERVER  <br/> |Outlook.Office365.com  <br/> | *Nœud de découverte automatique* : réponse/compte/protocole/serveur (EXPR) <sup>2</sup> <br/> |
|PR_ROH_FLAGS  <br/> |ROHFLAGS_USE_ROH (0 X 1)  <br/> ROH_FLAGS_USE_SSL (0 X 2)  <br/>  ROHFLAGS_MUTUAL_AUTH (0 X 4)  <br/>  ROHFLAGS_HTTP_FIRST_ON_FAST (0 X 8)  <br/>  ROHFLAGS_HTTP_FIRST_ON_SLOW (0 X 20)  <br/> |Contient les paramètres d’un profil utilisé par Outlook pour se connecter à Microsoft Exchange Server à l’aide d’un appel de procédure distante (RPC) sur protocole HTTP (Hypertext Transfer). *Nœud de découverte automatique* : réponse/compte/protocole/SSL (EXPR) <sup>2</sup> <br/> |
| PR_ROH_PROXY_AUTH_SCHEME  <br/> | RPC_C_HTTP_AUTHN_SCHEME_BASIC (0 X 1)  <br/> |Représente le protocole d’authentification à utiliser pour ce profil de *Nœud de découverte automatique* : réponse/compte/protocole/AuthPackage (EXPR) <sup>2</sup> <br/> |
|PR_PROFILE_AUTH_PACKAGE  <br/> |RPC_C_AUTHN_NONE (0 X 0)  <br/> |Décrit le schéma d’authentification à utiliser pour le *Nœud de la découverte automatique* de RPC : réponse/compte/protocole/AuthPackage (EXCH)) <sup>3</sup> <br/> |
|PR_ROH_PROXY_PRINCIPAL_NAME  <br/> |Élément CertPrincipalName  <br/> |Utilisé pour prendre en charge l’authentification mutuelle ; par exemple, msstd : Outlook.com *Nœud de découverte automatique* : réponse/compte/protocole/CertPrincipalName (EXPR)) <sup>2</sup> <br/> |
   
### <a name="exchange-2013"></a>Exchange 2013
  
||||
|:-----|:-----|:-----|
|**Propriété** <br/> |**Valeur** <br/> |**Description** <br/> |
|PR_PROFILE_UNRESOLVED_NAME<sup>1</sup> <br/> |alias de boîte aux lettres  <br/> |L’alias de la boîte aux lettres cible ; par exemple, administrateur  <br/> |
|PR_PROFILE_UNRESOLVED_SERVER<sup>1</sup> <br/> |id du serveur personnalisé  <br/> |La valeur est récupérée à partir de la **découverte automatique**. dans le format <guid>@tenant.onmicrosoft.com ; par exemple, F5FA2827-5978-43cd-8FA8-E07BC3BB5591@contoso.onmicrosoft.com  <br/>  *Nœud de découverte automatique* : réponse/compte/protocole/serveur (EXCH)  <br/> |
|PR_ROH_PROXY_SERVER  <br/> | nom de domaine du serveur client access  <br/> | Le nom de domaine complet (FQDN) ; par exemple, e2013cas.contoso.com *Nœud de découverte automatique* : réponse/compte/protocole/serveur (EXPR) <sup>2</sup> <br/> |
|PR_ROH_FLAGS  <br/> |ROHFLAGS_USE_ROH (0 X 1)  <br/>  ROHFLAGS_HTTP_FIRST_ON_FAST (0 X 8)  <br/> ROHFLAGS_HTTP_FIRST_ON_SLOW (0 X 20))  <br/> |Contient les paramètres d’un profil utilisé par Outlook pour se connecter à Microsoft Exchange Server à l’aide d’un appel de procédure distante (RPC) sur le protocole HTTP (Hypertext Transfer) *Nœud de découverte automatique* : réponse/compte/protocole/SSL (EXPR) <sup>2</sup> <br/> |
| PR_ROH_PROXY_AUTH_SCHEME  <br/> | RPC_C_HTTP_AUTHN_SCHEME_NTLM (0 X 2)  <br/> |Représente le protocole d’authentification à utiliser pour ce profil de *Nœud de découverte automatique* : réponse/compte/protocole/AuthPackage (EXPR) <sup>2</sup> <br/> |
|PR_PROFILE_AUTH_PACKAGE  <br/> |RPC_C_AUTHN_WINNT (0XA)  <br/> |Décrit le schéma d’authentification à utiliser pour RPC *Nœud de découverte automatique* : réponse/compte/protocole/AuthPackage (EXCH)) <sup>3</sup> <br/> |
   
> [!NOTE] 
> - Toutes les valeurs de propriété mentionnés ci-dessus peuvent varier pour votre organisation. 
> - <sup>1</sup> , vous devez utiliser la version Unicode, plutôt que la version ANSI. 
> - Vous devez utiliser le XML ancienne simple (POX) en fonction de découverte automatique. Il s’agit de la découverte automatique pris en charge uniquement pour la configuration des profils Outlook/Exchange.
> - Vous pouvez utiliser Outlook pour créer une demande de découverte automatique en votre nom en double-cliquant sur l’icône Outlook dans la **Barre d’état système**, tout en maintenant la touche CTRL ENFONCÉE et en cliquant sur la **Configuration automatique du courrier électronique de Test**. 
> - Pour PR_ROH_FLAGS, votre environnement peut nécessiter l’indicateur ROHFLAGS_SSL_ONLY (0 x 2) pour indiquer à MAPI à utiliser SSL uniquement. Si votre environnement nécessite l’authentification mutuelle, vous devez définir cet indicateur [ROHFLAGS_MUTUAL_AUTH (0 x 4)]. Définition de ROHFLAGS_MUTUAL_AUTH (0 x 4) nécessite que vous définissez également la propriété PR_ROH_PROXY_PRINCIPAL_NAME. Vous devez définir cette option pour être le nom principal du serveur.
> - <sup>2</sup> pour Outlook 2010, vous devez utiliser le protocole EXPR. Outlook 2013 utilise le protocole EXHTTP. 
> - <sup>3</sup> cette valeur ne peut pas être dans la réponse de découverte automatique. Le cas contraire, le client doit utiliser Kerberos ou NTLM. 
    
Pour des conseils de dépannage, voir [comment configurer un profil Outlook à l’aide de MFCMAPI pour Exchange 2013](https://blogs.msdn.microsoft.com/dvespa/2014/01/16/how-to-configure-an-outlook-profile-using-mfcmapi-for-exchange-2013).
  
## <a name="see-also"></a>Voir aussi

- [Référence MAPI Outlook](https://msdn.microsoft.com/library/office/cc765775.aspx)  
- [Créer par programme un profil dans Outlook](https://msdn.microsoft.com/library/office/mt707568.aspx)
    

