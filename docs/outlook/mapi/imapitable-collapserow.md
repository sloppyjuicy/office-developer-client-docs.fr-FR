---
title: IMAPITableCollapseRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.CollapseRow
api_type:
- COM
ms.assetid: 1a23e555-be26-43fb-a715-cfc4ffa623cd
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b4dd7e9715c2d3c99eda44f7eed0b3360a2e33be
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595299"
---
# <a name="imapitablecollapserow"></a>IMAPITable::CollapseRow

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Réduire une catégorie de table étendue, supprimant tous les titres de niveau inférieur et les lignes de feuilles appartenant à la catégorie à partir de l’affichage tableau.
  
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
  
> [in] Le nombre d’octets dans la propriété PR_INSTANCE_KEY indiqué par le paramètre _pbInstanceKey_ . 
    
 _pbInstanceKey_
  
> [in] Pointeur vers la propriété **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) qui identifie la ligne d’en-tête de la catégorie. 
    
 _ulFlags_
  
> Réservé ; doit être égal à zéro.
    
 _lpulRowCount_
  
> [out] Pointeur vers le nombre total de lignes qui sont supprimés de l’affichage tableau.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’opération de réduction a réussi.
    
MAPI_E_NOT_FOUND 
  
> La ligne identifiée par le paramètre _pbInstanceKey_ n’existe pas. 
    
MAPI_E_INVALID_ENTRYID 
  
> La ligne identifiée par le paramètre _pbInstanceKey_ n’existe pas. Cette erreur est une alternative à MAPI_E_NOT_FOUND ; fournisseurs de services peuvent renvoyer le d’eux. 
    
## <a name="remarks"></a>Remarques

La méthode **IMAPITable::CollapseRow** réduire une catégorie de table et le supprime de l’affichage tableau. Les lignes sont réduits commençant à la ligne identifiée par la propriété **PR_INSTANCE_KEY** désignée par le paramètre _pbInstanceKey_ . Le nombre de lignes qui sont supprimés de l’affichage est retourné dans le contenu du paramètre _lpulRowCount_ . 
  
Les notifications ne sont jamais générées pour les lignes de tableau qui sont supprimés d’un affichage à la suite d’une opération de réduction. 
  
Lorsqu’une ligne est définie par un signet est réduite en dehors de l’affichage, le signet est déplacé pour pointer vers la ligne visible suivante. 
  
Pour plus d’informations sur les tables, voir, consultez [tri et catégorisation](sorting-and-categorization.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::DoExpandCollapse  <br/> |MFCMAPI utilise la méthode **IMAPITable::CollapseRow** pour réduire une catégorie de table.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable::ExpandRow](imapitable-expandrow.md)
  
[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

