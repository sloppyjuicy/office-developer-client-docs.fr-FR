---
title: IABProviderLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABProvider.Logon
api_type:
- COM
ms.assetid: f9468715-1674-4d14-81c8-2f24dbaa0453
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 59c6d4a05c91511ad8c481fd4ddbe42396442190
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348782"
---
# <a name="iabproviderlogon"></a>IABProvider::Logon

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Établit une connexion à une session active.
  
```cpp
HRESULT Logon(
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  ULONG ulFlags,
  ULONG FAR * lpulcbSecurity,
  LPBYTE FAR * lppbSecurity,
  LPMAPIERROR FAR * lppMAPIError,
  LPABLOGON FAR * lppABLogon
);
```

## <a name="parameters"></a>Paramètres

 _lpMAPISup_
  
> dans Pointeur vers l'objet de prise en charge du fournisseur de carnet d'adresses.
    
 _ulUIParam_
  
> dans Handle de la fenêtre parente de la boîte de dialogue d'ouverture de session que la méthode **d'ouverture de session** affiche, si elle est autorisée. Le paramètre _ulUIParam_ contient la valeur du paramètre du même nom transmis à MAPI dans l'appel précédent à la fonction [MAPILogonEx](mapilogonex.md) . 
    
 _lpszProfileName_
  
> dans Pointeur vers le nom du profil de session.
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le mode d'exécution de l'ouverture de session. Les indicateurs suivants peuvent être définis:
    
AB_NO_DIALOG 
  
> Le fournisseur ne doit pas afficher de boîte de dialogue lors de l'ouverture de session. Si cet indicateur n'est pas défini, le fournisseur peut afficher une boîte de dialogue pour inviter l'utilisateur à fournir des informations de configuration manquantes.
    
MAPI_DEFERRED_ERRORS 
  
> Active l' **ouverture de session** pour le retour, éventuellement avant la fin du processus d'ouverture de session. 
    
MAPI_UNICODE 
  
> Toutes les chaînes doivent être au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes doivent être au format ANSI.
    
 _lpulcbSecurity_
  
> [in, out] Pointeur vers la taille, en octets, de la structure des informations d'identification de sécurité vers laquelle pointe le paramètre _lppbSecurity_ . Lors de l'entrée, la valeur doit être différente de zéro; en sortie, la valeur doit être égale à zéro. Dans les deux cas, les pointeurs doivent être valides. 
    
 _lppbSecurity_
  
> [in, out] Pointeur vers un pointeur vers des informations d'identification de sécurité. Lors de l'entrée, la valeur doit être différente de zéro; en sortie, la valeur doit être égale à zéro. Dans les deux cas, le pointeur doit être valide.
    
 _lppMAPIError_
  
> remarquer Pointeur vers un pointeur vers une structure [MAPIERROR](mapierror.md) . Le paramètre _lppMAPIError_ peut être défini sur null s'il n'existe aucune structure **MAPIERROR** à renvoyer. 
    
 _lppABLogon_
  
> remarquer Pointeur vers un pointeur vers l'objet de connexion du fournisseur.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Une connexion à une session active a été établie.
    
MAPI_E_FAILONEPROVIDER 
  
> Le fournisseur ne peut pas se connecter, mais MAPI peut continuer à se connecter aux autres fournisseurs dans le service de messagerie auquel le fournisseur appartient. 
    
MAPI_E_UNCONFIGURED 
  
> Le fournisseur ne dispose pas d'informations suffisantes pour terminer l'ouverture de session. MAPI appelle la fonction d'entrée de service de message du fournisseur.
    
MAPI_E_UNKNOWN_CPID 
  
> Le serveur n'est pas configuré pour prendre en charge la page de code du client.
    
MAPI_E_UNKNOWN_LCID 
  
> Le serveur n'est pas configuré pour prendre en charge les informations de paramètres régionaux du client.
    
MAPI_E_USER_CANCEL 
  
> L'utilisateur a annulé l'opération, généralement en cliquant sur le bouton **Annuler** dans la boîte de dialogue d'ouverture de session. 
    
## <a name="remarks"></a>Remarques

Les connexions sont établies avec chaque fournisseur de carnet d'adresses dans le profil de session lorsqu'un client appelle la méthode [IMAPISession:: OpenAddressBook](imapisession-openaddressbook.md) . **OpenAddressBook** appelle ensuite la méthode **d'ouverture de session** de chaque fournisseur. 
  
Le nom de profil désigné par le paramètre _lpszProfileName_ est affiché dans le jeu de caractères du client de l'utilisateur, tel qu'indiqué par la présence ou l'absence de l'indicateur MAPI_UNICODE dans le paramètre _ulFlags_ . 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Dans votre implémentation de la méthode **Logon** , appelez la méthode [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) pour enregistrer un identificateur unique ou une structure [MAPIUID](mapiuid.md) . Chacun de vos objets aura un identificateur d'entrée qui inclut cette **MAPIUID**. MAPI utilise le **MAPIUID** pour faire correspondre un objet à son fournisseur. Par exemple, lorsqu'un client appelle la méthode [IMAPISession:: OpenEntry](imapisession-openentry.md) pour ouvrir un utilisateur de messagerie, **OpenEntry** examine la partie **MAPIUID** de l'identificateur d'entrée qui a été passée et la met en correspondance avec une **MAPIUID** inscrite par un fournisseur de carnet d'adresses. 
  
Si un client se connecte à votre fournisseur plusieurs fois, vous souhaiterez peut-être enregistrer une autre **MAPIUID** pour chaque connexion. L'inscription de structures **MAPIUID** uniques permet à MAPI d'acheminer correctement les demandes vers l'instance de fournisseur appropriée. Toutefois, vous souhaiterez peut-être que tous les objets d'ouverture de session partagent un **MAPIUID**. Dans ce cas, vous devez être en mesure de gérer le routage vous-même au lieu de vous appuyer sur MAPI. Pour plus d'informations sur la création d'un **MAPIUID**, consultez la rubrique [Register Service Provider unique Identifiers](registering-service-provider-unique-identifiers.md).
  
L'objet support que MAPI transmet à votre méthode **d'ouverture de session** dans le paramètre _lpMAPISup_ fournit l'accès à de nombreuses méthodes incluses dans l'interface [IMAPISupport: IUnknown](imapisupportiunknown.md) . MAPI crée un objet de prise en charge personnalisé pour votre type de fournisseur. Par exemple, si vous devez vous connecter à un système de messagerie ou à un service d'annuaire sous-jacent lorsque vous établissez votre connexion, vous pouvez appeler la méthode [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) pour récupérer les informations d'identification de sécurité pour cette session de connexion particulière. 
  
Si l' **ouverture de session** réussit, veillez à appeler la méthode [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) de l'objet de prise en charge pour incrémenter son décompte de référence. Cela permet à votre fournisseur de maintenir le pointeur d'objet de prise en charge pour le reste de la session. Si vous n'appelez pas cette méthode **AddRef** , MAPI décharge votre fournisseur. 
  
Vous pouvez inclure le nom de profil transmis dans le paramètre _lpszProfileName_ dans les boîtes de dialogue d'erreur, les écrans d'ouverture de session ou d'autres interfaces utilisateur. Pour utiliser le nom du profil, copiez-le vers le stockage que vous avez alloué. 
  
Créez un objet Logon et renvoyez un pointeur vers celui-ci dans le paramètre _lppABLogon_ . MAPI utilise cet objet de connexion pour appeler les méthodes dans votre implémentation [IABLogon](iablogoniunknown.md) . 
  
Si vous avez besoin d'un mot de passe lors de l'ouverture de session, affichez une boîte de dialogue de connexion uniquement si l'indicateur AB_NO_DIALOG n'est pas défini. Si l'utilisateur annule le processus d'ouverture de session, généralement en cliquant sur le bouton **Annuler** dans la boîte de dialogue, retournez MAPI_E_USER_CANCEL à partir de l' **ouverture de session**.
  
En règle générale, lorsqu'un fournisseur de carnet d'adresses ne peut pas se connecter, MAPI désactive le service de messagerie auquel appartient le fournisseur d'erreur, c'est-à-dire que MAPI n'essaiera pas d'établir de connexions pour les autres fournisseurs qui appartiennent au service pour le reste de la session. vie. Toutefois, si votre fournisseur ne peut pas établir de connexion et que vous ne souhaitez pas désactiver le service entier, renvoyez soit MAPI_E_FAILONEPROVIDER, soit MAPI_E_UNCONFIGURED. MAPI ne désactive pas le service de messagerie auquel appartient le fournisseur. 
  
Renvoyer MAPI_E_FAILONEPROVIDER si une erreur qui n'est pas assez grave empêche les autres fournisseurs du service de messagerie d'établir des connexions. Renvoyer MAPI_E_UNCONFIGURED si les informations de configuration nécessaires ne figurent pas dans le profil et que vous ne pouvez pas afficher une boîte de dialogue invitant l'utilisateur. MAPI répond en appelant la fonction de point d'entrée du service de messages de votre fournisseur avec MSG_SERVICE_CONFIGURE défini en tant que paramètre _ulContext_ pour permettre au service de se configurer lui-même, soit par programme, soit à l'aide d'une feuille de propriétés. Une fois la fonction de point d'entrée du service de messagerie terminée, MAPI tente de se connecter. 
  
## <a name="see-also"></a>Voir aussi



[IABLogon::Logoff](iablogon-logoff.md)
  
[IABLogon::OpenEntry](iablogon-openentry.md)
  
[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)
  
[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IABProvider : IUnknown](iabprovideriunknown.md)

