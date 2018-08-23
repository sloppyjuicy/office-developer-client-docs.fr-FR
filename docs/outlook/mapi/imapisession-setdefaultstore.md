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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: c7eda7089515942cb38a941bab863b3adf971bdc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587844"
---
# <a name="imapisessionsetdefaultstore"></a>IMAPISession::SetDefaultStore

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Établissement d’une banque de messages comme banque de messages par défaut pour la session.
  
```cpp
HRESULT SetDefaultStore(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le paramétrage de la banque de messages par défaut. Ces indicateurs sont mutuellement ; peut être défini qu’un seul des indicateurs suivants :
    
MAPI_DEFAULT_STORE
  
> Établit la banque de messages en tant que la valeur par défaut de la session. Met à jour la ligne de tableau d’état de la banque de messages en définissant l’indicateur STATUS_DEFAULT_STORE dans la colonne **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
    
MAPI_PRIMARY_STORE
  
> Définit la banque de messages comme le magasin à utiliser lors de la connexion. Si la banque de messages n’est pas la banque par défaut, les clients doivent rendre la valeur par défaut. Met à jour la ligne de tableau d’état de la banque de messages en définissant l’indicateur STATUS_PRIMARY_STORE dans la colonne **PR_RESOURCE_FLAGS** . 
    
MAPI_SECONDARY_STORE
  
> Définit la banque de messages comme le magasin à utiliser lors de la connexion si la banque de messages principale n’est pas disponible. Si un client ne peut pas ouvrir la banque principale, il doit ouvrir le stockage secondaire et le définir en tant que la valeur par défaut. Met à jour la ligne de tableau d’état de la banque de messages en définissant l’indicateur STATUS_SECONDARY_STORE dans la colonne **PR_RESOURCE_FLAGS** . 
    
MAPI_SIMPLE_STORE_PERMANENT
  
> Définit l’indicateur STATUS_SIMPLE_STORE dans **PR_RESOURCE_FLAGS** propriété du magasin message dans sa ligne de tableau d’état, ligne du tableau de magasin de message, dans le profil de la session. 
    
MAPI_SIMPLE_STORE_TEMPORARY
  
> Définit l’indicateur STATUS_SIMPLE_STORE dans la propriété **PR_RESOURCE_FLAGS** de la banque messages dans sa ligne tableau d’état et la ligne de tableau de magasin de message. Le profil n’est pas modifié. 
    
 _cbEntryID_
  
> [in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée de la banque de messages est destiné à la valeur par défaut. Si un client passe _lpEntryID_NULL, aucune banque de messages n’est activée par défaut.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’appel a réussi et renvoyé la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISession::SetDefaultStore** établit une banque de messages comme une des options suivantes : 
  
- La banque de messages par défaut pour la session.
    
- La banque de messages principale pour la session.
    
- Le magasin de message secondaire pour la session.
    
Pour établir une banque de messages par défaut, la banque de messages doit avoir les indicateurs suivants définis dans sa propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) :
  
- STORE_SUBMIT_OK
    
- STORE_CREATE_OK
    
- STORE_MODIFY_OK
    
## <a name="notes-to-callers"></a>Notes aux appelants

Vous pouvez déterminer la banque de messages par défaut pour la session en récupérant la table d’état et en recherchant la valeur de l’indicateur STATUS_DEFAULT_STORE dans la colonne **PR_RESOURCE_FLAGS** . La ligne qui possède ce paramètre représente la banque de messages est désignée comme la valeur par défaut de la session. 
  
Lorsque la MAPI_DEFAULT_STORE ou l’indicateur MAPI_SIMPLE_STORE_PERMANENT est défini, MAPI met à jour le profil, table banque de messages et table d’état. 
  
Chaque fois qu’une modification est apportée à la valeur par défaut de banque de messages, les notifications suivantes sont générées :
  
- Une notification d’événement **fnevTableModified** est émise pour chaque ligne concernée dans les deux le magasin et l’état de la table de messages. 
    
- Une notification interne est émise au spouleur MAPI. Déjà en cours sont effectuées sans modification ; nouvelles opérations qui impliquent la banque de messages par défaut, telles que le téléchargement de message, sont traitées de la nouvelle banque par défaut.
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnSetDefaultStore  <br/> |MFCMAPI utilise la méthode **IMAPISession::SetDefaultStore** pour définir le magasin sélectionné en tant que la banque par défaut.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagResourceFlags](pidtagresourceflags-canonical-property.md)
  
[Propriété canonique PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

