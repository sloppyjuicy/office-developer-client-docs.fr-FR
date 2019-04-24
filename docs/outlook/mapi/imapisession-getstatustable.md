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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 17e936093536f548d16021523d9434f09777c6d9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338759"
---
# <a name="imapisessiongetstatustable"></a>IMAPISession::GetStatusTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit l'accès à la table d'État, un tableau qui contient des informations sur toutes les ressources MAPI de la session.
  
```cpp
HRESULT GetStatusTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> dans Masque de réfixe des indicateurs qui déterminent le format des colonnes qui sont des chaînes de caractères. L'indicateur suivant peut être défini:
    
MAPI_UNICODE 
  
> Les colonnes de chaîne sont au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les colonnes de la chaîne sont au format ANSI.
    
 _lppTable_
  
> remarquer Pointeur vers un pointeur vers la table d'État.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La table a été renvoyée avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISession:: GetStatusTable** fournit l'accès à la table d'État qui contient des informations sur toutes les ressources MAPI de la session. Il y a une ligne dans le tableau pour obtenir des informations sur le sous-système MAPI, une ligne pour le spouleur MAPI, une ligne pour le carnet d'adresses intégré et une ligne pour chaque fournisseur de services dans le profil. 
  
Pour obtenir la liste complète des colonnes obligatoires et facultatives dans la table d'État, reportez-vous à la rubrique [Status tables](status-tables.md). 
  
La définition de l'indicateur MAPI_UNICODE dans le paramètre _ulFlags_ affecte le format des colonnes renvoyées par les méthodes [IMAPITable:: QueryColumns](imapitable-querycolumns.md) et [IMAPITable:: QueryRows](imapitable-queryrows.md) . Cet indicateur contrôle également les types de propriétés dans l'ordre de tri retourné par la méthode [IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MainDlg. cpp  <br/> |CMainDlg:: OnStatusTable  <br/> |MFCMAPI utilise la méthode **IMAPISession:: GetStatusTable** pour obtenir la table d'État à afficher.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable : IUnknown](imapitableiunknown.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Tables d'État](status-tables.md)

