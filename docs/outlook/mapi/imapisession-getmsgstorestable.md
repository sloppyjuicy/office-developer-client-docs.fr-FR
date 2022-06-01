---
title: IMAPISessionGetMsgStoresTable
description: IMAPISessionGetMsgStoresTable permet d’accéder à la table du magasin de messages qui contient des informations sur tous les magasins de messages dans le profil de session.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISession.GetMsgStoresTable
api_type:
- COM
ms.assetid: 77db2dff-4534-440f-a05c-635711cbc2c3
ms.openlocfilehash: 6e9264f671fd43f66155777442de8e2506e1edc2
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817248"
---
# <a name="imapisessiongetmsgstorestable"></a>IMAPISession::GetMsgStoresTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit l’accès à la table du magasin de messages qui contient des informations sur tous les magasins de messages dans le profil de session.
  
```cpp
HRESULT GetMsgStoresTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Masque de bits des indicateurs qui détermine le format des colonnes qui sont des chaînes de caractères. L’indicateur suivant peut être défini :
    
MAPI_UNICODE 
  
> Les colonnes de chaîne sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas défini, les colonnes de chaîne sont au format ANSI.
    
 _lppTable_
  
> [out] Pointeur vers un pointeur vers la table du magasin de messages.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La table a été retournée avec succès.
    
MAPI_E_BAD_CHARWIDTH 
  
> L’indicateur MAPI_UNICODE a été défini et la session ne prend pas en charge Unicode.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISession::GetMsgStoresTable** récupère un pointeur vers la table du magasin de messages, une table gérée par MAPI qui contient des informations sur chaque magasin de messages ouvert dans le profil. 
  
Pour obtenir la liste complète des colonnes requises et facultatives dans la table du magasin de messages, consultez [Tables du Magasin de messages](message-store-tables.md). 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Étant donné que MAPI met à jour la table du magasin de messages pendant la session chaque fois que des modifications se produisent, appelez la méthode **Advise** de la table du magasin de messages pour vous inscrire pour être informé de ces modifications. Les modifications possibles incluent l’ajout de nouveaux magasins de messages, la suppression des magasins existants et les modifications apportées au magasin par défaut. 
  
La définition de l’indicateur MAPI_UNICODE dans le paramètre _ulFlags_ affecte le format des colonnes retournées à partir des méthodes [IMAPITable::QueryColumns](imapitable-querycolumns.md) et [IMAPITable::QueryRows](imapitable-queryrows.md) . Cet indicateur contrôle également les types de propriétés dans l’ordre de tri retourné par la méthode [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenMessageStoreTable  <br/> |MFCMAPI utilise la méthode **IMAPISession::GetMsgStoresTable** pour obtenir la table du magasin de messages afin qu’elle puisse être affichée dans la boîte de dialogue principale de MFCMAPI. |
   
## <a name="see-also"></a>Voir aussi



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Tables du Magasin de messages](message-store-tables.md)

