---
title: IMAPITableSetColumns
description: IMAPITableSetColumns définit les propriétés particulières et l’ordre des propriétés à afficher sous forme de colonnes dans la table.
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
ms.openlocfilehash: 2850f04c1267cfe053c49a32bc4a0c425c50b741
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65827799"
---
# <a name="imapitablesetcolumns"></a>IMAPITable::SetColumns

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit les propriétés particulières et l’ordre des propriétés à afficher sous forme de colonnes dans la table.
  
```cpp
HRESULT SetColumns(
LPSPropTagArray lpPropTagArray,
ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpPropTagArray_
  
> [in] Pointeur vers un tableau de balises de propriété identifiant les propriétés à inclure en tant que colonnes dans la table. La partie type de propriété de chaque balise peut être définie sur un type valide ou **PR_NULL** pour réserver de l’espace pour les ajouts suivants. Le paramètre  _lpPropTagArray_ ne peut pas être défini sur NULL ; chaque table doit avoir au moins une colonne. 
    
 _ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôlent le retour d’un appel asynchrone à **SetColumns**, par exemple lorsque **SetColumns** est utilisé dans la notification. Les indicateurs suivants peuvent être définis : 
    
TBL_ASYNC 
  
> Demande que l’opération de paramètre de colonne soit effectuée de manière asynchrone, ce qui peut renvoyer **SetColumns** avant la fin complète de l’opération. 
    
TBL_BATCH 
  
> Permet à la table de reporter l’opération de paramètre de colonne jusqu’à ce que les données soient réellement requises.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’opération de définition de colonne a réussi.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours qui empêche le démarrage de l’opération de définition de colonne. Soit l’opération en cours doit être autorisée à se terminer, soit elle doit être arrêtée.
    
## <a name="remarks"></a>Remarques

L’ensemble de colonnes d’une table est le groupe de propriétés qui composent les colonnes des lignes de la table. Il existe un jeu de colonnes par défaut pour chaque type de table. L’ensemble de colonnes par défaut est constitué des propriétés que l’implémenteur de table inclut automatiquement. Les utilisateurs de table peuvent modifier cet ensemble par défaut en appelant la méthode **IMAPITable::SetColumns** . Ils peuvent demander que d’autres colonnes soient ajoutées à l’ensemble par défaut si l’implémenteur de table les prend en charge pour que les colonnes soient supprimées ou que l’ordre des colonnes soit modifié. **SetColumns** spécifie les colonnes retournées avec chaque ligne et l’ordre de ces colonnes dans la ligne. 
  
Le succès de l’opération **SetColumns** n’est visible qu’après qu’un appel ultérieur a été effectué pour récupérer les données de la table. C’est alors que toutes les erreurs sont signalées. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Certains fournisseurs autorisent un appel **SetColumns** pour commander uniquement les colonnes de table qui font partie des colonnes disponibles pour une vue de table. D’autres fournisseurs autorisent un appel **SetColumns** pour classer toutes les colonnes de table, y compris celles contenant des propriétés qui ne sont pas dans le jeu de colonnes d’origine. 
  
Lorsque TBL_BATCH est défini pour les opérations asynchrones, les fournisseurs doivent retourner un type de propriété de PT_ERROR et une valeur de propriété NULL pour les colonnes qui ne sont pas prises en charge.
  
Vous n’avez pas besoin de répondre à l’indicateur TBL_ASYNC demandant que l’opération soit asynchrone. Si vous ne prenez pas en charge la définition de jeu de colonnes asynchrone, effectuez l’opération de façon synchrone. Si vous pouvez gérer l’indicateur TBL_ASYNC et qu’une autre opération asynchrone est toujours en cours, retournez MAPI_E_BUSY. Sinon, retournez S_OK que vous preniez ou non en charge toutes les propriétés incluses dans le tableau de balises de propriétés. Les erreurs résultant de propriétés non prises en charge doivent être retournées à partir de méthodes **IMAPITable** qui récupèrent des données, telles que **QueryRows**. 
  
Ne générez pas de notifications pour les lignes de table masquées par les appels à **Restreindre**. 
  
Lors de l’envoi de notifications de table, l’ordre des propriétés dans le membre de **ligne** de la structure [TABLE_NOTIFICATION](table_notification.md) et l’ordre spécifié par l’appel **SetColumns** le plus récent doivent être identiques au moment où la demande de notification a été envoyée. 
  
Un autre indicateur, TBL_BATCH, permet aux appelants de spécifier que l’implémenteur de table peut différer l’évaluation des résultats de l’opération jusqu’à une date ultérieure. Dans la mesure du possible, les appelants doivent définir cet indicateur, car l’opération par lot améliore les performances.
  
Il est souvent pratique pour les appelants de réserver des colonnes dans le jeu de lignes récupéré pour les valeurs à ajouter ultérieurement. Pour ce faire, les appelants placent **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) aux positions souhaitées dans le tableau de balises de propriétés passé à **SetColumns** ; la table passe ensuite **PR_NULL** à ces positions dans toutes les lignes récupérées avec **QueryRows**.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Lorsque vous créez le tableau de balises de propriétés pour le paramètre  _lpPropTagArray_ , commandez les balises dans l’ordre dans lequel vous souhaitez que les colonnes apparaissent dans la vue de table. 
  
Vous pouvez spécifier des propriétés à valeurs multiples à inclure dans l’ensemble de colonnes en appliquant l’indicateur d’instance à valeurs multiples, ou MVI_FLAG constante, à la balise de propriété. Définissez cet indicateur en passant la balise de propriété de la version à valeur unique de la propriété en tant que paramètre à la macro MVI_PROP comme suit :
  
```
MVI_PROP(ulPropTag)

```

La macro MVI_PROP définit MVI_FLAG pour la propriété, en transformant la balise en balise à valeurs multiples. Si vous essayez à tort d’appeler MVI_PROP sur une propriété à valeur unique, MAPI ignore l’appel et laisse la balise de propriété inchangée. 
  
Vous pouvez inclure des balises de propriété définies sur **PR_NULL** dans le tableau de balises de propriétés pour réserver de l’espace dans le jeu de colonnes. La réservation d’espace vous permet d’ajouter à un jeu de colonnes sans avoir à allouer un nouveau tableau de balises de propriétés. 
  
Lorsque votre appel à **SetColumns** entraîne une modification de l’ordre des colonnes d’une table et qu’une ou plusieurs de ces colonnes représentent une propriété à valeurs multiples, il est possible que le nombre de lignes de la table augmente. Si cela se produit, tous les signets de la table sont ignorés. Pour plus d’informations sur la façon dont les colonnes à valeurs multiples affectent les tables, consultez [Utilisation des colonnes à valeurs multiples](working-with-multivalued-columns.md).
  
La définition des colonnes est par défaut une opération synchrone. Toutefois, vous pouvez autoriser la table à reporter l’opération jusqu’au moment où les données sont nécessaires en définissant l’indicateur TBL_BATCH. La définition de cet indicateur peut améliorer les performances. Un autre indicateur, TBL_ASYNC, rend l’opération asynchrone, ce qui permet à **SetColumns** de revenir avant la fin de l’opération. Pour déterminer quand l’achèvement se produit, appelez [IMAPITable::GetStatus](imapitable-getstatus.md).
  
Si un appel à **SetColumns** retourne MAPI_E_BUSY, indiquant qu’une autre opération empêche le démarrage de votre opération, vous pouvez appeler [IMAPITable::Abort](imapitable-abort.md) pour arrêter l’opération en cours. 
  
Vous pouvez également appeler [HrAddColumnsEx](hraddcolumnsex.md) pour modifier un jeu de colonnes. La différence entre **HrAddColumnsEx** et **IMAPITable::SetColumns** est que **HrAddColumnsEx** est moins flexible ; il ne peut ajouter que des colonnes. Les colonnes supplémentaires sont placées au début de l’ensemble de colonnes ; toutes les colonnes existantes apparaissent en suivant ces colonnes. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::D oSetColumns  <br/> |MFCMAPI utilise la méthode **IMAPITable::SetColumns** pour définir les colonnes souhaitées pour la table. |
   
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

