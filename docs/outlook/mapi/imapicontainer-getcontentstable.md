---
title: IMAPIContainerGetContentsTable
description: IMAPIContainerGetContentsTable retourne un pointeur vers la table de contenu du conteneur. Cet article décrit sa syntaxe, ses paramètres, sa valeur de retour et ses remarques.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIContainer.GetContentsTable
api_type:
- COM
ms.assetid: 88c7a666-875d-473a-b126-dbbb7009f7d9
ms.openlocfilehash: 8ed6524f92b05b2f2bfd1e3d3736df73289e1177
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817262"
---
# <a name="imapicontainergetcontentstable"></a>IMAPIContainer::GetContentsTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Retourne un pointeur vers la table du contenu du conteneur.
  
```cpp
HRESULT GetContentsTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôle la façon dont la table des matières est retournée. Les indicateurs suivants peuvent être définis :
    
MAPI_ASSOCIATED 
  
> La table de contenu associée du conteneur doit être retournée à la place de la table des matières standard. Cet indicateur est utilisé uniquement avec les dossiers. Les messages inclus dans la table des matières associée ont été créés avec l’indicateur MAPI_ASSOCIATED défini dans l’appel à la méthode [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) . Les clients utilisent généralement la table des matières associée pour récupérer des formulaires, des vues et d’autres messages masqués. 
    
ACLTABLE_FREEBUSY
  
> Active l’accès aux droits frightsFreeBusySimple et frightsFreeBusyDetailed dans **PR_MEMBER_RIGHTS**.
    
MAPI_DEFERRED_ERRORS 
  
> **GetContentsTable** peut retourner correctement, éventuellement avant que la table ne soit mise à la disposition de l’appelant. Si la table n’est pas disponible, l’exécution d’un appel de table ultérieur peut générer une erreur. 
    
MAPI_UNICODE 
  
> Demande que les colonnes qui contiennent des données de chaîne soient retournées au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas défini, les chaînes doivent être retournées au format ANSI. 
    
SHOW_SOFT_DELETES
  
> Affiche les éléments actuellement marqués comme supprimés de manière réversible, c’est-à-dire qu’ils sont dans la phase de durée de rétention des éléments supprimés.
    
 _lppTable_
  
> [out] Pointeur vers un pointeur vers la table des matières.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La table du contenu a été récupérée avec succès.
    
MAPI_E_BAD_CHARWIDTH 
  
> Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, soit MAPI_UNICODE n’a pas été défini et l’implémentation prend uniquement en charge Unicode.
    
MAPI_E_NO_SUPPORT 
  
> Le conteneur n’a pas de contenu et ne peut pas fournir de table des matières.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIContainer::GetContentsTable** retourne un pointeur vers la table de contenu d’un conteneur. Une table de contenu contient des informations récapitulatives sur les objets du conteneur. 
  
Les tables de contenu ont des ensembles de colonnes longs. Pour obtenir la liste complète des colonnes requises et facultatives dans les tables de contenu, consultez [Tables de contenu](contents-tables.md). 
  
Il est possible que certains conteneurs n’aient pas de contenu. Ces conteneurs retournent MAPI_E_NO_SUPPORT de leurs implémentations de **GetContentsTable**.
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Si vous prenez en charge une table de contenu pour votre conteneur, vous devez également effectuer les opérations suivantes :
  
- Prise en charge des appels à la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) du conteneur pour ouvrir la propriété **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)).
    
- Retourner **PR_CONTAINER_CONTENTS** en réponse à un appel à la 
    
    [Méthodes IMAPIProp::GetProps](imapiprop-getprops.md) et [IMAPIProp::GetPropList](imapiprop-getproplist.md) . 
    
L’implémentation de cette méthode par un fournisseur de transport distant doit retourner un pointeur vers une interface [IMAPITable : IUnknown](imapitableiunknown.md) dans le paramètre _ppTable_ passé dans la méthode **GetContentsTable** . Si votre fournisseur de transport dispose d’une table de contenu existante, il suffit de retourner un pointeur vers celui-ci. Si ce n’est pas le cas, cette méthode doit créer un objet [IMAPITable : IUnknown](imapitableiunknown.md) , remplir la table avec des en-têtes de message (le cas échéant) et retourner un pointeur vers la nouvelle table. La méthode [ITableData::HrGetView](itabledata-hrgetview.md) est utile pour générer une valeur de retour et stocker le pointeur de table dans le paramètre _ppTable_ . La table des matières doit au moins contenir les colonnes de propriétés suivantes : 
  
- **PR_ENTRYID** ([PidTagEntryID](pidtagentryid-canonical-property.md))
    
- **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))
    
- **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))
    
- **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))
    
- **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))
    
- **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))
    
- **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))
    
- **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))
    
- **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))
    
- **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))
    
- **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))
    
- **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))
    
- **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))
    
- **PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))
    
- **PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))
    
## <a name="notes-to-callers"></a>Remarques pour les appelants

Les colonnes de table de contenu binaire et de chaîne peuvent être tronquées. En règle générale, les fournisseurs retournent 255 caractères. Étant donné que vous ne pouvez pas savoir au préalable si une table inclut des colonnes tronquées, supposons qu’une colonne est tronquée si la longueur de la colonne est de 255 ou 510 octets. Vous pouvez toujours récupérer la valeur complète d’une colonne tronquée, si nécessaire, directement à partir de l’objet en utilisant son identificateur d’entrée pour l’ouvrir, puis en appelant la méthode **IMAPIProp::GetProps** . 
  
Selon l’implémentation du fournisseur, les restrictions et les opérations de tri peuvent s’appliquer à l’ensemble d’une chaîne ou à la version tronquée de cette chaîne.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableDialog.cpp  <br/> |CContentsTableDlg::CContentsTableDlg  <br/> |La classe **CContentsTableDlg** utilise **GetContentsTable** pour obtenir les entrées d’une table de contenu. |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[Propriété canonique PidTagContainerContents](pidtagcontainercontents-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

