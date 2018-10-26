---
title: IMAPISessionGetMsgStoresTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetMsgStoresTable
api_type:
- COM
ms.assetid: 77db2dff-4534-440f-a05c-635711cbc2c3
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: cc0039cf2210446704d25b2156bd4ff50041a524
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586276"
---
# <a name="imapisessiongetmsgstorestable"></a>IMAPISession::GetMsgStoresTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet d’accéder à la table de magasin de message qui contient des informations sur toutes les banques de messages dans le profil de la session.
  
```cpp
HRESULT GetMsgStoresTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui détermine le format des colonnes sont des chaînes de caractères. Vous pouvez définir l’indicateur suivant :
    
MAPI_UNICODE 
  
> Les colonnes de type chaîne sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les colonnes de type chaîne sont au format ANSI.
    
 _lppTable_
  
> [out] Pointeur vers un pointeur vers la table.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le tableau a été renvoyé avec succès.
    
MAPI_E_BAD_CHARWIDTH 
  
> L’indicateur MAPI_UNICODE a été défini et que la session ne prend pas en charge Unicode.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISession::GetMsgStoresTable** récupère un pointeur vers la table, une table gérée par MAPI qui contient des informations sur chaque banque de messages ouverts dans le profil. 
  
Pour obtenir la liste complète des colonnes obligatoires et facultatifs dans le message magasin table, voir les [Tables de stocker des messages](message-store-tables.md). 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Étant donné que MAPI met à jour la table de banque de messages pendant la session en cas de modification, appelez la méthode **Advise** de la table de magasin de message pour s’inscrire afin d’être averti de ces modifications. Modifications possibles comprennent l’ajout de nouvelles banques de message, suppression existant stocke, remplace la banque par défaut. 
  
Définition de l’indicateur MAPI_UNICODE dans le paramètre _ulFlags_ affecte le format des colonnes retournées par les méthodes [IMAPITable::QueryColumns](imapitable-querycolumns.md) et [IMAPITable::QueryRows](imapitable-queryrows.md) . Cet indicateur contrôle également les types de propriétés dans l’ordre de tri renvoyé par la méthode [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenMessageStoreTable  <br/> |MFCMAPI utilise la méthode **IMAPISession::GetMsgStoresTable** pour obtenir la table afin qu’il peut être affiché dans la boîte de dialogue de MFCMAPI.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI en tant qu’exemple de code](mfcmapi-as-a-code-sample.md)
  
[Tables de la banque de messages](message-store-tables.md)

