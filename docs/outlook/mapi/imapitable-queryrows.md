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
ms.openlocfilehash: 179d76b56c1ba9b40768c691d0b1555377f7adb7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595047"
---
# <a name="imapitablequeryrows"></a>IMAPITable::QueryRows

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie une ou plusieurs lignes d’une table, en commençant à l’emplacement du curseur.
  
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
  
> [in] Masque de bits d’indicateurs qui contrôlent la façon dont les lignes sont retournées. Vous pouvez définir l’indicateur suivant :
    
TBL_NOADVANCE 
  
> Empêche le curseur de passer à la suite de la récupération de la ligne. Si l’indicateur TBL_NOADVANCE est défini, les points de curseur à la première ligne renvoyée. Si l’indicateur TBL_NOADVANCE n’est pas définie, le curseur pointe vers la ligne qui suit la dernière ligne renvoyée.
    
 _lppRows_
  
> [out] Pointeur vers un pointeur vers une structure [SRowSet](srowset.md) contenant les lignes du tableau. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les lignes ont été correctement renvoyées.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours qui empêche l’opération de récupération de ligne de démarrage. L’opération en cours doit être autorisée à effectuer ou il doit être arrêté.
    
MAPI_E_INVALID_PARAMETER 
  
> Le paramètre _IRowCount_ est défini sur zéro. 
    
## <a name="remarks"></a>Remarques

La méthode **IMAPITable::QueryRows** Obtient une ou plusieurs lignes de données d’une table. La valeur du paramètre _IRowCount_ affecte le point de départ pour la récupération. Si _IRowCount_ est positif, les lignes sont lues dans une direction avant, en commençant à la position actuelle. Si _IRowCount_ est négatif, **QueryRows** réinitialise le point de départ en déplacement vers l’arrière du nombre spécifié de lignes. Une fois que le curseur est réinitialisé, les lignes sont lues dans l’ordre chronologique. 
  
Le membre **cRows** dans la structure [SRowSet](srowset.md) désigné par le paramètre _lppRows_ indique le nombre de lignes retournées. Si aucune ligne n’est retournée : 
  
- Le curseur a été déjà positionné au début de la table et la valeur de _IRowCount_ est négative. - Ou - 
    
- Le curseur était placé déjà à la fin de la table et la valeur de _IRowCount_ est positive. 
    
Le nombre de colonnes et leur ordre est le même pour chaque ligne. Si une propriété n’existe pas pour une ligne ou une erreur de lecture d’une propriété, la structure **SPropValue** pour la propriété dans la ligne contient les valeurs suivantes : 
  
- PT_ERROR pour le type de propriété dans le membre **ulPropTag** . 
    
- MAPI_E_NOT_FOUND du membre de **valeur** . 
    
Mémoire utilisée pour les structures [SPropValue](spropvalue.md) dans le jeu de lignes indiqué par le paramètre _lppRows_ doit être allouée et libérée pour chaque ligne séparément. Utilisez [MAPIFreeBuffer](mapifreebuffer.md) pour libérer les structures de valeur de propriété et pour libérer de la ligne. Lorsqu’un appel **QueryRows** renvoie zéro, toutefois, indiquant le début ou la fin de la table, uniquement la structure de **SRowSet** doit être libéré. Pour plus d’informations sur la façon d’allouer et de libérer de la mémoire dans une structure **SRowSet** , consultez [Gestion de la mémoire ADRLIST des Structures SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).
  
Les lignes qui sont retournées et l’ordre dans lequel ils sont retournés dépendent ou non les appels ayant abouti ont été apportées à [IMAPITable](imapitable-restrict.md) et [IMAPITable::SortTable](imapitable-sorttable.md). **Restrict** filtre les lignes de l’affichage, à l’origine de **QueryRows** retourner uniquement les lignes qui correspondent aux critères spécifiés dans la restriction. **SortTable** établit une norme ou de catégorie ordre de tri, affecter la séquence de lignes retournées par **QueryRows**. Les lignes renvoyées sont dans l’ordre spécifié dans la structure [SSortOrderSet](ssortorderset.md) transmise à **SortTable**.
  
Les colonnes renvoyées pour chaque ligne et l’ordre dans lequel ils sont retournés dépendent ou non un appel réussi a été apporté à [IMAPITable::SetColumns](imapitable-setcolumns.md). **SetColumns** établit un ensemble de colonnes, spécifiez les propriétés à inclure dans les colonnes du tableau et l’ordre dans lequel ils doivent être inclus. Si un appel de la **méthode SetColumns** a été effectué, les colonnes dans chaque ligne et l’ordre de ces colonnes particuliers correspond à la colonne spécifiée dans l’appel. Si aucun appel **SetColumns** n’a été effectué, la table renvoie son jeu de colonne par défaut. 
  
Si aucun de ces appels a été effectué, **QueryRows** renvoie toutes les lignes de la table. Chaque ligne contient la colonne par défaut définie dans l’ordre par défaut. 
  
Lorsque l’ensemble de colonnes d’établir un appel à [IMAPITable::SetColumns](imapitable-setcolumns.md) comprend les colonnes PR_NULL, tableau [SPropValue](spropvalue.md) dans le jeu de lignes retourné dans _lppRows_ contiendra des emplacements vides. 
  
## <a name="notes-to-implementers"></a>Remarques à l’attention des responsables de l’implémentation

Vous pouvez autoriser un appelant demander une colonne à inclure dans l’ensemble de colonnes non pris en charge. Lorsque cela se produit, placez PT_ERROR dans la partie de type de propriété de la balise de propriété et MAPI_E_NOT_FOUND dans la valeur de propriété pour la colonne non pris en charge. 
  
Traite le nombre de lignes comme une demande plutôt qu’une condition requise. Vous pouvez retourner de n’importe où à partir de zéro lignes, s’il n’y a aucune ligne dans le sens de la requête, le nombre demandé. 
  
Retourner uniquement les lignes que l’utilisateur s’affiche lorsque les lignes sont demandées à partir d’un affichage tableau classés, permettant à l’appelant d’effectuer des hypothèses valides sur l’étendue des données et éviter le travail supplémentaire. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Généralement vous finirez avec le même nombre de lignes que vous avez spécifié dans le paramètre _lRowCount_ . Toutefois, lorsque les limites de mémoire ou de mise en œuvre un problème ou lorsque l’opération atteint le début ou la fin de la table prématurément, **QueryRows** retourne moins de lignes que vous avez demandé. 
  
Si **QueryRows** renvoie MAPI_E_BUSY, appelez la méthode [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) et réessayez l’appel **QueryRows** lorsque l’opération asynchrone est terminée. 
  
Lors de l’appel **QueryRows**, n’oubliez pas que la synchronisation des notifications asynchrones peut potentiellement provoquer le jeu de lignes que vous récupérez des **QueryRows** ne pas pour représenter précisément les données sous-jacentes. Par exemple, un appel à **QueryRows** suivant de tableau de contenu d’un dossier que la suppression d’un message, mais avant la réception de la notification correspondante entraîne la ligne supprimée à renvoyer à partir de la ligne est définie. Toujours attendre une notification avant la mise à jour de la vue des données. 
  
Pour plus d’informations sur la récupération des lignes à partir des tables, voir [Récupération de données à partir des lignes de tableau](retrieving-data-from-table-rows.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |DwThreadFuncLoadTable  <br/> |MFCMAPI utilise la méthode **IMAPITable::QueryRows** pour récupérer des lignes de la table à charger dans l’affichage.  <br/> |
   
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

