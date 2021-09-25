---
title: IMAPITableCollapseRow
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6f8d1319f5655591bdd11188910e2ac458b4dcfc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584352"
---
# <a name="imapitablecollapserow"></a>IMAPITable::CollapseRow

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Réduit une catégorie de tableau étendu, en supprimant les en-tête de niveau inférieur et les lignes de feuille appartenant à la catégorie de l’affichage Tableau.
  
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
  
> [in] Nombre d’octets dans la propriété PR_INSTANCE_KEY pointant vers le _paramètre pbInstanceKey._ 
    
 _pbInstanceKey_
  
> [in] Pointeur vers la **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) qui identifie la ligne de titre de la catégorie. 
    
 _ulFlags_
  
> Réservé ; doit être zéro.
    
 _lpulRowCount_
  
> [out] Pointeur vers le nombre total de lignes supprimées de l’affichage Tableau.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’opération de réduire a réussi.
    
MAPI_E_NOT_FOUND 
  
> La ligne identifiée par le  _paramètre pbInstanceKey_ n’existe pas. 
    
MAPI_E_INVALID_ENTRYID 
  
> La ligne identifiée par le  _paramètre pbInstanceKey_ n’existe pas. Cette erreur est une alternative à la MAPI_E_NOT_FOUND ; les fournisseurs de services peuvent renvoyer l’un ou l’autre. 
    
## <a name="remarks"></a>Remarques

La **méthode IMAPITable::CollapseRow** permet de réduire une catégorie de tableau et de la supprimer de l’affichage Tableau. Les lignes sont réduire à partir de la ligne identifiée par la **propriété PR_INSTANCE_KEY** pointée par le _paramètre pbInstanceKey._ Le nombre de lignes supprimées de l’affichage est renvoyé dans le contenu du _paramètre lpulRowCount._ 
  
Les notifications ne sont jamais générées pour les lignes de tableau qui sont supprimées d’un affichage suite à une opération de réduire. 
  
Lorsqu’une ligne définie par un signet est en dehors de l’affichage, le signet est déplacé pour pointer vers la ligne visible suivante. 
  
Pour plus d’informations sur les tableaux classés, voir [Tri et catégorisation.](sorting-and-categorization.md)
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::D oExpandCollapse  <br/> |MFCMAPI utilise la **méthode IMAPITable::CollapseRow** pour réduire une catégorie de tableau.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable::ExpandRow](imapitable-expandrow.md)
  
[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

