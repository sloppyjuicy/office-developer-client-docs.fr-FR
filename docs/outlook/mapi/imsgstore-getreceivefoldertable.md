---
title: IMsgStoreGetReceiveFolderTable
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 282be30ddd4e55e703cac37dae942c96b05afcd8
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62773284"
---
# <a name="imsgstoregetreceivefoldertable"></a>IMsgStore::GetReceiveFolderTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet d’accéder à la table des dossiers de réception, une table qui inclut des informations sur tous les dossiers de réception de la boutique de messages.
  
```cpp
HRESULT GetReceiveFolderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable );
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle l’accès à la table. Les indicateurs suivants peuvent être définies :
    
MAPI_DEFERRED_ERRORS 
  
> Permet à **GetReceiveFolderTable de renvoyer** correctement, éventuellement avant que la table soit entièrement disponible pour l’appelant. Si la table n’est pas entièrement disponible, la réalisation d’un appel de table ultérieur peut occasioner une erreur. 
    
MAPI_UNICODE 
  
> Les chaînes renvoyées sont au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    
 _lppTable_
  
> [out] Pointeur vers un pointeur vers le tableau du dossier de réception.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La table des dossiers de réception a été renvoyée avec succès.
    
## <a name="remarks"></a>Remarques

La **méthode IMsgStore::GetReceiveFolderTable** permet d’accéder à une table qui indique les paramètres de propriété pour tous les dossiers de réception de la boutique de messages. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Pour obtenir la liste des colonnes requises dans une table de dossiers de réception, voir [Tables des dossiers de réception](receive-folder-tables.md). 
  
Implémentez vos tables de dossiers de réception pour prendre en charge la définition de restrictions de propriété sur **la PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)). Cela permet d’accéder facilement à des dossiers de réception particuliers.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

La définition de l’indicateur MAPI_UNICODE dans le paramètre _ulFlags_ affecte le format des colonnes renvoyées par les méthodes [IMAPITable::QueryColumns](imapitable-querycolumns.md) et [IMAPITable::QueryRows](imapitable-queryrows.md) . Cet indicateur contrôle également les types de propriétés dans l’ordre de tri renvoyé par la méthode [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnDisplayReceiveFolderTable  <br/> |MFCMAPI utilise la méthode **IMsgStore::GetReceiveFolderTable** pour obtenir la table des dossiers de réception à afficher. |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

