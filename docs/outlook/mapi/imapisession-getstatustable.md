---
title: IMAPISessionGetStatusTable
description: IMAPISessionGetStatusTable permet d’accéder à la table d’état, une table qui contient des informations sur toutes les ressources MAPI de la session.
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
ms.openlocfilehash: 79048fbf8c2b4e39ff01825ebdf7e3237ad13b62
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817241"
---
# <a name="imapisessiongetstatustable"></a>IMAPISession::GetStatusTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit l’accès à la table d’état, une table qui contient des informations sur toutes les ressources MAPI de la session.
  
```cpp
HRESULT GetStatusTable(
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
  
> [out] Pointeur vers un pointeur vers la table d’état.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La table a été retournée avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISession::GetStatusTable** permet d’accéder à la table d’état qui contient des informations sur toutes les ressources MAPI de la session. La table contient une ligne pour plus d’informations sur le sous-système MAPI, une ligne pour le spouleur MAPI, une ligne pour le carnet d’adresses intégré et une ligne pour chaque fournisseur de services dans le profil. 
  
Pour obtenir la liste complète des colonnes obligatoires et facultatives dans la table d’état, consultez [Tables d’état](status-tables.md). 
  
La définition de l’indicateur MAPI_UNICODE dans le paramètre _ulFlags_ affecte le format des colonnes retournées à partir des méthodes [IMAPITable::QueryColumns](imapitable-querycolumns.md) et [IMAPITable::QueryRows](imapitable-queryrows.md) . Cet indicateur contrôle également les types de propriétés dans l’ordre de tri retourné par la méthode [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnStatusTable  <br/> |MFCMAPI utilise la méthode **IMAPISession::GetStatusTable** pour obtenir la table d’état à afficher. |
   
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

