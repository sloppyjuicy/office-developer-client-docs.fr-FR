---
title: IMsgStoreGetReceiveFolderTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.GetReceiveFolderTable
api_type:
- COM
ms.assetid: d115ab58-07d2-4b49-8e08-2881c2924102
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 303c2ef855d5cfc1d6614bda92b46c2da97717c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317352"
---
# <a name="imsgstoregetreceivefoldertable"></a>IMsgStore::GetReceiveFolderTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit l'accès à la table de dossiers de réception, un tableau qui contient des informations sur tous les dossiers de réception pour la Banque de messages.
  
```cpp
HRESULT GetReceiveFolderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable );
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle l'accès aux tableaux. Les indicateurs suivants peuvent être définis:
    
MAPI_DEFERRED_ERRORS 
  
> Permet à **GetReceiveFolderTable** de renvoyer correctement, éventuellement avant que la table soit entièrement disponible pour l'appelant. Si la table n'est pas entièrement disponible, un appel de tableau ultérieur peut déclencher une erreur. 
    
MAPI_UNICODE 
  
> Les chaînes renvoyées sont au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI.
    
 _lppTable_
  
> remarquer Pointeur vers un pointeur vers le tableau de dossiers de réception.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La table de dossiers de réception a été renvoyée avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **IMsgStore:: GetReceiveFolderTable** fournit l'accès à un tableau qui présente les paramètres de propriété de tous les dossiers de réception de la Banque de messages. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Pour obtenir la liste des colonnes requises dans une table de dossiers de réception, consultez la rubrique [Receive Folder tables](receive-folder-tables.md). 
  
Implémentez vos tables de dossiers de réception pour prendre en charge la définition de restrictions de propriété sur la propriété **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)). Cela permet d'accéder facilement à des dossiers de réception spécifiques.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

La définition de l'indicateur MAPI_UNICODE dans le paramètre _ulFlags_ affecte le format des colonnes renvoyées par les méthodes [IMAPITable:: QueryColumns](imapitable-querycolumns.md) et [IMAPITable:: QueryRows](imapitable-queryrows.md) . Cet indicateur contrôle également les types de propriétés dans l'ordre de tri retourné par la méthode [IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MsgStoreDlg. cpp  <br/> |CMsgStoreDlg:: OnDisplayReceiveFolderTable  <br/> |MFCMAPI utilise la méthode **IMsgStore:: GetReceiveFolderTable** pour obtenir la table de dossiers de réception à afficher.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

