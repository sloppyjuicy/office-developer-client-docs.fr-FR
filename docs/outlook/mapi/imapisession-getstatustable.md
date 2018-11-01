---
title: IMAPISessionGetStatusTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetStatusTable
api_type:
- COM
ms.assetid: 53428f8d-4838-46d1-a0ab-cafb194f4cc3
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 48a69fa49735014dcbfffad0673f1d4da62452e7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594830"
---
# <a name="imapisessiongetstatustable"></a>IMAPISession::GetStatusTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit l’accès à la table d’état, une table qui contient des informations sur toutes les ressources MAPI dans la session.
  
```cpp
HRESULT GetStatusTable(
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
  
> [out] Pointeur vers un pointeur vers la table d’état.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le tableau a été renvoyé avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISession::GetStatusTable** permet d’accéder à la table d’état qui contient des informations sur toutes les ressources MAPI dans la session. Il y a une ligne dans le tableau pour plus d’informations sur le sous-système MAPI, une ligne pour le spouleur MAPI, une ligne pour le carnet d’adresses intégré et une ligne pour chaque fournisseur de services dans le profil. 
  
Pour obtenir une liste complète des colonnes obligatoires et facultatifs dans la table d’état, voir [Tableaux d’état](status-tables.md). 
  
Définition de l’indicateur MAPI_UNICODE dans le paramètre _ulFlags_ affecte le format des colonnes retournées par les méthodes [IMAPITable::QueryColumns](imapitable-querycolumns.md) et [IMAPITable::QueryRows](imapitable-queryrows.md) . Cet indicateur contrôle également les types de propriétés dans l’ordre de tri renvoyé par la méthode [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnStatusTable  <br/> |MFCMAPI utilise la méthode **IMAPISession::GetStatusTable** pour obtenir la table d’état à afficher.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable : IUnknown](imapitableiunknown.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI en tant qu’exemple de code](mfcmapi-as-a-code-sample.md)
  
[Tableaux d’état](status-tables.md)

