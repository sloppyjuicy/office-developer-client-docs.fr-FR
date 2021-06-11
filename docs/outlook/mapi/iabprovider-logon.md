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
description: 'Derniére modification : samedi 23 juillet 2011'
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

## <a name="parameters"></a>Parameters

 _lpMAPISup_
  
> [in] Pointeur vers l’objet de support du fournisseur de carnet d’adresses.
    
 _ulUIParam_
  
> [in] Poignée vers la fenêtre parente de la boîte de dialogue d’ouverture de conversation que la méthode **Logon** affiche, si elle est autorisée. Le _paramètre ulUIParam_ contient la valeur du paramètre du même nom transmis à MAPI dans l’appel précédent à la [fonction MAPILogonEx.](mapilogonex.md) 
    
 _lpszProfileName_
  
> [in] Pointeur vers le nom du profil de session.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle l’utilisation de la logon. Les indicateurs suivants peuvent être définies :
    
AB_NO_DIALOG 
  
> Le fournisseur ne doit pas afficher de boîte de dialogue pendant l’accès. Si cet indicateur n’est pas définie, le fournisseur peut afficher une boîte de dialogue pour informer l’utilisateur de l’absence d’informations de configuration.
    
MAPI_DEFERRED_ERRORS 
  
> Permet à **l’utilisateur de** renvoyer correctement l’opération, éventuellement avant la fin du processus d’logonisation. 
    
MAPI_UNICODE 
  
> Toutes les chaînes doivent être au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les chaînes doivent être au format ANSI.
    
 _lpulcbSecurity_
  
> [in, out] Pointeur vers la taille, en octets, de la structure des informations d’identification de sécurité pointée par _le paramètre lppbSecurity._ Lors de l’entrée, la valeur doit être non zéro ; lors de la sortie, la valeur doit être zéro. Dans les deux cas, les pointeurs doivent être valides. 
    
 _lppbSecurity_
  
> [in, out] Pointeur vers un pointeur vers les informations d’identification de sécurité. Lors de l’entrée, la valeur doit être non zéro ; lors de la sortie, la valeur doit être zéro. Dans les deux cas, le pointeur doit être valide.
    
 _lppMAPIError_
  
> [out] Pointeur vers un pointeur vers une structure [MAPIERROR.](mapierror.md) Le  _paramètre lppMAPIError_ peut avoir la valeur NULL s’il n’existe aucune structure **MAPIERROR** à renvoyer. 
    
 _lppABLogon_
  
> [out] Pointeur vers un pointeur vers l’objet d’accès au fournisseur.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Une connexion à une session active a été établie avec succès.
    
MAPI_E_FAILONEPROVIDER 
  
> Le fournisseur ne peut pas se connecter, mais MAPI peut continuer à se connecter aux autres fournisseurs dans le service de messagerie auquel il appartient. 
    
MAPI_E_UNCONFIGURED 
  
> Le fournisseur ne dispose pas d’informations suffisantes pour terminer l’accès. MAPI appelle la fonction d’entrée de service de messagerie du fournisseur.
    
MAPI_E_UNKNOWN_CPID 
  
> Le serveur n’est pas configuré pour prendre en charge la page de code du client.
    
MAPI_E_UNKNOWN_LCID 
  
> Le serveur n’est pas configuré pour prendre en charge les informations de paramètres régionaux du client.
    
MAPI_E_USER_CANCEL 
  
> L’utilisateur a annulé l’opération,  généralement en cliquant sur le bouton Annuler dans la boîte de dialogue d’ouverture de conversation. 
    
## <a name="remarks"></a>Remarques

Les connexions sont établies avec chaque fournisseur de carnet d’adresses dans le profil de session lorsqu’un client appelle la méthode [IMAPISession::OpenAddressBook.](imapisession-openaddressbook.md) **OpenAddressBook** appelle ensuite la méthode **Logon** de chaque fournisseur. 
  
Le nom de profil pointé par le paramètre _lpszProfileName_ s’affiche dans le jeu de caractères du client de l’utilisateur, comme indiqué par la présence ou l’absence de l’indicateur MAPI_UNICODE dans le paramètre _ulFlags._ 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Dans votre implémentation de la méthode **Logon,** appelez la méthode [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) pour inscrire un identificateur unique ou une structure [MAPIUID.](mapiuid.md) Chacun de vos objets aura un identificateur d’entrée qui inclut ce **MAPIUID**. MAPI utilise **MAPIUID** pour faire correspondre un objet à son fournisseur. Par exemple, lorsqu’un client appelle la méthode [IMAPISession::OpenEntry](imapisession-openentry.md) pour ouvrir un utilisateur de messagerie, **OpenEntry** examine la partie **MAPIUID** de l’identificateur d’entrée qui a été passé et la correspond à un **MAPIUID** enregistré par un fournisseur de carnet d’adresses. 
  
Si un client se connecte à votre fournisseur plusieurs fois, vous pouvez inscrire un **MAPIUID** différent pour chaque connexion. L’inscription de structures **MAPIUID** uniques permet à MAPI d’router correctement les demandes vers l’instance de fournisseur appropriée. Toutefois, vous souhaitez peut-être que chaque objet d' logon partage un **MAPIUID**. Dans ce cas, vous devez être en mesure de gérer le routage vous-même au lieu de vous appuyer sur MAPI. Pour plus d’informations sur la création **d’un MAPIUID,** voir [Registering Service Provider Unique Identifiers](registering-service-provider-unique-identifiers.md).
  
L’objet de prise en charge que MAPI transmet à votre méthode **Logon** dans le paramètre _lpMAPISup_ permet d’accéder à de nombreuses méthodes incluses dans l’interface [IMAPISupport : IUnknown.](imapisupportiunknown.md) MAPI crée un objet de support personnalisé pour votre type de fournisseur. Par exemple, si vous devez vous connecter à un système de messagerie ou à un service d’annuaire sous-jacent lorsque vous établissez votre connexion, vous pouvez appeler la méthode [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) pour récupérer les informations d’identification de sécurité pour cette session d’ouverture de session particulière. 
  
Si **l’logon** est réussi, assurez-vous d’appeler la méthode [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) de l’objet de support pour incrémenter son nombre de références. Cela permet à votre fournisseur de conserver le pointeur d’objet de prise en charge pour le reste de la session. Si vous n’appelez pas cette **méthode AddRef,** MAPI déchargera votre fournisseur. 
  
Vous pouvez inclure le nom de profil transmis dans le paramètre  _lpszProfileName_ dans les boîtes de dialogue d’erreur, les écrans d’accès ou d’autres interfaces utilisateur. Pour utiliser le nom de profil, copiez-le dans le stockage que vous avez alloué. 
  
Créez un objet de logo et renvoyez un pointeur vers celui-ci dans le _paramètre lppABLogon._ MAPI utilise cet objet de logon pour appeler les méthodes dans votre [implémentation IABLogon.](iablogoniunknown.md) 
  
Si vous avez besoin d’un mot de passe lors de l’accès, affichez une boîte de dialogue d’AB_NO_DIALOG uniquement si l’indicateur de AB_NO_DIALOG n’est pas définie. Si l’utilisateur annule le processus d’MAPI_E_USER_CANCEL, généralement en cliquant sur le bouton Annuler dans la boîte de dialogue, MAPI_E_USER_CANCEL à partir de **l’MAPI_E_USER_CANCEL.** 
  
En règle générale, lorsqu’un fournisseur de carnet d’adresses ne peut pas se connecter, MAPI désactive le service de messagerie auquel appartient le fournisseur défaillant, autrement dit, MAPI ne tente pas d’établir de connexions pour les autres fournisseurs qui appartiennent au service pendant le reste de la durée de vie de la session. Toutefois, si votre fournisseur ne peut pas établir de connexion et que vous ne souhaitez pas désactiver l’intégralité du service, renvoyez MAPI_E_FAILONEPROVIDER ou MAPI_E_UNCONFIGURED. MAPI ne désactive pas le service de messagerie auquel appartient le fournisseur. 
  
Renvoyer MAPI_E_FAILONEPROVIDER si une erreur n’est pas suffisamment grave pour empêcher les autres fournisseurs du service de messagerie d’établir des connexions. Renvoyer MAPI_E_UNCONFIGURED si les informations de configuration nécessaires sont manquantes dans le profil et que vous ne pouvez pas afficher de boîte de dialogue pour inviter l’utilisateur. MAPI répond en appelant la fonction de point d’entrée du service de messagerie de votre fournisseur avec MSG_SERVICE_CONFIGURE définie comme paramètre  _ulContext_ pour donner au service la possibilité de se configurer lui-même, par programme ou à l’aide d’une feuille de propriétés. Lorsque la fonction de point d’entrée du service de message est terminée, MAPI retente l’accès. 
  
## <a name="see-also"></a>Voir aussi



[IABLogon::Logoff](iablogon-logoff.md)
  
[IABLogon::OpenEntry](iablogon-openentry.md)
  
[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)
  
[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IABProvider : IUnknown](iabprovideriunknown.md)

