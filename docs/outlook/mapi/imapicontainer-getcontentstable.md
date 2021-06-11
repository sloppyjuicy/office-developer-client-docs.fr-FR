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

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont la table des matières est renvoyée. Les indicateurs suivants peuvent être définies :
    
MAPI_ASSOCIATED 
  
> La table des matières associée au conteneur doit être renvoyée au lieu de la table des matières standard. Cet indicateur est utilisé uniquement avec les dossiers. Les messages qui sont inclus dans la table des matières associée ont été créés avec l’indicateur MAPI_ASSOCIATED définie dans l’appel à la méthode [IMAPIFolder::CreateMessage.](imapifolder-createmessage.md) Les clients utilisent généralement la table des matières associée pour récupérer des formulaires, des affichages et d’autres messages masqués. 
    
ACLTABLE_FREEBUSY
  
> Permet d’accéder aux droits frightsFreeBusySimple et frightsFreeBusyDetailed **dans PR_MEMBER_RIGHTS**.
    
MAPI_DEFERRED_ERRORS 
  
> **GetContentsTable** peut renvoyer correctement, éventuellement avant que la table soit disponible pour l’appelant. Si la table n’est pas disponible, effectuer un appel de table ultérieur peut occasioner une erreur. 
    
MAPI_UNICODE 
  
> Demande que les colonnes qui contiennent des données de chaîne soient renvoyées au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les chaînes doivent être renvoyées au format ANSI. 
    
SHOW_SOFT_DELETES
  
> Affiche les éléments actuellement marqués comme supprimés (supprimés (supprimés( en d’autres cas), ils sont dans la phase de rétention des éléments supprimés.
    
 _lppTable_
  
> [out] Pointeur vers un pointeur vers la table des matières.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La table des matières a été récupérée avec succès.
    
MAPI_E_BAD_CHARWIDTH 
  
> L’indicateur MAPI_UNICODE a été définie et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et l’implémentation prend uniquement en charge Unicode.
    
MAPI_E_NO_SUPPORT 
  
> Le conteneur n’a pas de contenu et ne peut pas fournir de table des matières.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPIContainer::GetContentsTable** renvoie un pointeur vers la table des matières d’un conteneur. Une table des matières contient des informations récapitulatifs sur les objets dans le conteneur. 
  
Les tables des matières ont des ensembles de colonnes longs. Pour obtenir la liste complète des colonnes obligatoires et facultatives dans les tables des matières, voir [Tables des matières.](contents-tables.md) 
  
Il est possible que certains conteneurs n’ont pas de contenu. Ces conteneurs retournent MAPI_E_NO_SUPPORT à partir de leurs implémentations **de GetContentsTable**.
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Si vous prendre en charge une table des matières pour votre conteneur, vous devez également :
  
- Prendre en charge les appels à la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) du conteneur pour ouvrir la propriété **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)).
    
- Renvoyer **PR_CONTAINER_CONTENTS** en réponse à un appel au conteneur 
    
    [Méthodes IMAPIProp::GetProps](imapiprop-getprops.md) et [IMAPIProp::GetPropList.](imapiprop-getproplist.md) 
    
L’implémentation de cette méthode par un fournisseur de transport distant doit renvoyer un pointeur vers une interface [IMAPITable : IUnknown](imapitableiunknown.md) dans le paramètre _ppTable_ transmis à la méthode **GetContentsTable.** Si votre fournisseur de transport possède une table des matières existante, il suffit de renvoyer un pointeur vers cette table. Si ce n’est pas le cas, cette méthode doit créer un objet [IMAPITable : IUnknown,](imapitableiunknown.md) remplir le tableau avec des en-têtes de message (le cas cas sont disponibles) et renvoyer un pointeur vers le nouveau tableau. La [méthode ITableData::HrGetView](itabledata-hrgetview.md) est utile pour générer une valeur de retour et stocker le pointeur de table dans le _paramètre ppTable._ La table des matières doit prendre en charge au moins les colonnes de propriété suivantes : 
  
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

Les colonnes de table de contenu binaire et de chaîne peuvent être tronquées. En règle générale, les fournisseurs retournent 255 caractères. Comme vous ne pouvez pas savoir au préalable si un tableau inclut des colonnes tronquées, supposons qu’une colonne est tronquée si la longueur de la colonne est de 255 ou 510 octets. Vous pouvez toujours récupérer la valeur complète d’une colonne tronquée, si nécessaire, directement à partir de l’objet en utilisant son identificateur d’entrée pour l’ouvrir, puis en appelant la méthode **IMAPIProp::GetProps.** 
  
Selon l’implémentation du fournisseur, les restrictions et les opérations de tri peuvent s’appliquer à l’ensemble d’une chaîne ou à la version tronquée de cette chaîne.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableDialog.cpp  <br/> |CContentsTableDlg::CContentsTableDlg  <br/> |La **classe CContentsTableDlg** utilise **GetContentsTable** pour obtenir les entrées dans une table des matières.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[Propriété canonique PidTagContainerContents](pidtagcontainercontents-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

