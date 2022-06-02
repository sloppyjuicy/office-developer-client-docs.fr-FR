---
title: IMAPITableCollapseRow
description: IMAPITableCollapseRow réduit une catégorie de table développée, en supprimant les en-têtes de niveau inférieur et les lignes de feuille appartenant à la catégorie de la vue de table.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.CollapseRow
api_type:
- COM
ms.assetid: 1a23e555-be26-43fb-a715-cfc4ffa623cd
ms.openlocfilehash: ea6693e341f9d3df60a0bfae59ab911f09b65910
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65827862"
---
# <a name="imapitablecollapserow"></a>IMAPITable::CollapseRow

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Réduit une catégorie de tableau développée, en supprimant les en-têtes de niveau inférieur et les lignes de feuille appartenant à la catégorie de la vue de table.
  
```cpp
HRESULT CollapseRow(
ULONG cbInstanceKey,
LPBYTE pbInstanceKey,
ULONG ulFlags,
ULONG FAR * lpulRowCount
);
```

## <a name="parameters"></a>Paramètres

 _cbInstanceKey_
  
> [in] Nombre d’octets dans la propriété PR_INSTANCE_KEY pointée par le paramètre  _pbInstanceKey_ . 
    
 _pbInstanceKey_
  
> [in] Pointeur vers la propriété **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) qui identifie la ligne de titre de la catégorie. 
    
 _ulFlags_
  
> Réservé; doit être égal à zéro.
    
 _lpulRowCount_
  
> [out] Pointeur vers le nombre total de lignes qui sont supprimées de la vue table.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’opération d’effondrement a réussi.
    
MAPI_E_NOT_FOUND 
  
> La ligne identifiée par le paramètre  _pbInstanceKey_ n’existe pas. 
    
MAPI_E_INVALID_ENTRYID 
  
> La ligne identifiée par le paramètre  _pbInstanceKey_ n’existe pas. Cette erreur est une alternative à MAPI_E_NOT_FOUND; les fournisseurs de services peuvent retourner l’un ou l’autre. 
    
## <a name="remarks"></a>Remarques

La méthode **IMAPITable::CollapseRow** réduit une catégorie de table et la supprime de la vue table. Les lignes sont réduites à partir de la ligne identifiée par la propriété **PR_INSTANCE_KEY** pointée par le paramètre  _pbInstanceKey_ . Le nombre de lignes supprimées de la vue est retourné dans le contenu du paramètre  _lpulRowCount_ . 
  
Les notifications ne sont jamais générées pour les lignes de table qui sont supprimées d’une vue à la suite d’une opération d’effondrement. 
  
Lorsqu’une ligne définie par un signet est réduite hors vue, le signet est déplacé pour pointer vers la ligne visible suivante. 
  
Pour plus d’informations sur les tables catégorisées, consultez [Tri et catégorisation](sorting-and-categorization.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::D oExpandCollapse  <br/> |MFCMAPI utilise la méthode **IMAPITable::CollapseRow** pour réduire une catégorie de table. |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable::ExpandRow](imapitable-expandrow.md)
  
[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

