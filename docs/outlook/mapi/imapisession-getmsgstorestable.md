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
ms.openlocfilehash: 5fced633023ebf00efaf5b667dc7994eeb5de316
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428136"
---
# <a name="imapisessiongetmsgstorestable"></a>IMAPISession::GetMsgStoresTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet d’accéder à la table de la boutique de messages qui contient des informations sur tous les magasins de messages dans le profil de session.
  
```cpp
HRESULT GetMsgStoresTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui détermine le format des colonnes qui sont des chaînes de caractères. L’indicateur suivant peut être définie :
    
MAPI_UNICODE 
  
> Les colonnes de chaîne sont au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les colonnes de chaîne sont au format ANSI.
    
 _lppTable_
  
> [out] Pointeur vers un pointeur vers le tableau de la boutique de messages.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La table a été renvoyée avec succès.
    
MAPI_E_BAD_CHARWIDTH 
  
> L’MAPI_UNICODE a été définie et la session ne prend pas en charge Unicode.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISession::GetMsgStoresTable** récupère un pointeur vers la table de la boutique de messages, une table maintenue par MAPI qui contient des informations sur chaque magasin de messages ouvert dans le profil. 
  
Pour obtenir la liste complète des colonnes obligatoires et facultatives dans la table de la boutique de messages, voir [Tables de la boutique de messages.](message-store-tables.md) 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Étant donné que MAPI met à jour la table de la boutique de messages pendant la session chaque fois que des modifications se produisent, appelez la méthode **Advise** de la table de la boutique de messages pour être averti de ces modifications. Les modifications possibles incluent l’ajout de nouvelles magasins de messages, la suppression de magasins existants et les modifications apportées à la boutique par défaut. 
  
La définition de l’indicateur MAPI_UNICODE dans le paramètre _ulFlags_ affecte le format des colonnes renvoyées par les méthodes [IMAPITable::QueryColumns](imapitable-querycolumns.md) et [IMAPITable::QueryRows.](imapitable-queryrows.md) Cet indicateur contrôle également les types de propriétés dans l’ordre de tri renvoyé par la méthode [IMAPITable::QuerySortOrder.](imapitable-querysortorder.md) 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenMessageStoreTable  <br/> |MFCMAPI utilise la méthode **IMAPISession::GetMsgStoresTable** pour obtenir la table de la boutique de messages afin qu’elle puisse être rendue dans la boîte de dialogue principale de MFCMAPI.  <br/> |
   
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
  
[Tables de la boutique de messages](message-store-tables.md)

