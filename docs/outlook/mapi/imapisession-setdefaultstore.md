---
title: IMAPISessionSetDefaultStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.SetDefaultStore
api_type:
- COM
ms.assetid: 456c207f-5d41-4d0c-94b6-0c58893a6bed
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f4ff2a3897306ebe4f77c08630782c5f2c7d5d3d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426106"
---
# <a name="imapisessionsetdefaultstore"></a>IMAPISession::SetDefaultStore

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Établit une banque de messages comme banque de messages par défaut pour la session.
  
```cpp
HRESULT SetDefaultStore(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> dans Masque de réinitialisation des indicateurs qui contrôle le paramètre de la Banque de messages par défaut. Ces indicateurs s'excluent mutuellement; un seul des indicateurs suivants peut être défini:
    
MAPI_DEFAULT_STORE
  
> Établit la Banque de messages comme valeur par défaut de la session. Met à jour la ligne de table d'État du magasin de messages en définissant l'indicateur STATUS_DEFAULT_STORE dans la colonne **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
    
MAPI_PRIMARY_STORE
  
> Établit la Banque de messages comme banque à utiliser lors de l'ouverture de session. S'il ne s'agit pas de la Banque de messages par défaut, les clients doivent le définir comme valeur par défaut. Met à jour la ligne de table d'État du magasin de messages en définissant l'indicateur STATUS_PRIMARY_STORE dans la colonne **PR_RESOURCE_FLAGS** . 
    
MAPI_SECONDARY_STORE
  
> Définit la Banque de messages comme banque à utiliser lors de l'ouverture de session si elle n'est pas disponible. Si un client ne peut pas ouvrir le magasin principal, il doit ouvrir le magasin secondaire et le définir par défaut. Met à jour la ligne de table d'État du magasin de messages en définissant l'indicateur STATUS_SECONDARY_STORE dans la colonne **PR_RESOURCE_FLAGS** . 
    
MAPI_SIMPLE_STORE_PERMANENT
  
> Définit l'indicateur STATUS_SIMPLE_STORE dans la propriété **PR_RESOURCE_FLAGS** de la Banque de messages dans sa ligne de table d'État, sa ligne de table de magasin de messages et le profil de session. 
    
MAPI_SIMPLE_STORE_TEMPORARY
  
> Définit l'indicateur STATUS_SIMPLE_STORE dans la propriété **PR_RESOURCE_FLAGS** de la Banque de messages dans sa ligne de table d'État et sa ligne de table de magasin de messages. Le profil n'est pas modifié. 
    
 _cbEntryID_
  
> dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> dans Pointeur vers l'identificateur d'entrée de la Banque de messages qui est conçue comme valeur par défaut. Si un client transmet la valeur NULL dans _lpEntryID_, aucune banque de messages n'est sélectionnée par défaut.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a réussi et a renvoyé la ou les valeurs attendues.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISession:: SetDefaultStore** établit une banque de messages de l'une des manières suivantes: 
  
- Banque de messages par défaut pour la session.
    
- Banque de messages principale de la session.
    
- Banque de messages secondaire pour la session.
    
Pour établir une banque de messages par défaut, les indicateurs suivants doivent être définis dans la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) de la Banque de messages:
  
- STORE_SUBMIT_OK
    
- STORE_CREATE_OK
    
- STORE_MODIFY_OK
    
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous pouvez déterminer la Banque de messages par défaut pour la session en récupérant la table d'État et en recherchant le paramètre de l'indicateur STATUS_DEFAULT_STORE dans la colonne **PR_RESOURCE_FLAGS** . La ligne qui contient ce paramètre représente la Banque de messages désignée comme session par défaut. 
  
Lorsque l'indicateur MAPI_DEFAULT_STORE ou MAPI_SIMPLE_STORE_PERMANENT est défini, MAPI met à jour le profil, la table de banque de messages et la table d'État. 
  
Chaque fois qu'une modification est apportée au paramètre par défaut de la Banque de messages, les notifications suivantes sont générées:
  
- Une notification d'événement **fnevTableModified** est émise pour chaque ligne concernée dans la Banque de messages et le tableau d'État. 
    
- Une notification interne est émise pour le spouleur MAPI. Les opérations déjà en cours sont effectuées sans modification; les nouvelles opérations qui impliquent la Banque de messages par défaut, telles que le téléchargement de messages, sont traitées pour le nouveau magasin par défaut.
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MainDlg. cpp  <br/> |CMainDlg:: OnSetDefaultStore  <br/> |MFCMAPI utilise la méthode **IMAPISession:: SetDefaultStore** pour définir la Banque sélectionnée comme banque par défaut.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagResourceFlags](pidtagresourceflags-canonical-property.md)
  
[Propriété canonique PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

