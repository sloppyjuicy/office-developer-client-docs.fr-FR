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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e6a180ceb325a705ebf226bb728c52cce7396490
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328961"
---
# <a name="imapitablecollapserow"></a>IMAPITable::CollapseRow

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Réduit une catégorie de tableau développée, en supprimant les en-têtes de niveau inférieur et les lignes de feuille appartenant à la catégorie de l'affichage tableau.
  
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
  
> dans Nombre d'octets dans la propriété PR_INSTANCE_KEY vers laquelle pointe le paramètre _pbInstanceKey_ . 
    
 _pbInstanceKey_
  
> dans Pointeur vers la propriété **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) qui identifie la ligne d'en-tête pour la catégorie. 
    
 _ulFlags_
  
> MSR doit être égal à zéro.
    
 _lpulRowCount_
  
> remarquer Pointeur vers le nombre total de lignes qui sont supprimées de l'affichage tableau.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'opération de réduction a réussi.
    
MAPI_E_NOT_FOUND 
  
> La ligne identifiée par le paramètre _pbInstanceKey_ n'existe pas. 
    
MAPI_E_INVALID_ENTRYID 
  
> La ligne identifiée par le paramètre _pbInstanceKey_ n'existe pas. Cette erreur est une alternative à MAPI_E_NOT_FOUND; les fournisseurs de services peuvent retourner l'un ou l'autre. 
    
## <a name="remarks"></a>Remarques

La méthode **IMAPITable:: CollapseRow** réduit une catégorie de table et la supprime de l'affichage tableau. Les lignes sont réduites en commençant à la ligne identifiée par la propriété **PR_INSTANCE_KEY** désignée par le paramètre _pbInstanceKey_ . Le nombre de lignes supprimées de la vue est renvoyé dans le contenu du paramètre _lpulRowCount_ . 
  
Les notifications ne sont jamais générées pour les lignes de tableau qui sont supprimées d'une vue suite à une opération de réduction. 
  
Lorsqu'une ligne définie par un signet est réduite en mode affichage, le signet est déplacé pour pointer vers la ligne visible suivante. 
  
Pour plus d'informations sur les tables classées, reportez-vous à la rubrique [Tri et catégorisation](sorting-and-categorization.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> |CContentsTableListCtrl::D oExpandCollapse  <br/> |MFCMAPI utilise la méthode **IMAPITable:: CollapseRow** pour réduire une catégorie de table.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable::ExpandRow](imapitable-expandrow.md)
  
[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

