---
title: IMAPISessionGetStatusTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISession.GetStatusTable
api_type:
- COM
ms.assetid: 53428f8d-4838-46d1-a0ab-cafb194f4cc3
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8c76d4fb1654b55a15d2c86db7ede25d1fc26da9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620897"
---
# <a name="imapisessiongetstatustable"></a>IMAPISession::GetStatusTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet d’accéder à la table d’état, une table qui contient des informations sur toutes les ressources MAPI de la session.
  
```cpp
HRESULT GetStatusTable(
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
  
> [out] Pointeur vers un pointeur vers le tableau d’état.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La table a été renvoyée avec succès.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISession::GetStatusTable** permet d’accéder à la table d’état qui contient des informations sur toutes les ressources MAPI de la session. Le tableau comprend une ligne pour obtenir des informations sur le sous-système MAPI, une ligne pour lepooler MAPI, une ligne pour le carnet d’adresses intégré et une ligne pour chaque fournisseur de services dans le profil. 
  
Pour obtenir la liste complète des colonnes obligatoires et facultatives dans le tableau d’état, voir [Tableaux d’état.](status-tables.md) 
  
La définition de l’indicateur MAPI_UNICODE dans le paramètre _ulFlags_ affecte le format des colonnes renvoyées par les méthodes [IMAPITable::QueryColumns](imapitable-querycolumns.md) et [IMAPITable::QueryRows.](imapitable-queryrows.md) Cet indicateur contrôle également les types de propriétés dans l’ordre de tri renvoyé par la méthode [IMAPITable::QuerySortOrder.](imapitable-querysortorder.md) 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnStatusTable  <br/> |MFCMAPI utilise la méthode **IMAPISession::GetStatusTable** pour obtenir la table d’état à restituer.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable : IUnknown](imapitableiunknown.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Tables d’état](status-tables.md)

