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
ms.openlocfilehash: 1b3d8c74d85696e733b378a4cac2b8e2a3b6a072
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784069"
---
# <a name="imapitableexpandrow"></a>IMAPITable::ExpandRow

  
  
**S’applique à**: Outlook 
  
Développe une catégorie de table réduite, ajout de la feuille ou des lignes d’en-tête de niveau inférieur appartenant à la catégorie à l’affichage tableau.
  
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
  
> [in] Le nombre d’octets dans la propriété PR_INSTANCE_KEY indiqué par le paramètre _pbInstanceKey_ . 
    
 _pbInstanceKey_
  
> [in] Pointeur vers la propriété **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) qui identifie la ligne d’en-tête de la catégorie. 
    
 _ulRowCount_
  
> [in] Le nombre maximal de lignes à renvoyer dans le paramètre _lppRows_ . 
    
 _ulFlags_
  
> Réservé ; doit être égal à zéro.
    
 _lppRows_
  
> [out] Pointeur vers une structure [SRowSet](srowset.md) recevoir des lignes qui ont été insérés dans la vue table à la suite de l’extension de la première (jusqu'à _ulRowCount_). Ces lignes sont insérées après la ligne d’en-tête identifiée par le paramètre _pbInstanceKey_ . Le paramètre _lppRows_ peut être NULL si le paramètre _ulRowCount_ est égale à zéro. 
    
 _lpulMoreRows_
  
> [out] Pointeur vers le nombre total de lignes qui ont été ajoutés à l’affichage tableau.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> La catégorie a été développée avec succès.
    
MAPI_E_NOT_FOUND 
  
> La ligne identifiée par le paramètre _pbInstanceKey_ n’existe pas. 
    
## <a name="remarks"></a>Remarques

La méthode **IMAPITable::ExpandRow** développe une catégorie de table réduite, ajout de la feuille ou les lignes d’en-tête de niveau inférieur qui appartiennent à la catégorie à l’affichage tableau. Limite le nombre de lignes à renvoyer dans le paramètre _lppRows_ peut être spécifiée dans le paramètre _ulRowCount_ . Lorsque _ulRowCount_ est défini sur une valeur supérieure à zéro, une ou plusieurs lignes sont retournées dans le jeu de lignes indiqué par _lppRows_la position du signet que bookmark_current est déplacé vers la ligne immédiatement après la dernière ligne de la ligne est définie.
  
Lorsque _ulRowCount_ est égale à zéro, demande qui zéro feuille ou lignes d’en-tête de niveau inférieur à ajouter à la catégorie ou zéro lignes sont retournées, car aucune feuille ou les lignes d’en-tête de niveau inférieur de la catégorie, la position de BOOKMARK_CURRENT est définie à la ligne la ligne identifié par _pbInstanceKey_. 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Ne génèrent pas de notifications sur les lignes qui sont ajoutés à un affichage de tableau en raison d’extension de catégorie.
  
## <a name="notes-to-callers"></a>Notes aux appelants

Le nombre de lignes dans le jeu de lignes indiqué par le paramètre _lppRows_ ne peut pas égal au nombre de lignes qui ont été ajoutés à la table, l’ensemble de la définir de feuille ou de lignes pour la catégorie d’en-tête de niveau inférieur. Erreurs peuvent se produire, telles que la mémoire ou le nombre de lignes dans la catégorie dépassant le nombre spécifié dans le paramètre _ulRowCount_ . Dans les deux cas, BOOKMARK_CURRENT sera positionné à la dernière ligne renvoyée. Pour récupérer immédiatement le reste des lignes de la catégorie, appelez [IMAPITable::QueryRows](imapitable-queryrows.md).
  
Ne prévoyez pas de recevoir une notification de table lorsqu’une catégorie modifie son état. Vous pouvez conserver un cache local des lignes qui peuvent être mises à jour à chaque appel **ExpandRow** ou **CollapseRow** . 
  
Pour plus d’informations sur les tables, voir, consultez [tri et catégorisation](sorting-and-categorization.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::DoExpandCollapse  <br/> |MFCMAPI utilise la méthode **IMAPITable::ExpandRow** pour développer une catégorie de table réduite.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable::CollapseRow](imapitable-collapserow.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

