---
title: IMAPISessionSetDefaultStore
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d5ff92222b91c7ab22f73d6e4714cda110ae69fe
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62776458"
---
# <a name="imapisessionsetdefaultstore"></a>IMAPISession::SetDefaultStore

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Établit une magasin de messages comme magasin de messages par défaut pour la session.
  
```cpp
HRESULT SetDefaultStore(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le paramètre de la magasin de messages par défaut. Ces indicateurs s’excluent mutuellement ; Vous ne pouvez définir qu’un seul des indicateurs suivants :
    
MAPI_DEFAULT_STORE
  
> Établit la magasin de messages comme la session par défaut. Met à jour la ligne de table d’état de la boutique de messages en STATUS_DEFAULT_STORE l’indicateur **PR_RESOURCE_FLAGS (**[PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
    
MAPI_PRIMARY_STORE
  
> Établit la boutique de messages en tant que magasin à utiliser lors de l’ouverture de ouverture de ouverture de ligne. Si la magasin de messages n’est pas la boutique par défaut, les clients doivent en faire la valeur par défaut. Met à jour la ligne de table d’état de la boutique de messages en STATUS_PRIMARY_STORE **l’indicateur** de PR_RESOURCE_FLAGS colonne. 
    
MAPI_SECONDARY_STORE
  
> Établit la magasin de messages en tant que magasin à utiliser lors de l’ouverture de ouverture de ouverture des de marché si la boutique de messages principale n’est pas disponible. Si un client ne peut pas ouvrir le magasin principal, il doit ouvrir le magasin secondaire et le définir comme magasin par défaut. Met à jour la ligne de table d’état de la boutique de messages en STATUS_SECONDARY_STORE **l’indicateur** PR_RESOURCE_FLAGS colonne. 
    
MAPI_SIMPLE_STORE_PERMANENT
  
> Définit l’STATUS_SIMPLE_STORE dans la propriété PR_RESOURCE_FLAGS de la boutique de  messages dans sa ligne de table d’état, la ligne de table de la boutique de messages et dans le profil de session. 
    
MAPI_SIMPLE_STORE_TEMPORARY
  
> Définit l’STATUS_SIMPLE_STORE dans la propriété PR_RESOURCE_FLAGS de la boutique de messages dans **la** ligne de table d’état et la ligne de table de la boutique de messages. Le profil n’est pas modifié. 
    
 _cbEntryID_
  
> [in] Nombre d’bytes dans l’identificateur d’entrée pointé par  _le paramètre lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée de la magasin de messages prévu comme valeur par défaut. Si un client transmet la valeur NULL dans  _lpEntryID_, aucune magasine de messages n’est sélectionnée par défaut.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi et a renvoyé la ou les valeurs attendues.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISession::SetDefaultStore** établit une magasin de messages comme l’une des suivantes : 
  
- Magasin de messages par défaut pour la session.
    
- Magasin de messages principal pour la session.
    
- Magasin de messages secondaire pour la session.
    
Pour établir une magasin de messages comme magasin de messages par défaut, les indicateurs suivants doivent être définies dans sa propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) :
  
- STORE_SUBMIT_OK
    
- STORE_CREATE_OK
    
- STORE_MODIFY_OK
    
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous pouvez déterminer la magasin de messages par défaut pour la session en récupérant la table d’état et en recherchant le paramètre de l’indicateur STATUS_DEFAULT_STORE dans la **colonne PR_RESOURCE_FLAGS** . La ligne qui possède ce paramètre représente la magasin de messages désignée comme session par défaut. 
  
Lorsque l’MAPI_DEFAULT_STORE ou l’indicateur MAPI_SIMPLE_STORE_PERMANENT est définie, MAPI met à jour le profil, la table de la boutique de messages et la table d’état. 
  
Chaque fois qu’une modification est apporté au paramètre par défaut de la boutique de messages, les notifications suivantes sont générées :
  
- Une notification **d’événement fnevTableModified** est émise pour chaque ligne concernée dans la table d’état et la magasin de messages. 
    
- Une notification interne est émise aupooler MAPI. Les opérations en cours sont terminées sans modification . les nouvelles opérations qui impliquent la magasin de messages par défaut, telles que le téléchargement des messages, sont traitées pour la nouvelle boutique par défaut.
    
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

