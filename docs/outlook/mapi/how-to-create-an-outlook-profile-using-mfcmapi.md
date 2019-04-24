---
title: Créer un profil Outlook en utilisant MFCMAPI
ms.date: 05/18/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 85581bc7-2d81-46af-8836-adef39c933fc
description: MFCMAPI permet d'accéder aux magasins MAPI afin de faciliter l'étude des problèmes liés à Exchange et à Outlook et de fournir aux développeurs la prise en charge du développement MAPI.
ms.openlocfilehash: 8a300ad53918b22cc3de5554a1e3c29289cd9365
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345989"
---
# <a name="create-an-outlook-profile-using-mfcmapi"></a>Créer un profil Outlook en utilisant MFCMAPI

MFCMAPI permet d'accéder aux magasins MAPI afin de faciliter l'étude des problèmes liés à Exchange et à Outlook et de fournir aux développeurs la prise en charge du développement MAPI.

**S’applique à**: Office 365 | Outlook | Outlook 2016 
  
Pour les non-développeurs, il est recommandé d'utiliser l'interface utilisateur Outlook pour créer des profils pour Exchange 2013.
  
## <a name="configure-an-outlook-profile-using-mfcmapi"></a>Configurer un profil Outlook à l'aide de MFCMAPI

1. Ouvrez [MFCMAPI](https://mfcmapi.codeplex.com/), puis, dans le menu **Profil** , cliquez sur **afficher les profils**. 
    
2. Dans le menu **actions** , cliquez sur **créer un profil**. 
    
3. Créez un nom pour le profil, puis cliquez sur **OK**. 
    
4. Cliquez avec le bouton droit sur le nouveau profil, puis, dans le menu **services** , cliquez sur **Ajouter un service**. 
    
5. Désactivez la case à cocher «Afficher l'interface utilisateur du service», puis cliquez sur **OK**. 
    
6. Double-cliquez sur le profil nouvellement créé, puis cliquez sur le service **MSEMS** . 
    
7. Recherchez la section profil Exchange.
    
   This can be difficult in Outlook�s MAPI, since in 2010 and above there is no longer the global profile section. To find the Profile section, find the property PR_EMSMDB_SECTION_UID (0x3D150102). The value will be the GUID of the profile section persisted in binary form, which will be used in the subsequent steps. Vous aurez besoin de cette valeur à l'étape 9.
    
8. Double-cliquez sur le service **MSEMS** . 
    
9. Recherchez la section Profil **Exchange** à l'aide de l'UID de l'étape 7, puis cliquez une fois pour sélectionner la ligne. 
    
10. Dans le menu propriété, cliquez sur **propriétés supplémentaires**. 
    
11. Cliquez sur **Ajouter**, puis ajoutez les propriétés suivantes: 
    
    **pour Outlook 2016**: `PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W (0x6641001F)` et`PR_DISPLAY_NAME_W`
    
    **pour Outlook pour Office 365**: `PR_PROFILE_UNRESOLVED_NAME`, `PR_PROFILE_UNRESOLVED_SERVER`, `PR_ROH_PROXY_SERVER`, `PR_ROH_FLAGS`, `PR_ROH_PROXY_AUTH_SCHEME`, `PR_PROFILE_AUTH_PACKAGE`et`PR_ROH_PROXY_PRINCIPAL_NAME` 
    
    **pour Exchange 2013**: `PR_PROFILE_UNRESOLVED_NAME`, `PR_PROFILE_UNRESOLVED_SERVER`, `PR_ROH_PROXY_SERVER` `PR_ROH_FLAGS` `PR_ROH_PROXY_AUTH_SCHEME`,, et `PR_PROFILE_AUTH_PACKAGE`. 
    
12. Cliquez sur **OK**, puis configurez chaque propriété en fonction du tableau ci-dessous, en fonction de la version à laquelle vous vous connectez. 
    
13. Dans le menu **session** , cliquez sur **ouverture de session et afficher le magasin**, puis sélectionnez le profil (s'il n'est pas déjà sélectionné). 
    
### <a name="outlook-2016"></a>Outlook 2016
  
||||
|:-----|:-----|:-----|
|**Property** <br/> |**Tag** <br/> |**Description** <br/> |
| PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W  <br/> |0x6641001F  <br/> |Adresse SMTP de l'utilisateur  <br/> |
|PR_DISPLAY_NAME_W  <br/> |0x3001001F  <br/> |Nom d'affichage de l'utilisateur  <br/> |
|PR_STORE_PROVIDERS  <br/> |0x3D000102  <br/> |ConFigurez la valeur de cette propriété, située dans la section **EMSMDB** , et mettez à jour l'UID correspondant pour la propriété correspondante.  <br/> |
   
### <a name="outlook-for-office-365"></a>Outlook pour Office 365
  
||||
|:-----|:-----|:-----|
|**Propriété** <br/> |**Value** <br/> |**Description** <br/> |
|PR_PROFILE_UNRESOLVED_NAME<sup>1</sup> <br/> |alias de boîte aux lettres  <br/> |Alias de la boîte aux lettres cible; par exemple, administrateur  <br/> |
|PR_PROFILE_UNRESOLVED_SERVER<sup>1</sup> <br/> |ID de serveur personnalisé  <br/> |Valeur extraite de la **découverte automatique**. au format <guid>@tenant. onmicrosoft.com; par exemple, F5FA2827-5978-43cd-8FA8-E07BC3BB5591@contoso.onmicrosoft.com  <br/>  *Nœud de découverte automatique* : Response/Account/Protocol/Server (Exch)  <br/> |
|PR_ROH_PROXY_SERVER  <br/> |Outlook.office365.com  <br/> | *Nœud de découverte automatique* : Response/Account/Protocol/Server (expr) <sup>2</sup> <br/> |
|PR_ROH_FLAGS  <br/> |ROHFLAGS_USE_ROH (0x1)  <br/> ROH_FLAGS_USE_SSL (0X2)  <br/>  ROHFLAGS_MUTUAL_AUTH (0x4)  <br/>  ROHFLAGS_HTTP_FIRST_ON_FAST (0x8)  <br/>  ROHFLAGS_HTTP_FIRST_ON_SLOW (0x20)  <br/> |Contient les paramètres d'un profil utilisé par Outlook pour se connecter à Microsoft Exchange Server à l'aide d'un appel de procédure distante (RPC) sur HTTP (Hypertext Transfer Protocol). *Nœud de découverte automatique* : Response/Account/Protocol/SSL (expr) <sup>2</sup> <br/> |
| PR_ROH_PROXY_AUTH_SCHEME  <br/> | RPC_C_HTTP_AUTHN_SCHEME_BASIC (0x1)  <br/> |Représente le protocole d'authentification à utiliser pour ce *nœud de découverte automatique* : Response/Account/Protocol/package (expr) <sup>2</sup> <br/> |
|PR_PROFILE_AUTH_PACKAGE  <br/> |RPC_C_AUTHN_NONE (0x0)  <br/> |Décrit le schéma d'authentification à utiliser pour le *nœud de découverte automatique* RPC: Response/Account/Protocol/package (Exch)) <sup>3</sup> <br/> |
|PR_ROH_PROXY_PRINCIPAL_NAME  <br/> |Élément CertPrincipalName  <br/> |Utilisé pour prendre en charge l'authentification mutuelle; par exemple, le *nœud de découverte* d'msstd:Outlook. com: Response/Account/Protocol/CERTPRINCIPALNAME (expr)) <sup>2</sup> <br/> |
   
### <a name="exchange-2013"></a>Exchange 2013
  
||||
|:-----|:-----|:-----|
|**Propriété** <br/> |**Value** <br/> |**Description** <br/> |
|PR_PROFILE_UNRESOLVED_NAME<sup>1</sup> <br/> |alias de boîte aux lettres  <br/> |Alias de la boîte aux lettres cible; par exemple, administrateur  <br/> |
|PR_PROFILE_UNRESOLVED_SERVER<sup>1</sup> <br/> |ID de serveur personnalisé  <br/> |Valeur extraite de la **découverte automatique**. au format <guid>@tenant. onmicrosoft.com; par exemple, F5FA2827-5978-43cd-8FA8-E07BC3BB5591@contoso.onmicrosoft.com  <br/>  *Nœud de découverte automatique* : Response/Account/Protocol/Server (Exch)  <br/> |
|PR_ROH_PROXY_SERVER  <br/> | nom de domaine du serveur d'accès au client  <br/> | Nom de domaine complet (FQDN); par exemple, le *nœud de découverte automatique* E2013cas.contoso.com: Response/Account/Protocol/Server (expr) <sup>2</sup> <br/> |
|PR_ROH_FLAGS  <br/> |ROHFLAGS_USE_ROH (0x1)  <br/>  ROHFLAGS_HTTP_FIRST_ON_FAST (0x8)  <br/> ROHFLAGS_HTTP_FIRST_ON_SLOW (0x20))  <br/> |Contient les paramètres d'un profil utilisé par Outlook pour se connecter à Microsoft Exchange Server à l'aide d'un appel de procédure distante (RPC) sur le *nœud de découverte automatique* http (Hypertext Transfer Protocol): Response/Account/Protocol/SSL (expr) <sup>2</sup> <br/> |
| PR_ROH_PROXY_AUTH_SCHEME  <br/> | RPC_C_HTTP_AUTHN_SCHEME_NTLM (0X2)  <br/> |Représente le protocole d'authentification à utiliser pour ce *nœud de découverte automatique* : Response/Account/Protocol/package (expr) <sup>2</sup> <br/> |
|PR_PROFILE_AUTH_PACKAGE  <br/> |RPC_C_AUTHN_WINNT (0xA)  <br/> |Décrit le modèle d'authentification à utiliser pour le *nœud de découverte automatique* RPC: Response/Account/Protocol/package (Exch)) <sup>3</sup> <br/> |
   
> [!NOTE] 
> - Toutes les valeurs de propriété mentionnées ci-dessus peuvent varier pour votre organisation. 
> - <sup>1</sup> vous devez utiliser la version Unicode, plutôt que la version ANSI. 
> - Vous devez utiliser la découverte automatique basée sur la découverte automatique XML (POX). Il s'agit de la seule découverte automatique prise en charge pour la configuration des profils Outlook/Exchange.
> - Vous pouvez utiliser Outlook pour effectuer une demande de découverte automatique en votre nom en cliquant avec le bouton droit sur l'icône Outlook dans la **barre d'état système**, tout en maintenant la touche CTRL enfoncée et en cliquant sur **tester la configuration automatique du courrier électronique**. 
> - Pour PR_ROH_FLAGS, votre environnement peut nécessiter l'indicateur ROHFLAGS_SSL_ONLY (0X2) pour indiquer à MAPI d'utiliser uniquement SSL. Si votre environnement requiert l'authentification mutuelle, vous devrez également définir cet indicateur sur [ROHFLAGS_MUTUAL_AUTH (0x4)]. Le paraMétrage de ROHFLAGS_MUTUAL_AUTH (0x4) nécessite également la définition de la propriété PR_ROH_PROXY_PRINCIPAL_NAME. Vous devez définir ce nom comme nom principal du serveur.
> - <sup>2</sup> pour Outlook 2010, vous devrez utiliser le protocole Expr. Outlook 2013 utilise le protocole exHTTP. 
> - <sup>3</sup> cette valeur peut ne pas figurer dans la réponse de découverte automatique. Si ce n'est pas spécifié, le client doit utiliser Kerberos ou NTLM. 
    
Pour obtenir des conseils de dépannage, consultez la rubrique relative [à la configuration d'un profil Outlook à l'aide de MFCMAPI pour Exchange 2013](https://blogs.msdn.microsoft.com/dvespa/2014/01/16/how-to-configure-an-outlook-profile-using-mfcmapi-for-exchange-2013).
  
## <a name="see-also"></a>Voir aussi

- [Référence MAPI Outlook](https://msdn.microsoft.com/library/office/cc765775.aspx)  
- [Créer par programme un profil dans Outlook](https://msdn.microsoft.com/library/office/mt707568.aspx)
    

