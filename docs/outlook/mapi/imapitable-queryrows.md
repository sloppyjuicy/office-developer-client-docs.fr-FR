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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 26d6ffe66a5e7749c9d8c4e5210e9f72de808932
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416292"
---
# <a name="imapitablequeryrows"></a>IMAPITable::QueryRows

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie une ou plusieurs lignes d’un tableau, en commençant à la position actuelle du curseur.
  
```cpp
HRESULT QueryRows(
LONG lRowCount,
ULONG ulFlags,
LPSRowSet FAR * lppRows
);
```

## <a name="parameters"></a>Parameters

 _lRowCount_
  
> [in] Nombre maximal de lignes à retourner.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôlent la façon dont les lignes sont renvoyées. L’indicateur suivant peut être définie :
    
TBL_NOADVANCE 
  
> Empêche le curseur d’avancer suite à la récupération de ligne. Si l TBL_NOADVANCE est définie, le curseur pointe vers la première ligne renvoyée. Si l TBL_NOADVANCE n’est pas définie, le curseur pointe vers la ligne qui suit la dernière ligne renvoyée.
    
 _lppRows_
  
> [out] Pointeur vers un pointeur vers une structure [SRowSet](srowset.md) qui détient les lignes du tableau. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les lignes ont été renvoyées avec succès.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours qui empêche le démarrage de l’opération de récupération de lignes. L’opération en cours doit être autorisée ou arrêtée.
    
MAPI_E_INVALID_PARAMETER 
  
> Le  _paramètre IRowCount_ est définie sur zéro. 
    
## <a name="remarks"></a>Remarques

La **méthode IMAPITable::QueryRows** obtient une ou plusieurs lignes de données d’une table. La valeur du  _paramètre IRowCount_ affecte le point de départ de la récupération. Si  _IRowCount est_ positif, les lignes sont lues dans une direction vers l’avant, en commençant à la position actuelle. Si  _IRowCount est_ négatif, **QueryRows** réinitialise le point de départ en déplaçant le nombre de lignes indiqué vers l’arrière. Une fois le curseur réinitialisé, les lignes sont lues dans l’ordre avant. 
  
Le **membre cRows** dans la structure [SRowSet](srowset.md) pointée par le paramètre  _lppRows_ indique le nombre de lignes renvoyées. Si aucune ligne n’est renvoyée : 
  
- Le curseur était déjà positionné au début du tableau et la valeur  _de IRowCount_ est négative. -Or- 
    
- Le curseur était déjà positionné à la fin du tableau et la valeur de  _IRowCount_ est positive. 
    
Le nombre de colonnes et leur ordre sont les mêmes pour chaque ligne. Si une propriété n’existe pas pour une ligne ou s’il existe une erreur lors de la lecture d’une propriété, la structure **SPropValue** de la propriété de la ligne contient les valeurs suivantes : 
  
- PT_ERROR type de propriété dans le **membre ulPropTag.** 
    
- MAPI_E_NOT_FOUND pour le **membre Valeur.** 
    
La mémoire utilisée pour les structures [SPropValue](spropvalue.md) dans le jeu de lignes pointé par le paramètre  _lppRows_ doit être allouée séparément et libérée pour chaque ligne. Utilisez [MAPIFreeBuffer pour](mapifreebuffer.md) libérer les structures de valeurs de propriété et pour libérer le jeu de lignes. Toutefois, lorsqu’un appel **à QueryRows** renvoie zéro, indiquant le début ou la fin de la table, seule la structure **SRowSet** elle-même doit être libérée. Pour plus d’informations sur la façon d’allouer et de libérer de la mémoire dans une structure **SRowSet,** voir [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).
  
Les lignes renvoyées et l’ordre dans lequel elles sont renvoyées varient selon que des appels réussis ont été effectués ou non à [IMAPITable::Restrict](imapitable-restrict.md) et [IMAPITable::SortTable](imapitable-sorttable.md). **Limitez** les filtres des lignes de l’affichage, ce qui a pour effet **que QueryRows** ne retourne que les lignes qui correspondent aux critères spécifiés dans la restriction. **SortTable** établit un ordre de tri standard ou catégorisé, affectant la séquence de lignes renvoyée par **QueryRows**. Les lignes renvoyées sont dans l’ordre spécifié dans la structure [SSortOrderSet](ssortorderset.md) transmise **à SortTable**.
  
Les colonnes renvoyées pour chaque ligne et l’ordre dans lequel elles sont renvoyées varient selon qu’un appel réussi a été effectué ou non à [IMAPITable::SetColumns](imapitable-setcolumns.md). **SetColumns** établit un jeu de colonnes, en spécifiant les propriétés à inclure dans les colonnes du tableau et l’ordre dans lequel elles doivent être incluses. Si un **appel SetColumns** a été effectué, les colonnes spécifiques de chaque ligne et l’ordre de ces colonnes correspondent à l’ensemble de colonnes spécifié dans l’appel. Si aucun **appel SetColumns n’a** été effectué, la table renvoie son jeu de colonnes par défaut. 
  
Si aucun de ces appels n’a été effectué, **QueryRows** renvoie toutes les lignes du tableau. Chaque ligne contient la colonne par défaut définie dans l’ordre par défaut. 
  
Lorsque le jeu de colonnes établi dans un appel à [IMAPITable::SetColumns](imapitable-setcolumns.md) inclut des colonnes définies sur PR_NULL, le tableau [SPropValue](spropvalue.md) dans le jeu de lignes renvoyé dans  _lppRows_ contient des emplacements vides. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Vous pouvez autoriser un appelant à demander qu’une colonne non pris en compte soit incluse dans le jeu de colonnes. Lorsque cela se produit, placez PT_ERROR dans la partie type de propriété de la balise de propriété et MAPI_E_NOT_FOUND dans la valeur de la propriété pour la colonne non pris en MAPI_E_NOT_FOUND. 
  
Traite le nombre de lignes comme une demande plutôt qu’une exigence. Vous pouvez revenir n’importe où de zéro ligne, s’il n’y a aucune ligne dans la direction de la requête, au numéro demandé. 
  
Renvoyer uniquement les lignes que l’utilisateur verra lorsque des lignes sont demandées à partir d’une vue de table classée, ce qui permet à l’appelant d’effectuer des hypothèses valides sur l’étendue des données et d’éviter tout travail supplémentaire. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

En règle générale, vous finirez par avoir autant de lignes que vous l’avez spécifié dans _le paramètre lRowCount._ Toutefois, lorsque les limites de mémoire ou d’implémentation sont un problème ou lorsque l’opération atteint le début ou la fin de la table prématurément, **QueryRows** retourne moins de lignes que demandé. 
  
Si **QueryRows** renvoie MAPI_E_BUSY, appelez la méthode [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) et réessayez l’appel à **QueryRows** une fois l’opération asynchrone terminée. 
  
Lorsque vous appelez **QueryRows,** sachez que le minutage des notifications asynchrones peut potentiellement entraîner le fait que le jeu de lignes que vous obtenez à partir de **QueryRows** ne représente pas précisément les données sous-jacentes. Par exemple, un appel de **QueryRows** à la table des matières d’un dossier après la suppression d’un message mais avant la réception de la notification correspondante entraîne le retour de la ligne supprimée dans le jeu de lignes. Attendez toujours l’arrivée d’une notification avant de mettre à jour la vue des données de l’utilisateur. 
  
Pour plus d’informations sur la récupération de lignes à partir de tables, voir Récupération des données à partir des [lignes de tableau.](retrieving-data-from-table-rows.md)
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |DwThreadFuncLoadTable  <br/> |MFCMAPI utilise la **méthode IMAPITable::QueryRows** pour récupérer les lignes de la table à charger dans l’affichage.  <br/> |
   
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

