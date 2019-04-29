---
title: IMAPIContainerGetContentsTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.GetContentsTable
api_type:
- COM
ms.assetid: 88c7a666-875d-473a-b126-dbbb7009f7d9
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 28315c5a09eba32816a0b63513cb98d1c30a96bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431105"
---
# <a name="imapicontainergetcontentstable"></a>IMAPIContainer::GetContentsTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie un pointeur vers la table des matières du conteneur.
  
```cpp
HRESULT GetContentsTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle la manière dont la table des matières est renvoyée. Les indicateurs suivants peuvent être définis:
    
MAPI_ASSOCIATED 
  
> La table des matières associée du conteneur doit être renvoyée à la place de la table des matières standard. Cet indicateur est utilisé uniquement avec les dossiers. Les messages qui sont inclus dans la table des matières associée ont été créés avec l'indicateur MAPI_ASSOCIATED défini dans l'appel à la méthode [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) . Les clients utilisent généralement le tableau contenu associé pour récupérer des formulaires, des vues et d'autres messages masqués. 
    
ACLTABLE_FREEBUSY
  
> Permet l'accès aux droits frightsFreeBusySimple et frightsFreeBusyDetailed dans **PR_MEMBER_RIGHTS**.
    
MAPI_DEFERRED_ERRORS 
  
> **GetContentsTable** peut être renvoyé correctement, éventuellement avant que la table soit mise à la disposition de l'appelant. Si la table n'est pas disponible, un appel de tableau ultérieur peut déclencher une erreur. 
    
MAPI_UNICODE 
  
> Demande que les colonnes qui contiennent des données de chaîne soient renvoyées au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes doivent être renvoyées au format ANSI. 
    
SHOW_SOFT_DELETES
  
> Affiche les éléments qui sont actuellement marqués comme étant supprimés de manière récupérable, c'est-à-dire qu'ils se trouvent dans la phase de durée de rétention des éléments supprimés.
    
 _lppTable_
  
> remarquer Pointeur vers un pointeur vers la table des matières.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La table de contenu a été récupérée avec succès.
    
MAPI_E_BAD_CHARWIDTH 
  
> L'indicateur MAPI_UNICODE a été défini et l'implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n'a pas été défini et l'implémentation prend en charge uniquement Unicode.
    
MAPI_E_NO_SUPPORT 
  
> Le conteneur n'a pas de contenu et ne peut pas fournir de table des matières.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIContainer:: GetContentsTable** renvoie un pointeur vers la table de contenu d'un conteneur. Une table des matières contient des informations récapitulatives sur les objets dans le conteneur. 
  
Les tables de contenu comportent des ensembles de colonnes de longue durée. Pour obtenir la liste complète des colonnes obligatoires et facultatives dans les tables de contenu, voir [content tables](contents-tables.md). 
  
Il est possible que certains conteneurs n'aient pas de contenu. Ces conteneurs renvoient MAPI_E_NO_SUPPORT à partir de leurs implémentations de **GetContentsTable**.
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Si vous prenez en charge une table des matières pour votre conteneur, vous devez également effectuer les opérations suivantes:
  
- Prendre en charge les appels à la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) du conteneur pour ouvrir la propriété **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)).
    
- Renvoyer **PR_CONTAINER_CONTENTS** en réponse à un appel au conteneur 
    
    [IMAPIProp:: GetProps](imapiprop-getprops.md) et [IMAPIProp:: GetPropList](imapiprop-getproplist.md) méthodes. 
    
L'implémentation d'un fournisseur de transport distant de cette méthode doit renvoyer un pointeur vers une interface [IMAPITable: IUnknown](imapitableiunknown.md) dans le paramètre _ppTable_ transmis à la méthode **GetContentsTable** . Si votre fournisseur de transport dispose d'un tableau de contenu existant, il suffit de renvoyer un pointeur vers celui-ci. Si ce n'est pas le cas, cette méthode doit créer un nouvel [IMAPITable: objet IUnknown](imapitableiunknown.md) , remplir le tableau avec des en-têtes de message (le cas échéant) et renvoyer un pointeur vers le nouveau tableau. La méthode [ITableData:: HrGetView](itabledata-hrgetview.md) est utile pour générer une valeur de retour et stocker le pointeur de table dans le paramètre _ppTable_ . La table de contenu doit prendre en charge au moins les colonnes de propriétés suivantes: 
  
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

Les colonnes de table de contenu binaire et de chaîne peuvent être tronquées. En règle générale, les fournisseurs renvoient 255 caractères. Étant donné que vous ne pouvez pas savoir si une table comporte des colonnes tronquées, supposons qu'une colonne est tronquée si sa longueur est de 255 ou 510 octets. Vous pouvez toujours récupérer la valeur complète d'une colonne tronquée, si nécessaire, directement à partir de l'objet à l'aide de son identificateur d'entrée pour l'ouvrir, puis en appelant la méthode **IMAPIProp:: GetProps** . 
  
En fonction de l'implémentation du fournisseur, les restrictions et les opérations de tri peuvent s'appliquer à l'ensemble d'une chaîne ou à la version tronquée de cette chaîne.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableDialog. cpp  <br/> |CContentsTableDlg:: CContentsTableDlg  <br/> |La classe **CContentsTableDlg** utilise **GetContentsTable** pour obtenir les entrées dans une table des matières.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[Propriété canonique PidTagContainerContents](pidtagcontainercontents-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

