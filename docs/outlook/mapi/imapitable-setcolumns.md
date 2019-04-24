---
title: IMAPITableSetColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SetColumns
api_type:
- COM
ms.assetid: 9a39cf8d-df0f-493c-b272-f15c65b3f15e
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 897330feb216dbc3ab143378977c77141cf488f0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328818"
---
# <a name="imapitablesetcolumns"></a>IMAPITable::SetColumns

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit les propriétés et l'ordre des propriétés spécifiques à afficher sous la forme de colonnes dans le tableau.
  
```cpp
HRESULT SetColumns(
LPSPropTagArray lpPropTagArray,
ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpPropTagArray_
  
> dans Pointeur vers un tableau de balises de propriété qui identifient les propriétés à inclure en tant que colonnes dans le tableau. La partie type de propriété de chaque balise peut être définie sur un type valide ou sur **PR_NULL** pour réserver de l'espace pour les ajouts suivants. Le paramètre _lpPropTagArray_ ne peut pas avoir la valeur null; chaque tableau doit comporter au moins une colonne. 
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le renvoi d'un appel asynchrone à **SetColumns**, par exemple lorsque la **SetColumns** est utilisée dans la notification. Les indicateurs suivants peuvent être définis: 
    
TBL_ASYNC 
  
> Demande que l'opération de définition de colonne soit effectuée de manière asynchrone, ce qui entraîne le renvoi éventuel de **SetColumns** avant la fin de l'opération. 
    
TBL_BATCH 
  
> Permet à la table de reporter l'opération de définition de colonne jusqu'à ce que les données soient réellement requises.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'opération de définition de la colonne a réussi.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours, ce qui empêche le démarrage de l'opération de définition de colonne. L'opération en cours doit être autorisée ou elle doit être arrêtée.
    
## <a name="remarks"></a>Remarques

Le jeu de colonnes d'un tableau est le groupe de propriétés qui composent les colonnes des lignes du tableau. Il existe un jeu de colonnes par défaut pour chaque type de tableau. L'ensemble de colonnes par défaut est composé des propriétés que le programme d'implémentation du tableau inclut automatiquement. Les utilisateurs de tableau peuvent modifier cet ensemble par défaut en appelant la méthode **IMAPITable:: SetColumns** . Ils peuvent demander à ce que d'autres colonnes soient ajoutées à l'ensemble par défaut si l'implémenteur de table les prend en charge, ou que l'ordre des colonnes doit être modifié. **SetColumns** spécifie les colonnes renvoyées avec chaque ligne et l'ordre de ces colonnes dans la ligne. 
  
La réussite de l'opération **SetColumns** n'est apparente qu'après qu'un appel a été effectué pour extraire les données de la table. Cela signifie que toutes les erreurs sont signalées. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Certains fournisseurs permettent à un appel **SetColumns** de trier uniquement les colonnes de table qui font partie des colonnes disponibles pour un affichage tableau. D'autres fournisseurs autorisent un appel **SetColumns** à trier toutes les colonnes de table, y compris celles contenant des propriétés qui ne figurent pas dans l'ensemble de colonnes d'origine. 
  
Lorsque TBL_BATCH est défini pour des opérations asynchrones, les fournisseurs doivent renvoyer un type de propriété PT_ERROR et une valeur de propriété NULL pour les colonnes qui ne sont pas prises en charge.
  
Vous n'avez pas besoin de répondre à l'indicateur TBL_ASYNC demandant que l'opération soit asynchrone. Si vous ne prenez pas en charge la définition de jeu de colonnes asynchrone, effectuez l'opération de façon synchrone. Si vous pouvez prendre en charge l'indicateur TBL_ASYNC et qu'une autre opération asynchrone est toujours en cours, renvoyez MAPI_E_BUSY. Sinon, renvoie S_OK, que vous soyez ou non en prise en charge de toutes les propriétés incluses dans le tableau de balises de propriété. Les erreurs résultant de propriétés non prises en charge doivent être renvoyées par les méthodes **IMAPITable** qui extraient des données, telles que **QueryRows**. 
  
Ne générez pas de notifications pour les lignes de tableau masquées en vue par les appels à **limiter**. 
  
Lors de l'envoi de notifications de table, l'ordre des propriétés dans le membre de **ligne** de la structure [TABLE_NOTIFICATION](table_notification.md) et l'ordre spécifié par le dernier appel **SetColumns** doivent être les mêmes que ceux de la demande de notification. a été envoyé. 
  
Un autre indicateur, TBL_BATCH, permet aux appelants de spécifier que l'implémenteur de table peut différer l'évaluation des résultats de l'opération jusqu'à une date ultérieure. Dans la mesure du possible, les appelants doivent définir cet indicateur car l'opération par lot améliore les performances.
  
Il est souvent commode pour les appelants de réserver certaines colonnes dans l'ensemble de lignes récupérés pour que les valeurs soient ajoutées ultérieurement. Pour cela, les appelants placent **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) aux positions souhaitées dans le tableau des balises de propriété transmises à **SetColumns**; le tableau transmet ensuite **PR_NULL** à ces positions dans toutes les lignes récupérées avec **QueryRows**.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Lors de la création du tableau de balises de propriété pour le paramètre _lpPropTagArray_ , organisez les balises dans l'ordre dans lequel vous souhaitez que les colonnes apparaissent dans l'affichage tableau. 
  
Vous pouvez spécifier que les propriétés à valeurs multiples doivent être incluses dans le jeu de colonnes en appliquant l'indicateur d'instance à valeurs multiples ou une constante MVI_FLAG à la balise de propriété. Définissez cet indicateur en transmettant la balise de propriété de la version à valeur unique de la propriété en tant que paramètre à la macro MVI_PROP comme suit:
  
```
MVI_PROP(ulPropTag)

```

La macro MVI_PROP définit MVI_FLAG pour la propriété, transformant la balise en balise à valeurs multiples. Si vous essayez d'appeler MVI_PROP à tort sur une propriété à valeur unique, MAPI ignore l'appel et laisse la balise de propriété inchangée. 
  
Vous pouvez inclure des balises de propriété définies sur **PR_NULL** dans le tableau des balises de propriété pour réserver de l'espace dans le jeu de colonnes. L'espace réservé vous permet d'ajouter à un jeu de colonnes sans devoir allouer un nouveau tableau de balises de propriété. 
  
Lorsque votre appel à **SetColumns** entraîne une modification de l'ordre des colonnes d'une table et qu'une ou plusieurs de ces colonnes représentent une propriété à valeurs multiples, il est possible que le nombre de lignes de la table augmente. Dans ce cas, tous les signets de la table sont ignorés. Pour plus d'informations sur l'impact des colonnes à valeurs multiples sur [les](working-with-multivalued-columns.md)tableaux, voir Working with multiValued Columns.
  
La définition de colonnes est par défaut une opération synchrone. Toutefois, vous pouvez autoriser la table à reporter l'opération jusqu'à ce que les données soient nécessaires en définissant l'indicateur TBL_BATCH. La définition de cet indicateur peut améliorer les performances. Un autre indicateur, TBL_ASYNC, rend l'opération asynchrone, ce qui permet le renvoi de **SetColumns** avant la fin de l'opération. Pour déterminer à quel moment l'opération se termine, appelez [IMAPITable:: GetStatus](imapitable-getstatus.md).
  
Si un appel à **SetColumns** renvoie MAPI_E_BUSY, indiquant qu'une autre opération empêche le démarrage de votre opération, vous pouvez appeler la méthode [IMAPITable:: Abort](imapitable-abort.md) pour arrêter l'opération en cours. 
  
Vous pouvez également appeler [HrAddColumnsEx](hraddcolumnsex.md) pour modifier un jeu de colonnes. La différence entre **HrAddColumnsEx** et **IMAPITable:: SetColumns** est que **HrAddColumnsEx** est moins flexible; Il peut uniquement ajouter des colonnes. Les colonnes supplémentaires sont placées au début de l'ensemble de colonnes; toutes les colonnes existantes apparaissent à la suite de ces colonnes. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> |CContentsTableListCtrl::D oSetColumns  <br/> |MFCMAPI utilise la méthode **IMAPITable:: SetColumns** pour définir les colonnes souhaitées pour le tableau.  <br/> |
   
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

