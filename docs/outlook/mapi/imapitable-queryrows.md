---
title: IMAPITableQueryRows
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QueryRows
api_type:
- COM
ms.assetid: f26384f1-467e-4343-92b3-0425da9d2123
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 26d6ffe66a5e7749c9d8c4e5210e9f72de808932
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328868"
---
# <a name="imapitablequeryrows"></a>IMAPITable::QueryRows

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie une ou plusieurs lignes d'un tableau, en commençant à la position actuelle du curseur.
  
```cpp
HRESULT QueryRows(
LONG lRowCount,
ULONG ulFlags,
LPSRowSet FAR * lppRows
);
```

## <a name="parameters"></a>Paramètres

 _lRowCount_
  
> dans Nombre maximal de lignes à renvoyer.
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôlent la façon dont les lignes sont renvoyées. L'indicateur suivant peut être défini:
    
TBL_NOADVANCE 
  
> Empêche le curseur de progresser à la suite de la récupération de la ligne. Si l'indicateur TBL_NOADVANCE est défini, le curseur pointe vers la première ligne renvoyée. Si l'indicateur TBL_NOADVANCE n'est pas défini, le curseur pointe sur la ligne suivant la dernière ligne renvoyée.
    
 _lppRows_
  
> remarquer Pointeur vers un pointeur vers une structure [SRowSet](srowset.md) contenant les lignes de tableau. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les lignes ont été renvoyées avec succès.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours, ce qui empêche le démarrage de l'opération de récupération de ligne. L'opération en cours doit être autorisée ou elle doit être arrêtée.
    
MAPI_E_INVALID_PARAMETER 
  
> Le paramètre _IRowCount_ est défini sur zéro. 
    
## <a name="remarks"></a>Remarques

La méthode **IMAPITable:: QueryRows** obtient une ou plusieurs lignes de données d'une table. La valeur du paramètre _IRowCount_ affecte le point de départ de la récupération. Si _IRowCount_ est positif, les lignes sont lues dans une direction de transfert, en commençant à la position actuelle. Si _IRowCount_ est négatif, **QueryRows** réinitialise le point de départ en dépassant le nombre indiqué de lignes. Une fois le curseur réinitialisé, les lignes sont lues dans l'ordre de transfert. 
  
Le **** membre Crows dans la structure [SRowSet](srowset.md) vers laquelle pointe le paramètre _lppRows_ indique le nombre de lignes renvoyées. Si aucune ligne n'est renvoyée: 
  
- Le curseur était déjà positionné au début de la table et la valeur de _IRowCount_ est négative. Des 
    
- Le curseur a déjà été positionné à la fin de la table et la valeur de _IRowCount_ est positive. 
    
Le nombre de colonnes et leur ordre sont les mêmes pour chaque ligne. Si une propriété n'existe pas pour une ligne ou s'il y a une erreur lors de la lecture d'une propriété, la structure **SPropValue** de la propriété dans la ligne contient les valeurs suivantes: 
  
- PT_ERROR pour le type de propriété dans le membre **ulPropTag** . 
    
- MAPI_E_NOT_FOUND pour le membre de la **valeur** . 
    
La mémoire utilisée pour les structures [SPropValue](spropvalue.md) dans l'ensemble de lignes pointé par le paramètre _lppRows_ doit être allouée et libérée séparément pour chaque ligne. Utilisez [MAPIFreeBuffer](mapifreebuffer.md) pour libérer les structures de valeur de propriété et libérer le jeu de lignes. Quand un appel à **QueryRows** renvoie zéro, toutefois, en indiquant le début ou la fin de la table, seule la structure **SRowSet** elle-même doit être libérée. Pour plus d'informations sur la façon d'allouer et de libérer de la mémoire dans une structure **SRowSet** , consultez la rubrique [Managing Memory for ADRLIST and SRowSet structures](managing-memory-for-adrlist-and-srowset-structures.md).
  
Les lignes renvoyées et l'ordre dans lequel elles sont renvoyées dépendent du fait que des appels ont été effectués ou non comme suit: [: Restrict](imapitable-restrict.md) et [IMAPITable:: SortTable](imapitable-sorttable.md). **Limiter** les lignes de filtrage à partir de l'affichage, entraînAnt la **QueryRows** à renvoyer uniquement les lignes correspondant aux critères spécifiés dans la restriction. **SortTable** établit un ordre de tri standard ou par catégorie, affectant la séquence de lignes renvoyées par **QueryRows**. Les lignes renvoyées sont dans l'ordre spécifié dans la structure [SSortOrderSet](ssortorderset.md) transmise à **SortTable**.
  
Les colonnes renvoyées pour chaque ligne et l'ordre dans lequel elles sont renvoyées dépendent du succès ou non de l'appel de la fonction [IMAPITable:: SetColumns](imapitable-setcolumns.md). **SetColumns** établit un jeu de colonnes, en spécifiant les propriétés à inclure dans les colonnes du tableau et l'ordre dans lequel elles doivent être incluses. Si un appel **SetColumns** a été effectué, les colonnes spécifiques de chaque ligne et l'ordre de ces colonnes correspondent au jeu de colonnes spécifié dans l'appel. Si aucun appel de **SetColumns** n'a été effectué, le tableau renvoie son jeu de colonnes par défaut. 
  
Si aucun de ces appels n'a été effectué, **QueryRows** renvoie toutes les lignes du tableau. Chaque ligne contient la colonne par défaut définie dans l'ordre par défaut. 
  
Lorsque le jeu de colonnes établi dans un appel de la PR_NULL: [SetColumns](imapitable-setcolumns.md) inclut des colonnes définies sur, le tableau [SPropValue](spropvalue.md) dans le jeu de lignes renvoyé dans _lppRows_ contiendra des slots vides. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Vous pouvez permettre à un appelant de demander qu'une colonne non prise en charge soit incluse dans le jeu de colonnes. Lorsque cela se produit, placez PT_ERROR dans la partie type de propriété de la balise de propriété et MAPI_E_NOT_FOUND dans la valeur de propriété pour la colonne non prise en charge. 
  
Traite le nombre de lignes comme une demande plutôt qu'une exigence. Vous pouvez renvoyer n'importe quel emplacement à partir de zéro ligne, s'il n'y a aucune ligne dans le sens de la requête, vers le nombre demandé. 
  
Renvoyer uniquement les lignes que l'utilisateur verra quand des lignes sont demandées à partir d'une vue de table classée, ce qui permet à l'appelant de formuler des hypothèses valides sur l'étendue des données et d'éviter tout travail supplémentaire. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

En règle générale, vous vous retrouvez avec autant de lignes que vous avez spécifiées dans le paramètre _lRowCount_ . Toutefois, lorsque la mémoire ou les limites d'implémentation posent problème ou lorsque l'opération atteint le début ou la fin de la table de façon prématurée, **QueryRows** renvoie moins de lignes que le nombre demandé. 
  
Si **QueryRows** renvoie MAPI_E_BUSY, appelez la méthode [IMAPITable:: WaitForCompletion](imapitable-waitforcompletion.md) et renouvelez l'appel à **QueryRows** une fois l'opération asynchrone terminée. 
  
Lors de l'appel de **QueryRows**, sachez que le temps de notifications asynchrones peut potentiellement provoquer l'ensemble de lignes que vous obtenez de **QueryRows** afin de ne pas représenter correctement les données sous-jacentes. Par exemple, un appel à **QueryRows** à la table de contenu d'un dossier à la suite de la suppression d'un message, mais avant la réception de la notification correspondante, entraîne le renvoi de la ligne Deleted dans l'ensemble de lignes. Attendez toujours qu'une notification arrive avant de mettre à jour la vue des données de l'utilisateur. 
  
Pour plus d'informations sur la récupération de lignes de tables, consultez la rubrique [extraction de données à partir de lignes de table](retrieving-data-from-table-rows.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> |DwThreadFuncLoadTable  <br/> |MFCMAPI utilise la méthode **IMAPITable:: QueryRows** pour récupérer les lignes de la table à charger dans la vue.  <br/> |
   
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

