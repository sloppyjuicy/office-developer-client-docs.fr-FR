---
title: IMAPITableSetColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.SetColumns
api_type:
- COM
ms.assetid: 9a39cf8d-df0f-493c-b272-f15c65b3f15e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 73525fa016b856519017d01d364f88be207ee9e3
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62777417"
---
# <a name="imapitablesetcolumns"></a>IMAPITable::SetColumns

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit les propriétés et l’ordre particuliers des propriétés à voir apparaître sous la valeur de colonnes dans le tableau.
  
```cpp
HRESULT SetColumns(
LPSPropTagArray lpPropTagArray,
ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpPropTagArray_
  
> [in] Pointeur vers un tableau de balises de propriétés identifiant les propriétés à inclure en tant que colonnes dans le tableau. La partie type de propriété de chaque balise peut être définie sur un type valide ou sur **PR_NULL** pour réserver de l’espace pour les ajouts suivants. Le  _paramètre lpPropTagArray ne_ peut pas être définie sur NULL ; chaque table doit avoir au moins une colonne. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le retour d’un appel asynchrone à **SetColumns**, par exemple lorsque **SetColumns** est utilisé dans la notification. Les indicateurs suivants peuvent être définies : 
    
TBL_ASYNC 
  
> Demande que l’opération de paramètre de colonne soit effectuée de manière asynchrone, ce qui peut entraîner le retour de **SetColumns** avant que l’opération ne soit entièrement terminée. 
    
TBL_BATCH 
  
> Permet au tableau de différer l’opération de définition de colonne jusqu’à ce que les données soient réellement requises.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’opération de paramètre de colonne a réussi.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours qui empêche le démarrage de l’opération de paramètre de colonne. L’opération en cours doit être autorisée ou arrêtée.
    
## <a name="remarks"></a>Remarques

L’ensemble de colonnes d’un tableau est le groupe de propriétés qui constitue les colonnes des lignes du tableau. Il existe un ensemble de colonnes par défaut pour chaque type de tableau. Le jeu de colonnes par défaut est composé des propriétés que l’implémenteur de table inclut automatiquement. Les utilisateurs du tableau peuvent modifier ce jeu par défaut en appelant la **méthode IMAPITable::SetColumns** . Ils peuvent demander que d’autres colonnes soient ajoutées à l’ensemble par défaut si l’implémenteur de tableau les prend en charge pour que les colonnes soient supprimées ou que l’ordre des colonnes soit modifié. **SetColumns** spécifie les colonnes qui sont renvoyées avec chaque ligne et l’ordre de ces colonnes dans la ligne. 
  
La réussite de **l’opération SetColumns** n’apparaît qu’après qu’un appel ultérieur a été effectué pour récupérer les données de la table. C’est ensuite que les erreurs sont signalées. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Certains fournisseurs autorisent un appel **SetColumns** à commander uniquement les colonnes de tableau qui font partie des colonnes disponibles pour un affichage tableau. D’autres fournisseurs autorisent un appel **SetColumns** pour commander toutes les colonnes de table, y compris celles qui contiennent des propriétés qui ne sont pas dans le jeu de colonnes d’origine. 
  
Lorsque TBL_BATCH est définie pour les opérations asynchrones, les fournisseurs doivent renvoyer un type de propriété de PT_ERROR et une valeur de propriété NULL pour les colonnes qui ne sont pas pris en charge.
  
Vous n’avez pas besoin de répondre à l’indicateur TBL_ASYNC demande que l’opération soit asynchrone. Si vous ne prisez pas en charge la définition de jeu de colonnes asynchrone, effectuez l’opération de manière synchrone. Si vous pouvez prendre en charge l’indicateur TBL_ASYNC et qu’une autre opération asynchrone est toujours en cours, renvoyez MAPI_E_BUSY. Sinon, renvoyez S_OK indépendamment de la prise en charge ou non de toutes les propriétés incluses dans le tableau de balises de propriétés. Les erreurs résultant de propriétés nonupportées doivent être renvoyées à partir des méthodes **IMAPITable** qui récupèrent des données, **telles que QueryRows**. 
  
Ne générez pas de notifications pour les lignes de tableau masquées par les appels à **Restreindre**. 
  
Lors de l’envoi de notifications de table, l’ordre des propriétés dans le membre de ligne de la structure TABLE_NOTIFICATION et l’ordre spécifié par l’appel **SetColumns** le plus récent doivent être identiques au moment où la demande de notification [a](table_notification.md) été envoyée. 
  
Un autre indicateur, TBL_BATCH, permet aux appelants de spécifier que l’implémenteur de table peut différer l’évaluation des résultats de l’opération jusqu’à une date ultérieure. Dans la mesure du possible, les appelants doivent définir cet indicateur, car l’opération par lot améliore les performances.
  
Il est souvent pratique pour les appelants de réserver certaines colonnes dans le jeu de lignes récupéré pour que les valeurs soient ajoutées ultérieurement. Pour ce faire, les appelants **PR_NULL (**[PidTagNull](pidtagnull-canonical-property.md)) aux positions souhaitées dans le tableau de balises de propriétés transmis **à SetColumns** ; La table est ensuite resserré **PR_NULL** à ces positions dans toutes les lignes récupérées avec **QueryRows**.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Lors de la création du tableau de balises de propriétés pour le paramètre  _lpPropTagArray_ , commandez les balises dans l’ordre dans le sens où les colonnes apparaissent dans l’affichage Tableau. 
  
Vous pouvez spécifier des propriétés à valeurs multiples à inclure dans l’ensemble de colonnes en appliquant l’indicateur d’instance à valeurs multiples, ou MVI_FLAG constante, à la balise de propriété. Définissez cet indicateur en passant la balise de propriété pour la version à valeur unique de la propriété en tant que paramètre à la macro MVI_PROP comme suit :
  
```
MVI_PROP(ulPropTag)

```

La macro MVI_PROP définira MVI_FLAG pour la propriété, ce qui transformera la balise en balise à valeurs multiples. Si vous essayez par erreur d’appeler MVI_PROP sur une propriété à valeur unique, MAPI ignore l’appel et laisse la balise de propriété inchangée. 
  
Vous pouvez inclure des balises de propriété définies **PR_NULL** dans le tableau de balises de propriétés pour réserver de l’espace dans le jeu de colonnes. La réservation d’espace vous permet d’ajouter un jeu de colonnes sans devoir allouer un nouveau tableau de balises de propriétés. 
  
Lorsque votre appel à **SetColumns** modifie l’ordre des colonnes d’un tableau et qu’une ou plusieurs de ces colonnes représentent une propriété à valeurs multiples, il est possible d’augmenter le nombre de lignes du tableau. Si cela se produit, tous les signets de la table sont ignorés. Pour plus d’informations sur l’impact des colonnes à valeurs multiples sur les tableaux, voir [Working with Multivalued Columns](working-with-multivalued-columns.md).
  
La définition de colonnes est une opération synchrone par défaut. Toutefois, vous pouvez autoriser la table à reporter l’opération jusqu’à ce que les données soient nécessaires en TBL_BATCH’indicateur. La définition de cet indicateur peut améliorer les performances. Un autre indicateur, TBL_ASYNC, rend l’opération asynchrone, ce qui permet à **SetColumns** de revenir avant la fin de l’opération. Pour déterminer quand l’achèvement se produit, appelez [IMAPITable::GetStatus](imapitable-getstatus.md).
  
Si un appel à **SetColumns** renvoie MAPI_E_BUSY, indiquant qu’une autre opération empêche le démarrage de votre opération, vous pouvez appeler [IMAPITable::Abort](imapitable-abort.md) pour arrêter l’opération en cours. 
  
Vous pouvez également appeler [HrAddColumnsEx](hraddcolumnsex.md) pour modifier un jeu de colonnes. La différence entre **HrAddColumnsEx** et **IMAPITable::SetColumns** est que **HrAddColumnsEx** est moins flexible ; il ne peut ajouter que des colonnes. Les colonnes supplémentaires sont placées au début du jeu de colonnes ; Toutes les colonnes existantes apparaissent après ces colonnes. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::D oSetColumns  <br/> |MFCMAPI utilise la **méthode IMAPITable::SetColumns** pour définir les colonnes souhaitées pour le tableau. |
   
## <a name="see-also"></a>Voir aussi



[HrQueryAllRows](hrqueryallrows.md)
  
[IMAPITable::Abort](imapitable-abort.md)
  
[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[SPropTagArray](sproptagarray.md)
  
[SPropValue](spropvalue.md)
  
[SRowSet](srowset.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

