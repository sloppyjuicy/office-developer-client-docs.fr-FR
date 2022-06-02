---
title: IMAPITableExpandRow
description: IMAPITableExpandRow développe une catégorie de table réduite, en ajoutant les lignes d’en-tête feuille ou de niveau inférieur appartenant à la catégorie à la vue de table.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.ExpandRow
api_type:
- COM
ms.assetid: b96dd8f6-e648-4014-8a1d-ae1da771c439
ms.openlocfilehash: 7c7f12e03cda37ec810f0ba65eb84657d8e828e7
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65827855"
---
# <a name="imapitableexpandrow"></a>IMAPITable::ExpandRow

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Développe une catégorie de table réduite, en ajoutant les lignes d’en-tête de feuille ou de niveau inférieur appartenant à la catégorie à la vue de table.
  
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
  
> [in] Nombre d’octets dans la propriété PR_INSTANCE_KEY pointée par le paramètre  _pbInstanceKey_ . 
    
 _pbInstanceKey_
  
> [in] Pointeur vers la propriété **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) qui identifie la ligne de titre de la catégorie. 
    
 _ulRowCount_
  
> [in] Nombre maximal de lignes à retourner dans le paramètre _lppRows_ . 
    
 _ulFlags_
  
> Réservé; doit être égal à zéro.
    
 _lppRows_
  
> [out] Pointeur vers une structure [SRowSet](srowset.md) recevant les premières lignes (jusqu’à  _ulRowCount_) qui ont été insérées dans la vue de table suite à l’expansion. Ces lignes sont insérées après la ligne de titre identifiée par le paramètre  _pbInstanceKey_ . Le paramètre  _lppRows_ peut être NULL si le paramètre _ulRowCount_ est égal à zéro. 
    
 _lpulMoreRows_
  
> [out] Pointeur vers le nombre total de lignes qui ont été ajoutées à la vue de table.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La catégorie a été développée avec succès.
    
MAPI_E_NOT_FOUND 
  
> La ligne identifiée par le paramètre  _pbInstanceKey_ n’existe pas. 
    
## <a name="remarks"></a>Remarques

La méthode **IMAPITable::ExpandRow** développe une catégorie de table réduite, en ajoutant les lignes d’en-tête feuille ou inférieure qui appartiennent à la catégorie à la vue de table. Une limite au nombre de lignes à retourner dans le paramètre _lppRows_ peut être spécifiée dans le paramètre _ulRowCount_ . Lorsque  _ulRowCount_ est défini sur une valeur supérieure à zéro et qu’une ou plusieurs lignes sont retournées dans l’ensemble de lignes pointé par  _lppRows_, la position du signet BOOKMARK_CURRENT est déplacée vers la ligne immédiatement après la dernière ligne du jeu de lignes.
  
Lorsque  _ulRowCount_ est défini sur zéro, en demandant que les lignes de titre de niveau zéro feuille ou de niveau inférieur soient ajoutées à la catégorie, ou si aucune ligne n’est retournée, car il n’existe aucune ligne de titre feuille ou de niveau inférieur dans la catégorie, la position de BOOKMARK_CURRENT est définie sur la ligne qui suit la ligne identifiée par  _pbInstanceKey_. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Ne générez pas de notifications sur les lignes qui sont ajoutées à une vue de table en raison de l’expansion des catégories.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Le nombre de lignes dans l’ensemble de lignes pointé par le paramètre  _lppRows_ peut ne pas être égal au nombre de lignes réellement ajoutées à la table, l’ensemble entier de lignes de titre de feuille ou de niveau inférieur pour la catégorie. Des erreurs peuvent se produire, comme une mémoire insuffisante ou le nombre de lignes dans la catégorie dépassant le nombre spécifié dans le paramètre  _ulRowCount_ . Dans les deux cas, BOOKMARK_CURRENT sera positionné à la dernière ligne retournée. Pour récupérer immédiatement les autres lignes de la catégorie, appelez [IMAPITable::QueryRows](imapitable-queryrows.md).
  
Ne vous attendez pas à recevoir une notification de table lorsqu’une catégorie change d’état. Vous pouvez gérer un cache local de lignes qui peuvent être mises à jour à chaque appel **ExpandRow** ou **CollapseRow** . 
  
Pour plus d’informations sur les tables catégorisées, consultez [Tri et catégorisation](sorting-and-categorization.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::D oExpandCollapse  <br/> |MFCMAPI utilise la méthode **IMAPITable::ExpandRow** pour développer une catégorie de table réduite. |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable::CollapseRow](imapitable-collapserow.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

