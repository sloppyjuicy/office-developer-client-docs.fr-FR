---
title: IMAPISessionSetDefaultStore
description: IMAPISessionSetDefaultStore établit un magasin de messages comme magasin de messages par défaut pour la session.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISession.SetDefaultStore
api_type:
- COM
ms.assetid: 456c207f-5d41-4d0c-94b6-0c58893a6bed
ms.openlocfilehash: e73453c97dd4204d1c8ca6fd8094bd063ad46667
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65827925"
---
# <a name="imapisessionsetdefaultstore"></a>IMAPISession::SetDefaultStore

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Établit un magasin de messages comme magasin de messages par défaut pour la session.
  
```cpp
HRESULT SetDefaultStore(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôle le paramètre du magasin de messages par défaut. Ces indicateurs s’excluent mutuellement; un seul des indicateurs suivants peut être défini :
    
MAPI_DEFAULT_STORE
  
> Établit le magasin de messages comme valeur par défaut de session. Met à jour la ligne de table d’état du magasin de messages en définissant l’indicateur STATUS_DEFAULT_STORE dans la colonne **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
    
MAPI_PRIMARY_STORE
  
> Établit le magasin de messages comme magasin à utiliser à l’ouverture de session. Si le magasin de messages n’est pas le magasin par défaut, les clients doivent en faire la valeur par défaut. Met à jour la ligne de la table d’état du magasin de messages en définissant l’indicateur de STATUS_PRIMARY_STORE dans la colonne **PR_RESOURCE_FLAGS** . 
    
MAPI_SECONDARY_STORE
  
> Établit le magasin de messages comme magasin à utiliser à l’ouverture de session si le magasin de messages principal n’est pas disponible. Si un client ne peut pas ouvrir le magasin principal, il doit ouvrir le magasin secondaire et le définir comme valeur par défaut. Met à jour la ligne de la table d’état du magasin de messages en définissant l’indicateur de STATUS_SECONDARY_STORE dans la colonne **PR_RESOURCE_FLAGS** . 
    
MAPI_SIMPLE_STORE_PERMANENT
  
> Définit l’indicateur STATUS_SIMPLE_STORE dans la propriété **PR_RESOURCE_FLAGS** du magasin de messages dans sa ligne de table d’état, sa ligne de table du magasin de messages et dans le profil de session. 
    
MAPI_SIMPLE_STORE_TEMPORARY
  
> Définit l’indicateur STATUS_SIMPLE_STORE dans la propriété **PR_RESOURCE_FLAGS** du magasin de messages dans la ligne de la table d’état et la ligne de la table du magasin de messages. Le profil n’est pas modifié. 
    
 _cbEntryID_
  
> [in] Nombre d’octets dans l’identificateur d’entrée pointé par le paramètre  _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée du magasin de messages qui est prévu comme valeur par défaut. Si un client passe NULL dans  _lpEntryID_, aucun magasin de messages n’est sélectionné comme valeur par défaut.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi et retourné la valeur ou les valeurs attendues.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISession::SetDefaultStore** établit un magasin de messages comme l’un des éléments suivants : 
  
- Magasin de messages par défaut pour la session.
    
- Magasin de messages principal pour la session.
    
- Magasin de messages secondaire pour la session.
    
Pour définir un magasin de messages comme magasin de messages par défaut, les indicateurs suivants doivent être définis dans sa propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) :
  
- STORE_SUBMIT_OK
    
- STORE_CREATE_OK
    
- STORE_MODIFY_OK
    
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous pouvez déterminer le magasin de messages par défaut pour la session en récupérant la table d’état et en recherchant le paramètre de l’indicateur STATUS_DEFAULT_STORE dans la colonne **PR_RESOURCE_FLAGS** . La ligne qui a ce paramètre représente le magasin de messages désigné comme valeur par défaut de session. 
  
Lorsque l’indicateur MAPI_DEFAULT_STORE ou MAPI_SIMPLE_STORE_PERMANENT est défini, MAPI met à jour le profil, la table du magasin de messages et la table d’état. 
  
Chaque fois qu’une modification est apportée au paramètre par défaut du magasin de messages, les notifications suivantes sont générées :
  
- Une notification d’événement **fnevTableModified** est émise pour chaque ligne affectée dans le magasin de messages et la table d’état. 
    
- Une notification interne est émise au spouleur MAPI. Les opérations déjà en cours sont terminées sans modification; Les nouvelles opérations qui impliquent le magasin de messages par défaut, comme le téléchargement de messages, sont traitées pour le nouveau magasin par défaut.
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnSetDefaultStore  <br/> |MFCMAPI utilise la méthode **IMAPISession::SetDefaultStore** pour définir le magasin sélectionné comme magasin par défaut. |
   
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagResourceFlags](pidtagresourceflags-canonical-property.md)
  
[Propriété canonique PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

