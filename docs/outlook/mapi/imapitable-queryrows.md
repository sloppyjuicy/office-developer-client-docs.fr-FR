---
title: IMAPITableQueryRows
description: IMAPITableQueryRows retourne une ou plusieurs lignes d’une table, en commençant à la position actuelle du curseur.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.QueryRows
api_type:
- COM
ms.assetid: f26384f1-467e-4343-92b3-0425da9d2123
ms.openlocfilehash: 147010f12a83c946bb38ffa938d38ad1c9f529bb
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65827820"
---
# <a name="imapitablequeryrows"></a>IMAPITable::QueryRows

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Retourne une ou plusieurs lignes d’une table, en commençant à la position actuelle du curseur.
  
```cpp
HRESULT QueryRows(
LONG lRowCount,
ULONG ulFlags,
LPSRowSet FAR * lppRows
);
```

## <a name="parameters"></a>Paramètres

 _lRowCount_
  
> [in] Nombre maximal de lignes à renvoyer.
    
 _ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôlent la façon dont les lignes sont retournées. L’indicateur suivant peut être défini :
    
TBL_NOADVANCE 
  
> Empêche le curseur d’avancer à la suite de la récupération de ligne. Si l’indicateur TBL_NOADVANCE est défini, le curseur pointe vers la première ligne retournée. Si l’indicateur TBL_NOADVANCE n’est pas défini, le curseur pointe vers la ligne qui suit la dernière ligne retournée.
    
 _lppRows_
  
> [out] Pointeur vers un pointeur vers une structure [SRowSet](srowset.md) contenant les lignes de table. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les lignes ont été retournées avec succès.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours qui empêche le démarrage de l’opération de récupération de ligne. Soit l’opération en cours doit être autorisée à se terminer, soit elle doit être arrêtée.
    
MAPI_E_INVALID_PARAMETER 
  
> Le paramètre  _IRowCount_ est défini sur zéro. 
    
## <a name="remarks"></a>Remarques

La méthode **IMAPITable::QueryRows** obtient une ou plusieurs lignes de données d’une table. La valeur du paramètre  _IRowCount_ affecte le point de départ de la récupération. Si  _IRowCount_ est positif, les lignes sont lues dans un sens avant, en commençant à la position actuelle. Si  _IRowCount_ est négatif, **QueryRows** réinitialise le point de départ en descendant le nombre de lignes indiqué. Une fois le curseur réinitialisé, les lignes sont lues dans l’ordre avant. 
  
Le membre **cRows** dans la structure [SRowSet](srowset.md) pointé par le paramètre  _lppRows_ indique le nombre de lignes retournées. Si aucune ligne n’est retournée : 
  
- Le curseur était déjà positionné au début de la table et la valeur  _d’IRowCount_ est négative. -Ou- 
    
- Le curseur était déjà positionné à la fin de la table et la valeur  _d’IRowCount_ est positive. 
    
Le nombre de colonnes et leur ordre sont identiques pour chaque ligne. S’il n’existe pas de propriété pour une ligne ou s’il y a une erreur lors de la lecture d’une propriété, la structure **SPropValue** de la propriété de la ligne contient les valeurs suivantes : 
  
- PT_ERROR pour le type de propriété dans le membre **ulPropTag** . 
    
- MAPI_E_NOT_FOUND pour le membre **Value** . 
    
La mémoire utilisée pour les structures [SPropValue](spropvalue.md) dans l’ensemble de lignes pointé par le paramètre  _lppRows_ doit être allouée séparément et libérée pour chaque ligne. Utilisez [MAPIFreeBuffer](mapifreebuffer.md) pour libérer les structures de valeur de propriété et libérer le jeu de lignes. Toutefois, lorsqu’un appel à **QueryRows** retourne zéro, indiquant le début ou la fin de la table, seule la structure **SRowSet** elle-même doit être libérée. Pour plus d’informations sur l’allocation et la libération de mémoire dans une structure **SRowSet** , consultez [Gestion de la mémoire pour les structures ADRLIST et SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).
  
Les lignes retournées et l’ordre dans lequel elles sont retournées dépendent de la réussite ou non des appels à [IMAPITable::Restrict](imapitable-restrict.md) et [IMAPITable::SortTable](imapitable-sorttable.md). **Restreignez** les lignes des filtres de la vue, ce qui fait **que QueryRows** retourne uniquement les lignes qui correspondent aux critères spécifiés dans la restriction. **SortTable** établit un ordre de tri standard ou catégorisé, affectant la séquence de lignes retournées par **QueryRows**. Les lignes retournées sont dans l’ordre spécifié dans la structure [SSortOrderSet](ssortorderset.md) passée à **SortTable**.
  
Les colonnes retournées pour chaque ligne et l’ordre dans lequel elles sont retournées dépendent de la réussite ou non d’un appel à [IMAPITable::SetColumns](imapitable-setcolumns.md). **SetColumns** établit un jeu de colonnes, en spécifiant les propriétés à inclure dans les colonnes de la table et l’ordre dans lequel elles doivent être incluses. Si un appel **SetColumns** a été effectué, les colonnes particulières de chaque ligne et l’ordre de ces colonnes correspondent au jeu de colonnes spécifié dans l’appel. Si aucun appel **SetColumns** n’a été effectué, la table retourne son jeu de colonnes par défaut. 
  
Si aucun de ces appels n’a été effectué, **QueryRows** retourne toutes les lignes de la table. Chaque ligne contient l’ensemble de colonnes par défaut dans l’ordre par défaut. 
  
Lorsque l’ensemble de colonnes établi dans un appel à [IMAPITable::SetColumns inclut des colonnes définies](imapitable-setcolumns.md) sur PR_NULL, le tableau [SPropValue](spropvalue.md) dans l’ensemble de  _lignes retourné dans lppRows contient des_ emplacements vides. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Vous pouvez autoriser un appelant à demander qu’une colonne non prise en charge soit incluse dans le jeu de colonnes. Dans ce cas, placez PT_ERROR dans la partie type de propriété de la balise de propriété et MAPI_E_NOT_FOUND dans la valeur de propriété de la colonne non prise en charge. 
  
Traitez le nombre de lignes comme une requête plutôt qu’une exigence. Vous pouvez retourner n’importe où à partir de zéro ligne, s’il n’y a pas de lignes dans le sens de la requête, au nombre demandé. 
  
Retourne uniquement les lignes que l’utilisateur verra lorsque des lignes sont demandées à partir d’une vue de table classée, ce qui permet à l’appelant de faire des hypothèses valides sur l’étendue des données et d’éviter un travail supplémentaire. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

En règle générale, vous vous retrouvez avec autant de lignes que vous l’avez spécifié dans le paramètre _lRowCount_ . Toutefois, lorsque les limites de mémoire ou d’implémentation sont un problème ou lorsque l’opération atteint le début ou la fin prématurément de la table, **QueryRows** retourne moins de lignes que demandé. 
  
Si **QueryRows** retourne MAPI_E_BUSY, appelez la méthode [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) et réessayez l’appel à **QueryRows** lorsque l’opération asynchrone est terminée. 
  
Lors de **l’appel de QueryRows**, sachez que le minutage des notifications asynchrones peut potentiellement empêcher le jeu de lignes que vous obtenez de **QueryRows** de représenter avec précision les données sous-jacentes. Par exemple, un appel à **QueryRows** à la table de contenu d’un dossier après la suppression d’un message, mais avant la réception de la notification correspondante entraîne le retour de la ligne supprimée dans le jeu de lignes. Attendez toujours qu’une notification arrive avant de mettre à jour l’affichage des données par l’utilisateur. 
  
Pour plus d’informations sur la récupération de lignes à partir de tables, consultez [Récupération de données à partir de lignes de table](retrieving-data-from-table-rows.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |DwThreadFuncLoadTable  <br/> |MFCMAPI utilise la méthode **IMAPITable::QueryRows** pour récupérer les lignes de la table à charger dans la vue. |
   
## <a name="see-also"></a>Voir aussi



[ADRENTRY](adrentry.md)
  
[FreeProws](freeprows.md)
  
[HrQueryAllRows](hrqueryallrows.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SRow](srow.md)
  
[SRowSet](srowset.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

