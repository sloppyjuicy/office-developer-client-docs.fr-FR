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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 871dafd7bf8959cf814d65991fe08fdb2b283c08
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783705"
---
# <a name="imapicontainergetcontentstable"></a>IMAPIContainer::GetContentsTable

  
  
**S’applique à**: Outlook 
  
Retourne un pointeur vers la table des matières du conteneur.
  
```cpp
HRESULT GetContentsTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont la table des matières est renvoyée. Les indicateurs suivants peuvent être définis :
    
MAPI_ASSOCIATED 
  
> Table des matières associée du conteneur doit être retournée au lieu de la table des matières standard. Cet indicateur est utilisé uniquement avec les dossiers. Les messages qui sont inclus dans le tableau contenu associé ont été créés avec l’indicateur MAPI_ASSOCIATED défini dans l’appel à la méthode [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) . Clients utilisent généralement le tableau contenu associé pour récupérer les formulaires, les vues et les autres messages masqués. 
    
ACLTABLE_FREEBUSY
  
> Permet d’accéder aux droits frightsFreeBusySimple et frightsFreeBusyDetailed dans **PR_MEMBER_RIGHTS**.
    
MAPI_DEFERRED_ERRORS 
  
> **GetContentsTable** peut renvoyer avec succès, probablement que le tableau soit disponible à l’appelant. Si le tableau n’est pas disponible, l’émission d’un appel de la table suivante peut déclencher une erreur. 
    
MAPI_UNICODE 
  
> Demandes de renvoyer les colonnes qui contiennent des données de type chaîne au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes doivent être retournées au format ANSI. 
    
SHOW_SOFT_DELETES
  
> Affiche les éléments qui sont actuellement marqués comme logicielles supprimés — autrement dit, ils sont dans la rétention des éléments supprimés phase de temps.
    
 _lppTable_
  
> [out] Pointeur vers un pointeur vers la table des matières.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le tableau contenu a été récupéré correctement.
    
MAPI_E_BAD_CHARWIDTH 
  
> Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été défini et l’implémentation prend en charge Unicode uniquement.
    
MAPI_E_NO_SUPPORT 
  
> Le conteneur n’a pas de contenu et ne peuvent pas fournir une table des matières.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIContainer::GetContentsTable** renvoie un pointeur vers la table des matières d’un conteneur. Une table des matières contient des informations récapitulatives concernant les objets dans le conteneur. 
  
Tables des matières disposez d’ensembles de colonne longs. Pour obtenir une liste complète des colonnes obligatoires et facultatifs dans les tableaux de contenu, voir [Les Tables de contenu](contents-tables.md). 
  
Il est possible pour certains conteneurs de n’avoir aucun contenu. Ces conteneurs renvoient MAPI_E_NO_SUPPORT à partir de leurs implémentations de **GetContentsTable**.
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Si vous prenez en charge une table des matières pour votre conteneur, vous devez également procédez comme suit :
  
- Prend en charge les appels de méthode de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) du conteneur pour ouvrir la propriété **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)).
    
- Retourner **PR_CONTAINER_CONTENTS** en réponse à un appel à du conteneur 
    
    Méthodes [IMAPIProp::GetProps](imapiprop-getprops.md) et [IMAPIProp::GetPropList](imapiprop-getproplist.md) . 
    
Implémentation d’un fournisseur de transport à distance de cette méthode doit renvoyer un pointeur vers une [IMAPITable : IUnknown](imapitableiunknown.md) interface dans le paramètre _ppTable_ transmis à la méthode **GetContentsTable** . Si votre fournisseur de transport a une table de contenu existante, il suffit de retourner un pointeur. Si pas, cette méthode doit créer une nouvelle [IMAPITable : IUnknown](imapitableiunknown.md) objet, remplir le tableau avec des en-têtes de message (s’ils sont disponibles) et retourner un pointeur vers la nouvelle table. La méthode [ITableData::HrGetView](itabledata-hrgetview.md) est utile pour la génération d’une valeur de retour et en stockant le pointeur de la table dans le paramètre _ppTable_ . La table des matières doit prendre en charge au moins les colonnes de propriété suivantes : 
  
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
    
## <a name="notes-to-callers"></a>Notes aux appelants

Colonnes de tableau contenu chaîne et binaires peuvent être tronqués. En règle générale, les fournisseurs retournent 255 caractères. Car vous ne pouvez pas savoir au préalable si une table inclut des colonnes tronqués, supposons qu’une colonne est tronquée si la longueur de la colonne est 255 ou 510 octets. Vous pouvez toujours récupérer la valeur complète d’une colonne tronquée, si nécessaire, directement à partir de l’objet à l’aide de son identificateur d’entrée pour l’ouvrir, puis en appelant la méthode **IMAPIProp::GetProps** . 
  
Selon l’implémentation du fournisseur, les restrictions et les opérations de tri peuvent s’appliquent à l’ensemble d’une chaîne ou vers la version tronquée de cette chaîne.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableDialog.cpp  <br/> |CContentsTableDlg::CContentsTableDlg  <br/> |La classe **CContentsTableDlg** utilise **GetContentsTable** pour obtenir les entrées dans une table des matières.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[Propriété canonique PidTagContainerContents](pidtagcontainercontents-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

