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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 681fd68fc068633912df1cb7f060b8c4111b5de8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566536"
---
# <a name="imsgstoregetreceivefoldertable"></a>IMsgStore::GetReceiveFolderTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet d’accéder à la table de dossier de réception, une table qui consacrée des informations sur tous les dossiers de réception de la banque de messages.
  
```cpp
HRESULT GetReceiveFolderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable );
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs que les contrôles de table access. Les indicateurs suivants peuvent être définis :
    
MAPI_DEFERRED_ERRORS 
  
> Permet de **GetReceiveFolderTable** renvoyer avec succès, éventuellement avant le tableau est entièrement disponible à l’appelant. Si le tableau n’est pas disponible, un appel de la table suivante peut déclencher une erreur. 
    
MAPI_UNICODE 
  
> Les chaînes retournées sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    
 _lppTable_
  
> [out] Pointeur vers un pointeur vers le tableau de dossier de réception.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le tableau de dossier de réception a été renvoyé avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **IMsgStore::GetReceiveFolderTable** permet d’accéder à un tableau qui affiche que les paramètres de propriété pour tous les messages recevoir des dossiers. 
  
## <a name="notes-to-implementers"></a>Remarques à l’attention des responsables de l’implémentation

Pour une liste de colonnes dans une table de dossier de réception, voir [S’afficher les Tables de dossier](receive-folder-tables.md). 
  
Mettre en œuvre votre recevoir des tables de dossier pour prendre en charge des restrictions de propriété de paramètre de la propriété **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)). Cette permet d’accéder facilement aux notamment recevoir des dossiers.
  
## <a name="notes-to-callers"></a>Notes aux appelants

Définition de l’indicateur MAPI_UNICODE dans le paramètre _ulFlags_ affecte le format des colonnes retournées par les méthodes [IMAPITable::QueryColumns](imapitable-querycolumns.md) et [IMAPITable::QueryRows](imapitable-queryrows.md) . Cet indicateur contrôle également les types de propriétés dans l’ordre de tri renvoyé par la méthode [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnDisplayReceiveFolderTable  <br/> |MFCMAPI utilise la méthode **IMsgStore::GetReceiveFolderTable** pour obtenir la table de dossier de réception à afficher.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

