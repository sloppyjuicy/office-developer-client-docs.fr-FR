---
title: IXPLogonValidateState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IXPLogon.ValidateState
api_type:
- COM
ms.assetid: c3649daa-cba1-48e3-9ffb-069c1bcf8228
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 4da8ae8d05a06c6e377d48a42298e74724674d5e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561305"
---
# <a name="ixplogonvalidatestate"></a>IXPLogon::ValidateState

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Vérifie l’état externe du fournisseur de transport. 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _ulUIParam_
  
> [in] Poignée vers la fenêtre parente de toutes les boîtes de dialogue ou fenêtres affichées par cette méthode.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont la vérification d’état est effectuée et les résultats de la vérification d’état. Les indicateurs suivants peuvent être définies :
    
ABORT_XP_HEADER_OPERATION 
  
> L’utilisateur a annulé l’opération, généralement en cliquant sur le bouton **Annuler** dans une boîte de dialogue. Le fournisseur de transport a la possibilité de continuer à travailler sur l’opération, ou il peut abandonner l’opération et retourner MAPI_E_USER_CANCELED. 
    
CONFIG_CHANGED 
  
> Valide l’état des fournisseurs de transport actuellement chargés en faisant appel à leur méthode [IXPLogon::AddressTypes](ixplogon-addresstypes.md) par lepooler MAPI. Cet indicateur permet également aupooler MAPI de corriger les défaillances critiques du fournisseur de transport sans forcer les applications clientes à se déconnecter, puis à se connecter à nouveau. 
    
FORCE_XP_CONNECT 
  
> L’utilisateur a sélectionné une opération de connexion. Lorsque cet indicateur est utilisé avec l’REFRESH_XP_HEADER_CACHE ou PROCESS_XP_HEADER_CACHE, l’action de connexion se produit sans mise en cache.
    
FORCE_XP_DISCONNECT 
  
> L’utilisateur a sélectionné une opération de déconnexion. Lorsque cet indicateur est utilisé avec REFRESH_XP_HEADER_CACHE ou PROCESS_XP_HEADER_CACHE, l’action de déconnexion se produit sans mise en cache.
    
PROCESS_XP_HEADER_CACHE 
  
> Les entrées de la table de cache d’en-tête doivent être traitées, tous les messages marqués avec l’indicateur MSGSTATUS_REMOTE_DOWNLOAD doivent être téléchargés et tous les messages marqués avec l’indicateur MSGSTATUS_REMOTE_DELETE doivent être supprimés. Les messages dont la MSGSTATUS_REMOTE_DOWNLOAD et MSGSTATUS_REMOTE_DELETE sont définies doivent être déplacés.
    
REFRESH_XP_HEADER_CACHE 
  
> Une nouvelle liste d’en-têtes de message doit être téléchargée et tous les indicateurs de marquage d’état des messages doivent être effacés.
    
SUPPRESS_UI 
  
> Empêche le fournisseur de transport d’afficher une interface utilisateur.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi et a renvoyé la ou les valeurs attendues.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours ; Il doit être autorisé à se terminer ou arrêté avant la tentative de cette opération.
    
MAPI_E_NO_SUPPORT 
  
> Le fournisseur de transport distant impliqué ne prend pas en charge l’interface utilisateur et l’application cliente elle-même doit afficher la boîte de dialogue.
    
MAPI_E_USER_CANCEL 
  
> L’utilisateur a annulé l’opération, généralement en cliquant sur le bouton **Annuler** dans une boîte de dialogue. 
    
## <a name="remarks"></a>Remarques

Lepooler MAPI appelle la méthode **IXPLogon::ValidateState** pour prendre en charge les appels à la méthode [IMAPIStatus::ValidateState](imapistatus-validatestate.md) pour l’objet d’état. Le fournisseur de transport doit répondre à l’appel **IXPLogon::ValidateState** exactement comme si lepooler MAPI avait ouvert un objet d’état pour la session d’ouverture de session en cours, puis appelé **IMAPIStatus::ValidateState** sur cet objet. 
  
Pour prendre en charge son implémentation **d’IMAPIStatus::ValidateState,** lepooler MAPI appelle **IXPLogon::ValidateState** sur tous les objets d’ouverture de session pour tous les fournisseurs de transport actifs qui s’exécutent dans une session de profil. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

