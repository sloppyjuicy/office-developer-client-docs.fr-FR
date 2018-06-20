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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 21a6907f7511779d7e8ec6825ac68d109d2f48eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783606"
---
# <a name="iabproviderlogon"></a>IABProvider::Logon

  
  
**S’applique à**: Outlook 
  
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
  
> [in] Pointeur vers l’objet de prise en charge du fournisseur de carnet d’adresses.
    
 _ulUIParam_
  
> [in] Handle vers la fenêtre parente de la boîte de dialogue d’ouverture de session qui affiche la méthode **d’ouverture de session** , en cas d’autorisation. Le paramètre _ulUIParam_ contient la valeur du paramètre du même nom passé à MAPI dans l’appel à la fonction [MAPILogonEx](mapilogonex.md) précédent. 
    
 _lpszProfileName_
  
> [in] Pointeur vers le nom du profil de la session.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont les paramètres de connexion est effectuée. Les indicateurs suivants peuvent être définis :
    
AB_NO_DIALOG 
  
> Le fournisseur ne doit pas afficher une boîte de dialogue au cours de l’ouverture de session. Si cet indicateur n’est pas défini, le fournisseur peut afficher une boîte de dialogue pour inviter l’utilisateur pour les informations de configuration manquantes.
    
MAPI_DEFERRED_ERRORS 
  
> Permet l' **ouverture de session** renvoyer avec succès, éventuellement, avant l’ouverture de session est terminée. 
    
MAPI_UNICODE 
  
> Toutes les chaînes doivent être au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes doivent être au format ANSI.
    
 _lpulcbSecurity_
  
> [entrée, sortie] Un pointeur vers la taille, en octets, de la structure d’informations d’identification de sécurité indiqué par le paramètre _lppbSecurity_ . À l’entrée, la valeur doit être différente de zéro ; dans la sortie, la valeur doit être zéro. Dans les deux cas, les pointeurs doivent être valides. 
    
 _lppbSecurity_
  
> [entrée, sortie] Pointeur vers un pointeur vers les informations d’identification de sécurité. À l’entrée, la valeur doit être différente de zéro ; dans la sortie, la valeur doit être zéro. Dans les deux cas, le pointeur doit être valid.
    
 _lppMAPIError_
  
> [out] Pointeur vers un pointeur vers une structure [MAPIERROR](mapierror.md) . Le paramètre _lppMAPIError_ peut être défini sur la valeur NULL s’il n’existe aucune structure **MAPIERROR** pour renvoyer. 
    
 _lppABLogon_
  
> [out] Pointeur vers un pointeur vers l’objet du fournisseur d’ouverture de session.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Une connexion à une session active a été établie.
    
RÉFÉRENCE À MAPI_E_FAILONEPROVIDER 
  
> Le fournisseur ne peut pas se connecter, mais MAPI peut continuer à se connecter sur les autres fournisseurs dans le service de message à laquelle appartient le fournisseur. 
    
MAPI_E_UNCONFIGURED 
  
> Le fournisseur n’a pas suffisamment d’informations pour effectuer l’ouverture de session. MAPI appelle la fonction de l’entrée de service de message du fournisseur.
    
MAPI_E_UNKNOWN_CPID 
  
> Le serveur n’est pas configuré pour prendre en charge de la page de codes du client.
    
MAPI_E_UNKNOWN_LCID 
  
> Le serveur n’est pas configuré pour prendre en charge les informations de paramètres régionaux du client.
    
MAPI_E_USER_CANCEL 
  
> L’utilisateur a annulé l’opération de généralement en cliquant sur le bouton **Annuler** dans la boîte de dialogue d’ouverture de session. 
    
## <a name="remarks"></a>Remarques

Connexions sont établies avec chaque fournisseur de carnet d’adresses dans le profil de session lorsqu’un client appelle la méthode [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) . **OpenAddressBook** appelle ensuite la méthode **d’ouverture de session** de chaque fournisseur. 
  
Le nom de profil vers laquelle pointé le paramètre _lpszProfileName_ s’affiche dans le jeu de caractères du client de l’utilisateur comme indiqué par la présence ou l’absence de l’indicateur MAPI_UNICODE dans le paramètre _ulFlags_ . 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Dans votre implémentation de la méthode **d’ouverture de session** , appelez la méthode [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) pour inscrire un identificateur unique, ou une structure [MAPIUID](mapiuid.md) . Chacun de vos objets aura un identificateur d’entrée qui inclut ce **MAPIUID**. MAPI utilise le **MAPIUID** pour correspondre à un objet avec son fournisseur. Par exemple, lorsqu’un client appelle la méthode [IMAPISession::OpenEntry](imapisession-openentry.md) pour ouvrir un utilisateur de messagerie, **OpenEntry** examine la partie **MAPIUID** de l’identificateur d’entrée qui a été passé et qu’il correspond à un **MAPIUID** enregistrés en une fournisseur de carnet d’adresses. 
  
Si un client se connecte à votre fournisseur plusieurs fois, vous souhaiterez peut-être inscrire un autre **MAPIUID** pour chaque ouverture de session. Inscription des structures **MAPIUID** uniques permet de MAPI router correctement les demandes à l’instance de fournisseur approprié. Toutefois, vous souhaiterez peut-être ont tous les objets d’ouverture de session de partager un **MAPIUID**. Dans ce cas, vous devez être en mesure de gérer le routage vous-même au lieu de s’appuyer sur MAPI. Pour plus d’informations sur la création d’un **MAPIUID**, voir [Inscription des identificateurs uniques Service fournisseur](registering-service-provider-unique-identifiers.md).
  
L’objet de prise en charge MAPI transmet à votre méthode **d’ouverture de session** dans le paramètre _lpMAPISup_ fournit l’accès à de nombreuses méthodes inclus dans le [IMAPISupport : IUnknown](imapisupportiunknown.md) interface. MAPI crée un objet de prise en charge qui est adapté à votre type de fournisseur. Par exemple, si vous avez besoin pour vous connecter à un système de messagerie sous-jacent ou le service d’annuaire lorsque vous établissez une connexion, vous pouvez appeler la méthode [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) pour récupérer les informations d’identification de sécurité pour cette session particulière. 
  
Si **l’ouverture de session** réussit, assurez-vous que vous appelez la méthode [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) de l’objet de la prise en charge pour incrémenter son décompte de références. Cela permet à votre fournisseur de conserver le pointeur d’objet prise en charge pour le reste de la session. Si vous n’appelez pas cette méthode **AddRef** , MAPI décharge votre fournisseur. 
  
Vous pouvez inclure le nom de profil transmis dans le paramètre _lpszProfileName_ dans les boîtes de dialogue d’erreur, écrans d’ouverture de session ou autres interfaces utilisateur. Pour utiliser le nom de profil, copiez-le vers un stockage que vous avez alloué. 
  
Créer un objet d’ouverture de session et d’y revenir un pointeur dans le paramètre _lppABLogon_ . MAPI utilise cet objet d’ouverture de session pour effectuer des appels aux méthodes dans votre implémentation [IABLogon](iablogoniunknown.md) . 
  
Si vous avez besoin d’un mot de passe au cours de l’ouverture de session, afficher une boîte de dialogue d’ouverture de session uniquement si l’indicateur AB_NO_DIALOG n’est pas définie. Si l’utilisateur annule le processus d’ouverture de session, généralement retourner MAPI_E_USER_CANCEL en cliquant sur le bouton **Annuler** dans la boîte de dialogue **d’ouverture de session**.
  
En règle générale, lorsqu’un fournisseur de carnet d’adresses ne peut pas se connecter, MAPI désactive le service de message à laquelle appartient le fournisseur défectueux — autrement dit, MAPI n’essaie pas d’établir des connexions pour tous les autres fournisseurs qui appartiennent au service pour le reste de la session durée de vie. Cependant, si votre fournisseur ne peut pas établir une connexion et que vous souhaitez ne pas désactiver le service entier, renvoie une référence à MAPI_E_FAILONEPROVIDER ou MAPI_E_UNCONFIGURED. MAPI ne désactive pas le service de message à laquelle appartient le fournisseur. 
  
Retour référence à MAPI_E_FAILONEPROVIDER si une erreur produit qui n’est pas suffisamment grave pour empêcher les autres fournisseurs dans le service de message d’établir des connexions. Retourner MAPI_E_UNCONFIGURED si les informations de configuration nécessaires sont absents du profil et vous ne pouvez pas afficher une boîte de dialogue pour inviter l’utilisateur. MAPI répond en fonction de point d’entrée de votre fournisseur message service MSG_SERVICE_CONFIGURE pourvue l’appel en tant que paramètre _ulContext_ pour donner la possibilité de configurer lui-même, soit par programme le service ou à l’aide d’une feuille de propriétés. Lorsque le message service point d’entrée fonction est terminé, MAPI réessayer l’ouverture de session. 
  
## <a name="see-also"></a>Voir aussi



[IABLogon::Logoff](iablogon-logoff.md)
  
[IABLogon::OpenEntry](iablogon-openentry.md)
  
[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)
  
[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IABProvider : IUnknown](iabprovideriunknown.md)

