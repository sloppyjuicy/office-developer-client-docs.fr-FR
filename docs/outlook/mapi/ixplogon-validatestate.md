---
title: IXPLogonValidateState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.ValidateState
api_type:
- COM
ms.assetid: c3649daa-cba1-48e3-9ffb-069c1bcf8228
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 4fd0dd02c5cf6f6a49b782d06c02e373dcfc3327
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577484"
---
# <a name="ixplogonvalidatestate"></a>IXPLogon::ValidateState

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Vérifie l’état externe du fournisseur de transport. 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _ulUIParam_
  
> [in] Handle vers la fenêtre parente de toutes les boîtes de dialogue ou windows qui affiche cette méthode.
    
 _ulFlags_
  
> [in] Un masque de bits d’indicateurs qui contrôlent la façon dont le contrôle d’état est effectué et les résultats de la vérification du statut. Les indicateurs suivants peuvent être définis :
    
ABORT_XP_HEADER_OPERATION 
  
> L’utilisateur a annulé l’opération de généralement en cliquant sur le bouton **Annuler** dans une boîte de dialogue. Le fournisseur de transport a la possibilité de continuer à travailler sur l’opération, ou elle peut annuler l’opération et retourner des MAPI_E_USER_CANCELED. 
    
CONFIG_CHANGED 
  
> Valide l’état des fournisseurs de transport actuellement chargés en entraînant le spouleur MAPI appeler leur méthode [IXPLogon::AddressTypes](ixplogon-addresstypes.md) . Cet indicateur permet également le spouleur MAPI pour corriger les échecs de fournisseur de transport critique sans forcer les applications clientes et déconnectez-vous puis reconnectez-vous. 
    
FORCE_XP_CONNECT 
  
> L’utilisateur a sélectionné une opération de connexion. Lorsque cet indicateur est utilisé avec l’indicateur REFRESH_XP_HEADER_CACHE ou PROCESS_XP_HEADER_CACHE, l’action de connexion se produit sans mise en cache.
    
FORCE_XP_DISCONNECT 
  
> L’utilisateur a sélectionné une opération de déconnexion. Lorsque cet indicateur est utilisé avec REFRESH_XP_HEADER_CACHE ou PROCESS_XP_HEADER_CACHE, l’action de déconnexion se produit sans mise en cache.
    
PROCESS_XP_HEADER_CACHE 
  
> Entrées de la table de cache d’en-tête doivent être traitées, tous les messages marqués avec l’indicateur MSGSTATUS_REMOTE_DOWNLOAD doivent être téléchargés et tous les messages marqués avec l’indicateur MSGSTATUS_REMOTE_DELETE doivent être supprimés. Messages MSGSTATUS_REMOTE_DOWNLOAD et MSGSTATUS_REMOTE_DELETE la valeur doivent être déplacés.
    
REFRESH_XP_HEADER_CACHE 
  
> Une nouvelle liste d’en-têtes de message doit être téléchargée et statut du message tous les indicateurs de marquage doit être effacé.
    
SUPPRESS_UI 
  
> Le fournisseur de transport empêche l’affichage d’une interface utilisateur.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’appel a réussi et renvoyé la valeur attendue ou les valeurs.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours ; Il doit être autorisé pour effectuer, ou il doit être arrêté avant cette opération est tentée.
    
MAPI_E_NO_SUPPORT 
  
> Le fournisseur de transport à distance impliqué ne prend pas en charge une interface utilisateur et l’application cliente elle-même doit afficher la boîte de dialogue.
    
MAPI_E_USER_CANCEL 
  
> L’utilisateur a annulé l’opération de généralement en cliquant sur le bouton **Annuler** dans une boîte de dialogue. 
    
## <a name="remarks"></a>Remarques

Le spouleur MAPI appelle la méthode **IXPLogon::ValidateState** pour prendre en charge des appels à la méthode [IMAPIStatus::ValidateState](imapistatus-validatestate.md) pour l’objet d’état. Le fournisseur de transport doit répondre à l’appel **IXPLogon::ValidateState** exactement comme si le spouleur MAPI avait ouvert un objet d’état pour la session en cours et ensuite appelée **IMAPIStatus::ValidateState** sur cet objet. 
  
Pour prendre en charge son implémentation de **IMAPIStatus::ValidateState**, le spouleur MAPI appelle **IXPLogon::ValidateState** sur tous les objets d’ouverture de session pour tous les fournisseurs de transport actif qui sont en cours d’exécution dans une session de profil. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

