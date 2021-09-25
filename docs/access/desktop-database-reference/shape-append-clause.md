---
title: Shape Append, clause
TOCTitle: Shape Append clause
ms:assetid: 8f29afc3-fb93-4439-b67b-cad0eed0bda9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249633(v=office.15)
ms:contentKeyID: 48546301
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c0304e104953a5c95f25ca22ba719756dccc6ecc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605917"
---
# <a name="shape-append-clause"></a>Shape Append, clause


**S’applique à** : Access 2013, Office 2013

La clause APPEND de commande SHAPE ajoute une ou plusieurs colonnes à un objet **Recordset**. Souvent, ces colonnes sont des chapitres qui font référence à un objet **Recordset** enfant.

## <a name="syntax"></a>Syntaxe

```vb 
 
SHAPE [parent-command [[AS] parent-alias]] APPEND column-list
```

## <a name="description"></a>Description

Cette clause comporte les parties suivantes :

- *parent-command*

- Un des éléments suivants ou aucun (vous pouvez omettre *parent-command* complètement) :
    
  - Commande fournisseur entre accolades (« {} ») qui retourne un objet **Recordset**. La commande est transmise au fournisseur de données sous-jacent et sa syntaxe dépend des exigences du fournisseur. Elle est en général écrite en langage SQL, même si ADO n'exige pas de langage de requête particulier.
    
  - Autre commande Shape placée entre parenthèses.
    
  - Mot-clé TABLE, suivi du nom d'une table du fournisseur de données.

- *parent-alias*

  - Alias facultatif qui fait référence à l'objet **Recordset** parent.

- *column-list*

  - Un ou plusieurs des éléments suivants :
    
    - Colonne agrégée.
    
    - Colonne calculée.
    
    - Nouvelle colonne créée avec la clause NEW.
    
    - Colonne de chapitre. Une définition de colonne de chapitre est placée entre parenthèses (« () »). Reportez-vous à la syntaxe ci-dessous


        ```vb 
        
        SHAPE [parent-command [[AS] parent-alias]] 
        APPEND (child-recordset [ [[AS] child-alias] 
        RELATE parent-column TO child-column | PARAMETER param-number, ... ]) 
        [[AS] chapter-alias] 
        [, ... ] 
        ```

- *child-recordset*

  - Commande fournisseur entre accolades (« {} ») qui retourne un objet **Recordset**. La commande est transmise au fournisseur de données sous-jacent et sa syntaxe dépend des exigences du fournisseur. Elle est en général écrite en langage SQL, même si ADO n'exige pas de langage de requête particulier.
    
  - Autre commande Shape placée entre parenthèses.
    
  - Nom d'un objet **Recordset** mis en forme existant.
    
  - Mot-clé TABLE, suivi du nom d'une table du fournisseur de données.

- *child-alias*

  - Alias qui fait référence à l'objet **Recordset** enfant.

- *parent-column*

  - Colonne de l'objet **Recordset** retournée par *parent-command.*

- *child-column*

  - Colonne de l'objet **Recordset** retournée par *child-command*.

- *param-number*

  - Consultez [Fonctionnement des commandes paramétrées](operation-of-parameterized-commands.md).

- *chapter-alias*

  - Alias qui fait référence à la colonne de chapitre ajoutée au parent.


> [!NOTE]
> - La clause _« parent-column TO child-column »_ est en fait une liste, où chaque relation définie est séparée par une virgule.
> - La clause suivant le mot-clé APPEND est en fait une liste, dans laquelle chaque clause est séparée par une virgule et définit une autre colonne à ajouter au parent.



## <a name="remarks"></a>Remarques

Lorsque vous créez des commandes de fournisseur depuis une entrée utilisateur dans le cadre d'une commande SHAPE, SHAPE traite la commande fournisseur fournie par l'utilisateur sous la forme d'une chaîne opaque et la passe fidèlement au fournisseur. Par exemple, dans la commande SHAPE suivante,

```vb 
 
SHAPE {select * from t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

SHAPE exécute deux commandes : select \* from t1 et (select \* from t2 RELATE k1 TO k2). Si l'utilisateur fournit une commande composée de plusieurs commandes fournisseur séparées par des points-virgules, SHAPE ne sera pas capable de discerner les composantes de la commande. Ainsi, dans la commande SHAPE suivante,

```vb 
 
SHAPE {select * from t1; drop table t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

SHAPE exécute select \* from t1; drop table t1 et (select from t2 RELATE k1 TO k2), sans se rendre compte que le tableau de drop t1 est une commande de fournisseur distincte et, dans ce \* cas, dangereuse. Les applications doivent toujours valider l'entrée utilisateur pour empêcher d'éventuelles attaques de pirates.

Cette section contient les rubriques suivantes :

- [Operation of Non-Parameterized Commands](operation-of-non-parameterized-commands.md)

- [Operation of Parameterized Commands](operation-of-parameterized-commands.md)

- [Hybrid Commands](hybrid-commands.md)

- [Intervening Shape COMPUTE Clauses](intervening-shape-compute-clauses.md)
