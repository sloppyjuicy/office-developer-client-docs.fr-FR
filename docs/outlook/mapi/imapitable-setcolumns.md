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
ms.openlocfilehash: 9eeab1e1186aeb5a9b458facd59bd4cc155e8014
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784093"
---
# <a name="imapitablesetcolumns"></a>IMAPITable::SetColumns

  
  
**S’applique à**: Outlook 
  
Définit les propriétés et l’ordre des propriétés apparaissent sous forme de colonnes dans le tableau.
  
```cpp
HRESULT SetColumns(
LPSPropTagArray lpPropTagArray,
ULONG ulFlags
);
```

## <a name="parameters"></a>Param�tres

 _lpPropTagArray_
  
> [in] Pointeur vers un tableau de balises de propriété identification des propriétés pour être inclus en tant que colonnes dans le tableau. La partie du type de propriété de chaque balise peut avoir un type valide ou **PR_NULL** à réserver un espace pour les ajouts suivants. Le paramètre _lpPropTagArray_ ne peut pas être défini sur NULL ; chaque table doit comporter au moins une colonne. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le retour d’un appel asynchrone au **SetColumns**, par exemple lorsque **SetColumns** est utilisé dans la notification. Les indicateurs suivants peuvent être définis : 
    
TBL_ASYNC 
  
> Demandes l’opération de définition de colonne est effectuée en mode asynchrone à l’origine de **SetColumns** potentiellement retourner avant que l’opération est entièrement terminée. 
    
TBL_BATCH 
  
> Permet à la table de différer l’opération de définition de colonne jusqu'à ce que les données sont réellement nécessaires.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le paramètre colonne a réussi.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours qui empêche la colonne définissant l’opération de démarrage. L’opération en cours doit être autorisée à effectuer ou il doit être arrêté.
    
## <a name="remarks"></a>Remarques

L’ensemble de colonnes d’une table est le groupe de propriétés qui constituent les colonnes des lignes dans le tableau. Il est une colonne par défaut pour chaque type de table. L’ensemble de colonnes par défaut est composée des propriétés qui inclut automatiquement de l’implémentation de la table. Les utilisateurs de tableau peuvent modifier cette valeur par défaut définie en appelant la méthode **IMAPITable::SetColumns** . Ils peuvent demander que les autres colonnes ajoutées à la valeur par défaut si l’implémentation de la table prend en charge les colonnes supprimées ou modifier l’ordre de colonnes que la valeur. **SetColumns** spécifie les colonnes qui sont retournées avec chaque ligne et l’ordre de ces colonnes dans la ligne. 
  
La réussite de l’opération **SetColumns** n’apparaît qu’après qu’un appel suivant a été effectué pour récupérer les données de la table. Il est alors que les erreurs détectées. 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Certains fournisseurs permettent à un appel **SetColumns** trier uniquement les colonnes de tableau qui font partie des colonnes disponibles pour un affichage de tableau. Autres fournisseurs d’autorisent un appel **SetColumns** trier toutes les colonnes du tableau, y compris ceux qui contiennent des propriétés pas dans l’ensemble de colonnes d’origine. 
  
Lorsque TBL_BATCH est défini pour les opérations asynchrones, fournisseurs doivent renvoyer un type de propriété de PT_ERROR et une valeur de la propriété Null pour les colonnes qui ne sont pas pris en charge.
  
Il est inutile de répondre à le TBL_ASYNC indicateur qui sollicitent que l’opération asynchrone. Si vous ne prennent pas en charge colonne asynchrone définition, effectuer l’opération de manière synchrone. Si vous pouvez prendre en charge l’indicateur TBL_ASYNC et l’autre asynchrone opération est toujours en cours, renvoyée MAPI_E_BUSY. Sinon, renvoie S_OK quel que soit ou non toutes les propriétés incluses dans le tableau de la propriété tag prend en charge. Erreurs résultant des propriétés non prises en charge doivent être renvoyées à partir de méthodes **IMAPITable** qui récupèrent des données, telles que **QueryRows**. 
  
Ne génèrent pas de notifications pour les lignes de tableau sont masquées à partir de la vue par les appels à **restreindre**. 
  
Lors de l’envoi des notifications de table, l’ordre des propriétés de membre de la **ligne** de la structure [TABLE_NOTIFICATION](table_notification.md) et l’ordre spécifié par l’appel le plus récent **SetColumns** doit être identique à compter de l’heure de la notification de demande a été envoyé. 
  
Un autre indicateur, TBL_BATCH, permet aux appelants de spécifier que l’implémentation de la table peut différer l’évaluation des résultats de l’opération jusqu'à une date ultérieure. La mesure du possible, les appelants doivent définir cet indicateur car une opération par lot améliore les performances.
  
Il est souvent pratique pour les appelants à réserver certaines colonnes dans le jeu de lignes récupérées pour les valeurs d’être ajoutées ultérieurement. Les appelants cela en plaçant **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) à la position souhaitée dans le tableau de balise de propriété passé à **SetColumns**; le tableau sera puis renvoie **PR_NULL** à ces postes dans toutes les lignes extraites avec **QueryRows**.
  
## <a name="notes-to-callers"></a>Notes aux appelants

Lors de la création du tableau de balise de propriété pour le paramètre _lpPropTagArray_ , les balises de commande dans l’ordre souhaité les colonnes à afficher dans l’affichage tableau. 
  
Vous pouvez spécifier les propriétés à valeurs multiples pour être inclus dans la colonne en appliquant l’indicateur d’instance à valeurs multiples, ou une constante MVI_FLAG, à la balise de propriété. Définissez cet indicateur en transmettant la balise de propriété pour la version de la propriété à valeur unique en tant que paramètre à la macro MVI_PROP comme suit :
  
```
MVI_PROP(ulPropTag)

```

La macro MVI_PROP définira MVI_FLAG pour la propriété transformer la balise en une balise à valeurs multiples. Si vous essayez tort d’appeler MVI_PROP sur une propriété à valeur unique, MAPI ignorera l’appel et laissez la balise de propriété inchangée. 
  
Vous pouvez inclure des balises de propriété **PR_NULL** la valeur dans le tableau de la propriété tag pour réserver un espace dans la colonne. Réservation d’espace vous permet d’ajouter à une colonne sans avoir à allouer un nouveau tableau de balise de propriété. 
  
Lors de l’appel de **SetColumns** provoque une modification de l’ordre des colonnes d’une table et un ou plusieurs de ces colonnes représentent une propriété à valeurs multiples, il est possible pour le nombre de lignes de la table pour augmenter. Si cela se produit, tous les signets du tableau sont ignorées. Pour plus d’informations sur la façon de colonnes à valeurs multiples affectent les tables, voir [utilisation des colonnes à valeurs multiples](working-with-multivalued-columns.md).
  
Définition des colonnes par défaut est une opération synchrone. Toutefois, vous pouvez autoriser la table à différer l’opération jusqu'à ce que les données sont nécessaires à la définition de l’indicateur TBL_BATCH. Définition de cet indicateur peut améliorer les performances. Un autre indicateur, TBL_ASYNC, effectue l’opération asynchrone, ce qui permet de **SetColumns** retourner avant que l’opération est terminée. Pour déterminer si l’exécution se produit, appelez [IMAPITable::GetStatus](imapitable-getstatus.md).
  
Si un appel à la **méthode SetColumns** renvoie MAPI_E_BUSY, indiquant qu’une autre opération empêche l’opération de démarrage, vous pouvez appeler [IMAPITable::Abort](imapitable-abort.md) pour arrêter l’opération en cours. 
  
Vous pouvez également appeler [HrAddColumnsEx](hraddcolumnsex.md) pour modifier un ensemble de colonnes. La différence entre **HrAddColumnsEx** et **IMAPITable::SetColumns** est **HrAddColumnsEx** moins de souplesse ; Il ne peut ajouter des colonnes. Les colonnes supplémentaires sont placés au début de l’ensemble de colonnes ; toutes les colonnes existantes apparaissent après ces colonnes. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::DoSetColumns  <br/> |MFCMAPI utilise la méthode **IMAPITable::SetColumns** pour définir les colonnes souhaitées pour la table.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[HrQueryAllRows](hrqueryallrows.md)
  
[IMAPITable::Abort](imapitable-abort.md)
  
[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable](imapitable-restrict.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[SPropTagArray](sproptagarray.md)
  
[SPropValue](spropvalue.md)
  
[SRowSet](srowset.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

