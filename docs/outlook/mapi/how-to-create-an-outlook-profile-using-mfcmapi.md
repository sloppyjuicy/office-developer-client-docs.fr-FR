---
title: Créer un profil Outlook en utilisant MFCMAPI
ms.date: 05/18/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 85581bc7-2d81-46af-8836-adef39c933fc
description: MFCMAPI permet d’accéder aux magasins MAPI pour faciliter l’examen des problèmes Exchange et Outlook et fournir aux développeurs la prise en charge du développement MAPI.
ms.openlocfilehash: 8a300ad53918b22cc3de5554a1e3c29289cd9365
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345989"
---
# <a name="create-an-outlook-profile-using-mfcmapi"></a>Créer un profil Outlook en utilisant MFCMAPI

MFCMAPI permet d’accéder aux magasins MAPI pour faciliter l’examen des problèmes Exchange et Outlook et fournir aux développeurs la prise en charge du développement MAPI.

**S’applique à**: Office 365 | Outlook | Outlook 2016 
  
Pour les non-développeurs, il est recommandé d’utiliser l’interface utilisateur Outlook pour créer des profils pour Exchange 2013.
  
## <a name="configure-an-outlook-profile-using-mfcmapi"></a>Configurer un profil Outlook à l’aide de MFCMAPI

1. Ouvrez [MFCMAPI](https://mfcmapi.codeplex.com/)et, dans le menu **Profil,** cliquez sur **Afficher les profils.** 
    
2. Dans le menu **Actions,** cliquez sur **Créer un profil.** 
    
3. Créez un nom pour le profil, puis cliquez sur **OK.** 
    
4. Cliquez avec le bouton droit sur le nouveau profil, puis, dans le menu **Services,** cliquez **sur Ajouter un service.** 
    
5. Décochez la case « Afficher l’interface utilisateur du service », puis cliquez sur **OK.** 
    
6. Double-cliquez sur le profil nouvellement créé, puis cliquez sur le service **MSEMS.** 
    
7. Recherchez la section Exchange profil.
    
   This can be difficult in Outlook�s MAPI, since in 2010 and above there is no longer the global profile section. To find the Profile section, find the property PR_EMSMDB_SECTION_UID (0x3D150102). The value will be the GUID of the profile section persisted in binary form, which will be used in the subsequent steps. Vous aurez besoin de cette valeur à l’étape 9.
    
8. Double-cliquez sur le service **MSEMS.** 
    
9. Recherchez la section **Exchange** profil utilisateur à l’aide de l’UID de l’étape 7, puis cliquez en un seul clic pour sélectionner la ligne. 
    
10. Dans le menu Propriétés, cliquez **sur Propriétés supplémentaires.** 
    
11. Cliquez **sur** Ajouter, puis ajoutez les propriétés suivantes : 
    
    **Pour Outlook 2016**: `PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W (0x6641001F)` et`PR_DISPLAY_NAME_W`
    
    **Par Outlook pour Office 365**: `PR_PROFILE_UNRESOLVED_NAME` , `PR_PROFILE_UNRESOLVED_SERVER` , , `PR_ROH_PROXY_SERVER` `PR_ROH_FLAGS` , `PR_ROH_PROXY_AUTH_SCHEME` et `PR_PROFILE_AUTH_PACKAGE``PR_ROH_PROXY_PRINCIPAL_NAME` 
    
    **Pour Exchange 2013**: `PR_PROFILE_UNRESOLVED_NAME` `PR_PROFILE_UNRESOLVED_SERVER` , , , `PR_ROH_PROXY_SERVER` et `PR_ROH_FLAGS` `PR_ROH_PROXY_AUTH_SCHEME` `PR_PROFILE_AUTH_PACKAGE` . 
    
12. Cliquez **sur OK,** puis configurez chaque propriété en fonction du tableau ci-dessous, en fonction de la version à qui vous vous connectez. 
    
13. Dans le menu **Session,** cliquez sur **Ouverture** de session et Magasin d’affichage, puis sélectionnez le profil (s’il n’est pas déjà sélectionné). 
    
### <a name="outlook-2016"></a>Outlook 2016
  
||||
|:-----|:-----|:-----|
|**Property** <br/> |**Tag** <br/> |**Description** <br/> |
| PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W  <br/> |0x6641001F  <br/> |Adresse SMTP de l’utilisateur  <br/> |
|PR_DISPLAY_NAME_W  <br/> |0x3001001F  <br/> |Nom d’affichage de l’utilisateur  <br/> |
|PR_STORE_PROVIDERS  <br/> |0x3D000102  <br/> |Configurer la valeur de cette propriété, située dans la section **EMSMDB,** et mettre à jour l’UID correspondant pour la propriété correspondante  <br/> |
   
### <a name="outlook-for-office-365"></a>Outlook pour Office 365
  
||||
|:-----|:-----|:-----|
|**Propriété** <br/> |**Valeur** <br/> |**Description** <br/> |
|PR_PROFILE_UNRESOLVED_NAME<sup>1</sup> <br/> |alias de boîte aux lettres  <br/> |Alias de la boîte aux lettres cible ; par exemple, Administrateur  <br/> |
|PR_PROFILE_UNRESOLVED_SERVER<sup>1</sup> <br/> |ID de serveur personnalisé  <br/> |Valeur récupérée à partir **de la découverte automatique.** au format <guid> @tenant.onmicrosoft.com; par exemple, F5FA2827-5978-43cd-8FA8-E07BC3BB5591@contoso.onmicrosoft.com  <br/>  *Nœud de découverte automatique*  : Réponse/Compte/Protocole/Serveur (EXCH)  <br/> |
|PR_ROH_PROXY_SERVER  <br/> |outlook.office365.com  <br/> | *Nœud de découverte automatique*  : Réponse/Compte/Protocole/Serveur (EXPR) <sup>2</sup> <br/> |
|PR_ROH_FLAGS  <br/> |ROHFLAGS_USE_ROH (0x1)  <br/> ROH_FLAGS_USE_SSL (0x2)  <br/>  ROHFLAGS_MUTUAL_AUTH (0x4)  <br/>  ROHFLAGS_HTTP_FIRST_ON_FAST (0x8)  <br/>  ROHFLAGS_HTTP_FIRST_ON_SLOW (0x20)  <br/> |Contient les paramètres d’un profil utilisé par Outlook pour se connecter à Microsoft Exchange Server à l’aide d’un appel de procédure distante (RPC) sur HTTP (Hypertext Transfer Protocol). *Nœud de découverte automatique*  : Response/Account/Protocol/SSL (EXPR) <sup>2</sup> <br/> |
| PR_ROH_PROXY_AUTH_SCHEME  <br/> | RPC_C_HTTP_AUTHN_SCHEME_BASIC (0x1)  <br/> |Représente le protocole d’authentification  à utiliser pour ce nœud de découverte automatique de profil : Response/Account/Protocol/AuthPackage (EXPR) <sup>2</sup> <br/> |
|PR_PROFILE_AUTH_PACKAGE  <br/> |RPC_C_AUTHN_NONE (0x0)  <br/> |Décrit le schéma d’authentification à utiliser pour le nœud de découverte automatique *RPC*  : Response/Account/Protocol/AuthPackage (EXCH) <sup>3</sup> <br/> |
|PR_ROH_PROXY_PRINCIPAL_NAME  <br/> |Élément CertPrincipalName  <br/> |Utilisé pour prendre en charge l’authentification mutuelle ; par exemple, msstd:outlook.com *Autodiscover Node*  : Response/Account/Protocol/CertPrincipalName (EXPR) <sup>) 2</sup> <br/> |
   
### <a name="exchange-2013"></a>Exchange 2013
  
||||
|:-----|:-----|:-----|
|**Propriété** <br/> |**Valeur** <br/> |**Description** <br/> |
|PR_PROFILE_UNRESOLVED_NAME<sup>1</sup> <br/> |alias de boîte aux lettres  <br/> |Alias de la boîte aux lettres cible ; par exemple, Administrateur  <br/> |
|PR_PROFILE_UNRESOLVED_SERVER<sup>1</sup> <br/> |ID de serveur personnalisé  <br/> |Valeur récupérée à partir **de la découverte automatique.** au format <guid> @tenant.onmicrosoft.com; par exemple, F5FA2827-5978-43cd-8FA8-E07BC3BB5591@contoso.onmicrosoft.com  <br/>  *Nœud de découverte automatique*  : Réponse/Compte/Protocole/Serveur (EXCH)  <br/> |
|PR_ROH_PROXY_SERVER  <br/> | nom de domaine du serveur d’accès au client  <br/> | Le nom de domaine complet (FQDN) ; par exemple, e2013cas.contoso.com  *de*  découverte automatique : Response/Account/Protocol/Server (EXPR) <sup>2</sup> <br/> |
|PR_ROH_FLAGS  <br/> |ROHFLAGS_USE_ROH (0x1)  <br/>  ROHFLAGS_HTTP_FIRST_ON_FAST (0x8)  <br/> ROHFLAGS_HTTP_FIRST_ON_SLOW (0x20))  <br/> |Contient les paramètres d’un profil utilisé par Outlook pour se connecter à Microsoft Exchange Server à l’aide d’un appel de procédure distante (RPC) sur un nœud de découverte automatique HTTP (Hypertext Transfer *Protocol)* : Réponse/Compte/Protocole/SSL (EXPR) <sup>2</sup> <br/> |
| PR_ROH_PROXY_AUTH_SCHEME  <br/> | RPC_C_HTTP_AUTHN_SCHEME_NTLM (0x2)  <br/> |Représente le protocole d’authentification  à utiliser pour ce nœud de découverte automatique de profil : Response/Account/Protocol/AuthPackage (EXPR) <sup>2</sup> <br/> |
|PR_PROFILE_AUTH_PACKAGE  <br/> |RPC_C_AUTHN_WINNT (0xA)  <br/> |Décrit le schéma d’authentification à utiliser pour le nœud de découverte automatique *RPC*  : Response/Account/Protocol/AuthPackage (EXCH) ) <sup>3</sup> <br/> |
   
> [!NOTE] 
> - Toutes les valeurs de propriété mentionnées ci-dessus peuvent varier pour votre organisation particulière. 
> - <sup>1</sup> Vous devez utiliser la version Unicode, plutôt que la version ANSI. 
> - Vous devez utiliser la découverte automatique basée sur l’ancien XML simple (POX). Il s’agit de la seule découverte automatique prise en charge pour la configuration Outlook/Exchange profils.
> - Vous pouvez utiliser Outlook pour effectuer une demande de découverte automatique en votre nom en cliquant avec le bouton droit sur l’icône Outlook dans la bac **système,** tout en maintenant la Ctrl en place et en cliquant sur **Tester** la configuration automatique du courrier électronique. 
> - Par PR_ROH_FLAGS, votre environnement peut exiger l’indicateur ROHFLAGS_SSL_ONLY (0x2) pour indiquer à MAPI d’utiliser uniquement SSL. Si votre environnement nécessite une authentification mutuelle, vous devez également définir cet indicateur [ROHFLAGS_MUTUAL_AUTH (0x4)]. La ROHFLAGS_MUTUAL_AUTH (0x4) nécessite de définir également la propriété PR_ROH_PROXY_PRINCIPAL_NAME. Vous devez définir ce nom comme le nom principal du serveur.
> - <sup>2</sup> Pour Outlook 2010, vous devez utiliser le protocole EXPR. Outlook 2013 utilise le protocole EXHTTP. 
> - <sup>3</sup> Cette valeur n’est peut-être pas dans la réponse de découverte automatique. S’il n’est pas spécifié, le client doit utiliser Kerberos ou NTLM. 
    
Pour obtenir des conseils de dépannage, voir Comment configurer un profil Outlook’aide de [MFCMAPI pour Exchange 2013](https://blogs.msdn.microsoft.com/dvespa/2014/01/16/how-to-configure-an-outlook-profile-using-mfcmapi-for-exchange-2013).
  
## <a name="see-also"></a>Voir aussi

- [Référence MAPI Outlook](https://msdn.microsoft.com/library/office/cc765775.aspx)  
- [Créer un profil par programme dans Outlook](https://msdn.microsoft.com/library/office/mt707568.aspx)
    

