---
title: IMsgStoreGetReceiveFolderTable
description: IMsgStore GetReceiveFolderTable fournit l’accès à la table de dossiers de réception, qui inclut des informations sur tous les dossiers de réception pour le magasin de messages.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgStore.GetReceiveFolderTable
api_type:
- COM
ms.assetid: d115ab58-07d2-4b49-8e08-2881c2924102
ms.openlocfilehash: 90d8347018421988006437d0772d8330b007f715
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828303"
---
# <a name="imsgstoregetreceivefoldertable"></a>IMsgStore::GetReceiveFolderTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit l’accès à la table de dossiers de réception, une table qui inclut des informations sur tous les dossiers de réception pour le magasin de messages.
  
```cpp
HRESULT GetReceiveFolderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable );
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôlent l’accès à la table. Les indicateurs suivants peuvent être définis :
    
MAPI_DEFERRED_ERRORS 
  
> Permet à **GetReceiveFolderTable** de retourner correctement, éventuellement avant que la table soit entièrement disponible pour l’appelant. Si la table n’est pas entièrement disponible, l’exécution d’un appel de table ultérieur peut générer une erreur. 
    
MAPI_UNICODE 
  
> Les chaînes retournées sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas défini, les chaînes sont au format ANSI.
    
 _lppTable_
  
> [out] Pointeur vers un pointeur vers la table de dossiers de réception.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La table de dossiers de réception a été retournée avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **IMsgStore::GetReceiveFolderTable** permet d’accéder à une table qui affiche les paramètres de propriété de tous les dossiers de réception du magasin de messages. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Pour obtenir la liste des colonnes requises dans une table de dossiers de réception, consultez [Tables de dossiers de](receive-folder-tables.md) réception. 
  
Implémentez vos tables de dossiers de réception pour prendre en charge la définition de restrictions de propriété sur la propriété **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)). Cela permet d’accéder facilement à des dossiers de réception particuliers.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

La définition de l’indicateur MAPI_UNICODE dans le paramètre _ulFlags_ affecte le format des colonnes retournées à partir des méthodes [IMAPITable::QueryColumns](imapitable-querycolumns.md) et [IMAPITable::QueryRows](imapitable-queryrows.md) . Cet indicateur contrôle également les types de propriétés dans l’ordre de tri retourné par la méthode [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnDisplayReceiveFolderTable  <br/> |MFCMAPI utilise la méthode **IMsgStore::GetReceiveFolderTable** pour obtenir la table de dossiers de réception à afficher. |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

