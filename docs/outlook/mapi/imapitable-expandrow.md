---
title: IMAPITableExpandRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.ExpandRow
api_type:
- COM
ms.assetid: b96dd8f6-e648-4014-8a1d-ae1da771c439
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 5e2ce756baaefef7bd0028e746b1dbe10756365e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329041"
---
# <a name="imapitableexpandrow"></a>IMAPITable::ExpandRow

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Développe une catégorie de table réduite, ajoutant la feuille ou les lignes de titre de niveau inférieur appartenant à la catégorie à l'affichage tableau.
  
```cpp
HRESULT ExpandRow(
ULONG cbInstanceKey,
LPBYTE pbInstanceKey,
ULONG ulRowCount,
ULONG ulFlags,
LPSRowSet FAR * lppRows,
ULONG FAR * lpulMoreRows
);
```

## <a name="parameters"></a>Paramètres

 _cbInstanceKey_
  
> dans Nombre d'octets dans la propriété PR_INSTANCE_KEY vers laquelle pointe le paramètre _pbInstanceKey_ . 
    
 _pbInstanceKey_
  
> dans Pointeur vers la propriété **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) qui identifie la ligne d'en-tête pour la catégorie. 
    
 _ulRowCount_
  
> dans Nombre maximal de lignes à renvoyer dans le paramètre _lppRows_ . 
    
 _ulFlags_
  
> MSR doit être égal à zéro.
    
 _lppRows_
  
> remarquer Pointeur vers une structure [SRowSet](srowset.md) qui reçoit les premières lignes (jusqu'à _ulRowCount_) qui ont été insérées dans l'affichage de tableau à la suite de l'expansion. Ces lignes sont insérées après la ligne d'en-tête identifiée par le paramètre _pbInstanceKey_ . Le paramètre _lppRows_ peut être null si le paramètre _ulRowCount_ est égal à zéro. 
    
 _lpulMoreRows_
  
> remarquer Pointeur vers le nombre total de lignes qui ont été ajoutées à l'affichage tableau.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La catégorie a été développée.
    
MAPI_E_NOT_FOUND 
  
> La ligne identifiée par le paramètre _pbInstanceKey_ n'existe pas. 
    
## <a name="remarks"></a>Remarques

La méthode **IMAPITable:: ExpandRow** développe une catégorie de table réduite, ajoutant la feuille ou les lignes de titre de niveau inférieur qui appartiennent à la catégorie à la vue de table. Une limite au nombre de lignes à renvoyer dans le paramètre _lppRows_ peut être spécifiée dans le paramètre _ulRowCount_ . Lorsque _ulRowCount_ est défini sur une valeur supérieure à zéro et qu'une ou plusieurs lignes sont renvoyées dans l'ensemble de lignes désigné par _lppRows_, la position du signet BOOKMARK_CURRENT est déplacée vers la ligne qui suit immédiatement la dernière ligne du jeu de lignes.
  
Lorsque _ulRowCount_ est défini sur zéro, demander l'ajout de lignes de titre zéro ou de niveau inférieur à la catégorie, ou la renvoi de lignes null est possible, car il n'existe aucune ligne de titre de niveau inférieur ou de niveau inférieur dans la catégorie, la position de BOOKMARK_CURRENT est définie sur la ligne suivi de la ligne identifiée par _pbInstanceKey_. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Ne générez pas de notifications sur les lignes ajoutées à une vue de table en raison de l'expansion de catégorie.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Le nombre de lignes dans l'ensemble de lignes désigné par le paramètre _lppRows_ ne peut pas être égal au nombre de lignes réellement ajoutées à la table, l'ensemble de lignes feuille ou de titre de niveau inférieur de la catégorie. Des erreurs peuvent se produire, comme une mémoire insuffisante ou le nombre de lignes de la catégorie dépassant le nombre spécifié dans le paramètre _ulRowCount_ . Dans les deux cas, BOOKMARK_CURRENT est positionné sur la dernière ligne renvoyée. Pour récupérer immédiatement les autres lignes de la catégorie, appelez [IMAPITable:: QueryRows](imapitable-queryrows.md).
  
Ne prévoyez pas de recevoir une notification de table lorsqu'une catégorie modifie son état. Vous pouvez gérer un cache local de lignes qui peuvent être mis à jour à chaque appel de **ExpandRow** ou de **CollapseRow** . 
  
Pour plus d'informations sur les tables classées, reportez-vous à la rubrique [Tri et catégorisation](sorting-and-categorization.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> |CContentsTableListCtrl::D oExpandCollapse  <br/> |MFCMAPI utilise la méthode **IMAPITable:: ExpandRow** pour développer une catégorie de table réduite.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable::CollapseRow](imapitable-collapserow.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

