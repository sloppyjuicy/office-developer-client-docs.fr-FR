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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5e2ce756baaefef7bd0028e746b1dbe10756365e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415165"
---
# <a name="imapitableexpandrow"></a>IMAPITable::ExpandRow

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Développe une catégorie de tableaux réduit, en ajoutant les lignes de titre de niveau inférieur ou feuille appartenant à la catégorie à l’affichage tableau.
  
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
  
> [in] Nombre d’octets dans la propriété PR_INSTANCE_KEY pointant vers le _paramètre pbInstanceKey._ 
    
 _pbInstanceKey_
  
> [in] Pointeur vers la **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) qui identifie la ligne de titre de la catégorie. 
    
 _ulRowCount_
  
> [in] Nombre maximal de lignes à renvoyer dans le _paramètre lppRows._ 
    
 _ulFlags_
  
> Réservé ; doit être zéro.
    
 _lppRows_
  
> [out] Pointeur vers une structure [SRowSet](srowset.md) recevant les premières lignes (jusqu’à  _ulRowCount)_ qui ont été insérées dans l’affichage Tableau suite à l’expansion. Ces lignes sont insérées après la ligne de titre identifiée par le _paramètre pbInstanceKey._ Le  _paramètre lppRows_ peut être NULL si  _le paramètre ulRowCount_ est zéro. 
    
 _lpulMoreRows_
  
> [out] Pointeur vers le nombre total de lignes ajoutées à l’affichage Tableau.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La catégorie a été étendue avec succès.
    
MAPI_E_NOT_FOUND 
  
> La ligne identifiée par le  _paramètre pbInstanceKey_ n’existe pas. 
    
## <a name="remarks"></a>Remarques

La **méthode IMAPITable::ExpandRow** développe une catégorie de tableaux réduit, en ajoutant les lignes de titre de niveau inférieur ou feuille qui appartiennent à la catégorie à l’affichage Tableau. Une limite au nombre de lignes à retourner dans le paramètre _lppRows_ peut être spécifiée dans le _paramètre ulRowCount._ Lorsque  _ulRowCount_ est définie sur une valeur supérieure à zéro et qu’une ou plusieurs lignes sont renvoyées dans le jeu de lignes pointé par  _lppRows,_ la position du signet BOOKMARK_CURRENT est déplacée vers la ligne qui suit immédiatement la dernière ligne du jeu de lignes.
  
Lorsque  _ulRowCount_ est défini sur zéro, en demandant l’ajout de lignes d’en-tête de feuille ou de bas niveau à la catégorie, ou qu’il n’y a aucune ligne de titre de niveau inférieur ou feuille dans la catégorie, la position de BOOKMARK_CURRENT est définie sur la ligne qui suit la ligne identifiée par  _pbInstanceKey_. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Ne générez pas de notifications sur les lignes qui sont ajoutées à un affichage tableau en raison de l’extension de catégorie.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Le nombre de lignes dans le jeu de lignes pointé par le paramètre  _lppRows_ peut ne pas être égal au nombre de lignes réellement ajoutées au tableau, à l’ensemble des lignes de titre de niveau inférieur ou feuille pour la catégorie. Des erreurs peuvent se produire, telles qu’une mémoire insuffisante ou le nombre de lignes de la catégorie dépassant le nombre spécifié dans _le paramètre ulRowCount._ Dans les deux cas, BOOKMARK_CURRENT sera positionné à la dernière ligne renvoyée. Pour récupérer immédiatement le reste des lignes de la catégorie, appelez [IMAPITable::QueryRows](imapitable-queryrows.md).
  
Ne vous attendez pas à recevoir une notification de tableau lorsqu’une catégorie change d’état. Vous pouvez gérer un cache local de lignes qui peut être mis à jour avec chaque **appel ExpandRow** **ou CollapseRow.** 
  
Pour plus d’informations sur les tableaux classés, voir [Tri et catégorisation.](sorting-and-categorization.md)
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::D oExpandCollapse  <br/> |MFCMAPI utilise la **méthode IMAPITable::ExpandRow** pour développer une catégorie de tableaux réduire.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable::CollapseRow](imapitable-collapserow.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

