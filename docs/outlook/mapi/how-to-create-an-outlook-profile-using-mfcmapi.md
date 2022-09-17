---
title: Créer un profil Outlook en utilisant MFCMAPI
manager: lindalu
ms.date: 03/11/2022
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 85581bc7-2d81-46af-8836-adef39c933fc
description: MFCMAPI fournit l’accès aux magasins MAPI pour faciliter l’examen des problèmes Exchange et Outlook et fournir aux développeurs la prise en charge du développement MAPI.
ms.openlocfilehash: 2a445d8a42419349660d66f599391620556cbf90
ms.sourcegitcommit: 9d63c4fab7bca6b2a14f9883334abbc6c490d711
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/17/2022
ms.locfileid: "67796002"
---
# <a name="create-an-outlook-profile-using-mfcmapi"></a>Créer un profil Outlook en utilisant MFCMAPI

MFCMAPI fournit l’accès aux magasins MAPI pour faciliter l’examen des problèmes Exchange et Outlook et fournir aux développeurs la prise en charge du développement MAPI. Downlaod 

**S’applique à**: Office 365 | Outlook | Outlook 2016
  
Pour les non-développeurs, il est recommandé d’utiliser l’interface utilisateur Outlook pour créer des profils pour Exchange 2013.
  
## <a name="configure-an-outlook-profile-using-mfcmapi"></a>Configurer un profil Outlook à l’aide de MFCMAPI

1. Téléchargez la [dernière version de MFCMAPI](https://github.com/stephenegriffin/mfcmapi/releases) à partir de GitHub.

1. Dans le menu **Profil** , sélectionnez **Afficher les profils**.

1. Dans le menu **Actions** , sélectionnez **Créer un profil**.

1. Créez un nom pour le profil, puis choisissez **OK**.

1. Cliquez avec le bouton droit sur le nouveau profil, puis dans le menu **Services** , sélectionnez **Ajouter un service**.

1. Décochez la case « Afficher l’interface utilisateur du service », puis choisissez **OK**.

1. Double-cliquez sur le profil nouvellement créé, puis sélectionnez le service **MSEMS** .

1. Recherchez la section Profil Exchange.

   This can be difficult in Outlook�s MAPI, since in 2010 and above there is no longer the global profile section. To find the Profile section, find the property PR_EMSMDB_SECTION_UID (0x3D150102). The value will be the GUID of the profile section persisted in binary form, which will be used in the subsequent steps. Vous aurez besoin de cette valeur à l’étape 10.

1. Double-cliquez sur le service **MSEMS** .

1. Recherchez la section profil **Exchange** à l’aide de l’UID de l’étape 7, puis cliquez sur un seul clic pour sélectionner la ligne.

1. Dans le menu **Propriétés** , sélectionnez **Propriétés supplémentaires**.

1. Sélectionnez **Ajouter**, puis ajoutez les propriétés suivantes :

    **Pour Outlook 2016** : `PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W (0x6641001F)` et`PR_DISPLAY_NAME_W`

    **Pour Outlook pour Office 365** : `PR_PROFILE_UNRESOLVED_NAME`, `PR_PROFILE_UNRESOLVED_SERVER`, `PR_ROH_PROXY_SERVER`, `PR_ROH_FLAGS`, `PR_ROH_PROXY_AUTH_SCHEME`et `PR_PROFILE_AUTH_PACKAGE``PR_ROH_PROXY_PRINCIPAL_NAME`

    **Pour Exchange 2013** : `PR_PROFILE_UNRESOLVED_NAME`, `PR_PROFILE_UNRESOLVED_SERVER`, `PR_ROH_PROXY_SERVER`, `PR_ROH_FLAGS`, `PR_ROH_PROXY_AUTH_SCHEME`et `PR_PROFILE_AUTH_PACKAGE`.

1. Choisissez **OK**, puis configurez chaque propriété en fonction du tableau ci-dessous, en fonction de la version à laquelle vous vous connectez.

1. Dans le menu **Session** , sélectionnez Ouverture de session **et Magasin d’affichage**, puis sélectionnez le profil (s’il n’est pas déjà sélectionné).

### <a name="outlook-2016"></a>Outlook 2016
  
|**Propriété**|**Tag**|**Description**|
|:-----|:-----|:-----|
|PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W  <br/> |0x6641001F  <br/> |Adresse SMTP de l’utilisateur  <br/> |
|PR_DISPLAY_NAME_W  <br/> |0x3001001F  <br/> |Nom d’affichage de l’utilisateur  <br/> |
|PR_STORE_PROVIDERS  <br/> |0x3D000102  <br/> |Configurez la valeur de cette propriété, située dans la section **EMSMDB** , et mettez à jour l’UID correspondant pour la propriété correspondante  <br/> |

### <a name="outlook-for-office-365"></a>Outlook pour Office 365
  
|**Propriété**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|PR_PROFILE_UNRESOLVED_NAME<sup>1</sup> <br/> |alias de boîte aux lettres  <br/> |Alias de la boîte aux lettres cible ; par exemple, Administrateur  <br/> |
|PR_PROFILE_UNRESOLVED_SERVER<sup>1</sup> <br/> |ID de serveur personnalisé  <br/> |Valeur récupérée à partir de la **découverte automatique**. au format *guid*@tenant.onmicrosoft.com; par exemple, F5FA2827-5978-43cd-8FA8-E07BC3BB5591@contoso.onmicrosoft.com  <br/>  *Nœud de découverte automatique*  : Response/Account/Protocol/Server (EXCH)  <br/> |
|PR_ROH_PROXY_SERVER  <br/> |outlook.office365.com  <br/> | *Nœud de découverte automatique*  : réponse/compte/protocole/serveur (EXPR) <sup>2</sup> <br/> |
|PR_ROH_FLAGS  <br/> |ROHFLAGS_USE_ROH (0x1)  <br/> ROH_FLAGS_USE_SSL (0x2)  <br/>  ROHFLAGS_MUTUAL_AUTH (0x4)  <br/>  ROHFLAGS_HTTP_FIRST_ON_FAST (0x8)  <br/>  ROHFLAGS_HTTP_FIRST_ON_SLOW (0x20)  <br/> |Contient les paramètres d’un profil utilisé par Outlook pour se connecter à Microsoft Exchange Server à l’aide d’un appel de procédure distante (RPC) via le protocole HTTP (Hypertext Transfer Protocol). *Nœud de découverte automatique*  : Response/Account/Protocol/SSL (EXPR) <sup>2</sup> <br/> |
| PR_ROH_PROXY_AUTH_SCHEME  <br/> | RPC_C_HTTP_AUTHN_SCHEME_BASIC (0x1)  <br/> |Représente le protocole d’authentification à utiliser pour ce nœud de *découverte automatique*  de profil : Response/Account/Protocol/AuthPackage (EXPR) <sup>2</sup> <br/> |
|PR_PROFILE_AUTH_PACKAGE  <br/> |RPC_C_AUTHN_NONE (0x0)  <br/> |Décrit le schéma d’authentification à utiliser pour le *nœud de découverte automatique*  RPC : Response/Account/Protocol/AuthPackage (EXCH) ) <sup>3</sup> <br/> |
|PR_ROH_PROXY_PRINCIPAL_NAME  <br/> |Élément CertPrincipalName  <br/> |Utilisé pour prendre en charge l’authentification mutuelle ; par exemple, msstd:outlook.com *Autodiscover Node*  : Response/Account/Protocol/CertPrincipalName (EXPR) ) <sup>2</sup> <br/> |

### <a name="exchange-2013"></a>Exchange 2013
  
|**Propriété**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|PR_PROFILE_UNRESOLVED_NAME<sup>1</sup> <br/> |alias de boîte aux lettres  <br/> |Alias de la boîte aux lettres cible ; par exemple, Administrateur  <br/> |
|PR_PROFILE_UNRESOLVED_SERVER<sup>1</sup> <br/> |ID de serveur personnalisé  <br/> |Valeur récupérée à partir de la **découverte automatique**. au format *guid*@tenant.onmicrosoft.com; par exemple, F5FA2827-5978-43cd-8FA8-E07BC3BB5591@contoso.onmicrosoft.com  <br/>  *Nœud de découverte automatique*  : Response/Account/Protocol/Server (EXCH)  <br/> |
|PR_ROH_PROXY_SERVER  <br/> | nom de domaine du serveur d’accès client  <br/> | Nom de domaine complet (FQDN) ; par exemple, e2013cas.contoso.com  *nœud de découverte automatique*  : Response/Account/Protocol/Server (EXPR) <sup>2</sup> <br/> |
|PR_ROH_FLAGS  <br/> |ROHFLAGS_USE_ROH (0x1)  <br/>  ROHFLAGS_HTTP_FIRST_ON_FAST (0x8)  <br/> ROHFLAGS_HTTP_FIRST_ON_SLOW (0x20))  <br/> |Contient les paramètres d’un profil utilisé par Outlook pour se connecter à Microsoft Exchange Server à l’aide d’un appel de procédure distante (RPC) via le *nœud de découverte automatique* HTTP (Hypertext Transfer Protocol) : Response/Account/Protocol/SSL (EXPR) <sup>2</sup> <br/> |
| PR_ROH_PROXY_AUTH_SCHEME  <br/> | RPC_C_HTTP_AUTHN_SCHEME_NTLM (0x2)  <br/> |Représente le protocole d’authentification à utiliser pour ce nœud de *découverte automatique*  de profil : Response/Account/Protocol/AuthPackage (EXPR) <sup>2</sup> <br/> |
|PR_PROFILE_AUTH_PACKAGE  <br/> |RPC_C_AUTHN_WINNT (0xA)  <br/> |Décrit le schéma d’authentification à utiliser pour le *nœud de découverte automatique*  RPC : Response/Account/Protocol/AuthPackage (EXCH) ) <sup>3</sup> <br/> |

> [!NOTE]
>
> - Toutes les valeurs de propriété mentionnées ci-dessus peuvent varier pour votre organisation particulière.
> - <sup>1</sup> Vous devez utiliser la version Unicode, plutôt que la version ANSI.
> - Vous devez utiliser la découverte automatique basée sur Plain Old XML (POX). Il s’agit de la seule découverte automatique prise en charge pour la configuration des profils Outlook/Exchange.
> - Vous pouvez utiliser Outlook pour effectuer une demande de découverte automatique en votre nom en cliquant avec le bouton droit sur l’icône Outlook dans la **barre d’état système**, tout en maintenant la touche Ctrl enfoncée et en cliquant sur **Tester la configuration automatique des messages électroniques**.
> - Pour PR_ROH_FLAGS, votre environnement peut nécessiter l’ROHFLAGS_SSL_ONLY d’indicateur (0x2) pour indiquer à MAPI d’utiliser uniquement SSL. Si votre environnement nécessite une authentification mutuelle, vous devez également définir cet indicateur [ROHFLAGS_MUTUAL_AUTH (0x4)]. Si vous définissez ROHFLAGS_MUTUAL_AUTH (0x4), vous devez également définir la propriété PR_ROH_PROXY_PRINCIPAL_NAME. Vous devez définir ce nom comme nom principal du serveur.
> - <sup>2</sup> Pour Outlook 2010, vous devez utiliser le protocole EXPR. Outlook 2013 utilise le protocole EXHTTP.
> - <sup>3</sup> Cette valeur peut ne pas figurer dans la réponse de découverte automatique. S’il n’est pas spécifié, le client doit utiliser Kerberos ou NTLM.

Pour obtenir des conseils de dépannage, consultez [Comment configurer un profil Outlook à l’aide de MFCMAPI pour Exchange 2013](/archive/blogs/dvespa/how-to-configure-an-outlook-profile-using-mfcmapi-for-exchange-2013).
  
## <a name="see-also"></a>Voir aussi

- [Référence MAPI Outlook](/office/client-developer/outlook/mapi/outlook-mapi-reference)
- [Créer un profil par programmation dans Outlook](/office/client-developer/outlook/mapi/how-to-programmatically-create-a-profile-in-outlook)
