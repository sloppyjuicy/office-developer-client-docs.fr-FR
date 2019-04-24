---
title: Shape Append, clause
TOCTitle: Shape Append clause
ms:assetid: 8f29afc3-fb93-4439-b67b-cad0eed0bda9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249633(v=office.15)
ms:contentKeyID: 48546301
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 40c35e8b2c3fb3f0b92bf261b62c252a61a367b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306446"
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
> - La clause _«parent-Column to Child-Column»_ est en fait une liste, dans laquelle chaque relation définie est séparée par une virgule.
> - La clause suivant le mot-clé APPEND est en fait une liste, dans laquelle chaque clause est séparée par une virgule et définit une autre colonne à ajouter au parent.



## <a name="remarks"></a>Remarques

Lorsque vous créez des commandes de fournisseur depuis une entrée utilisateur dans le cadre d'une commande SHAPE, SHAPE traite la commande fournisseur fournie par l'utilisateur sous la forme d'une chaîne opaque et la passe fidèlement au fournisseur. Par exemple, dans la commande SHAPE suivante,

```vb 
 
SHAPE {select * from t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

SHAPE exécute deux commandes: SELECT \* from T1 et (Select \* from T2 relate K1 to K2). Si l'utilisateur fournit une commande composée de plusieurs commandes fournisseur séparées par des points-virgules, SHAPE ne sera pas capable de discerner les composantes de la commande. Ainsi, dans la commande SHAPE suivante,

```vb 
 
SHAPE {select * from t1; drop table t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

La forme exécute Select \* à partir de T1; drop table T1 et (Select \* from T2 relat K1 à K2), il n'est pas vrai que drop table T1 est un élément distinct et dans ce cas, une commande de fournisseur dangereuse. Les applications doivent toujours valider l'entrée utilisateur pour empêcher d'éventuelles attaques de pirates.

Cette section contient les rubriques suivantes :

- [Operation of Non-Parameterized Commands](operation-of-non-parameterized-commands.md)

- [Operation of Parameterized Commands](operation-of-parameterized-commands.md)

- [Hybrid Commands](hybrid-commands.md)

- [Intervening Shape COMPUTE Clauses](intervening-shape-compute-clauses.md)
