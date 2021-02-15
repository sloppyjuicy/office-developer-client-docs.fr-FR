---
title: Fonctionnement des commandes paramétrées
TOCTitle: Operation of parameterized commands
ms:assetid: 71edbd16-21db-7afa-356b-d8e7afb92b3a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249456(v=office.15)
ms:contentKeyID: 48545596
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 145a2ee6c3d3c614eb9660350a0bb8a00d44d04c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288286"
---
# <a name="operation-of-parameterized-commands"></a>Fonctionnement des commandes paramétrées

**S’applique à** : Access 2013, Office 2013

Si vous utilisez un **jeu d'enregistrements** enfant de taille imposante, notamment par rapport à celle du **jeu d'enregistrements** parent, mais que vous n'avez besoin d'accéder qu'à un nombre réduit de chapitres enfant, nous vous conseillons d'utiliser une commande paramétrée.

Une *commande non paramétrée* extrait l'intégralité des **jeux d'enregistrements** enfant et parent, ajoute une colonne de chapitre au parent, puis affecte une référence au chapitre enfant associé de chaque ligne parent.

Une *commande paramétrée* extrait l'intégralité du **jeu d'enregistrements** parent, mais n'extrait le **jeu d'enregistrements** de chapitre que lorsque vous accédez à la colonne de chapitre. Cette différence dans la méthode d'extraction apporte des améliorations considérables en matière de performances.

Vous pouvez par exemple spécifier ce qui suit :

```vb 
 
SHAPE {SELECT * FROM customer} 
 APPEND ({SELECT * FROM orders WHERE cust_id = ?} 
 RELATE cust_id TO PARAMETER 0) 
```

Les tables parent et enfant ont un nom de colonne en commun, \_ id cust *.* La *commande enfant a* un espace réservé « ? », auquel la clause RELATE fait référence (autrement dit, « ... PARAMÈTRE 0 « ).

> [!NOTE]
> [!REMARQUE] La clause PARAMETER appartient uniquement à la syntaxe de commande de mise en forme. Elle n'est associée ni à l'objet [Parameter](parameter-object-ado.md), ni à la collection [Parameters](parameters-collection-ado.md) ADO.

Lors de l'exécution de la commande de mise en forme paramétrée, l'opération suivante se produit :

1.  La *commande-parent* est exécutée et renvoie un **jeu d'enregistrements** parent de la table Customers.

2.  Une colonne de chapitre est ajoutée au **jeu d'enregistrements** parent.

3.  Lorsque vous accédez à la colonne de chapitre d’une ligne parente, la *commande* enfant est exécutée à l’aide de la valeur de l’ID customer.cust comme valeur \_ du paramètre.

4.  Toutes les lignes du jeu de lignes du fournisseur de données créées à l’étape 3 sont utilisées pour renseigner le **jeu d’enregistrements** enfant. Dans cet exemple, il s’agit de toutes les lignes de la table Orders dans lesquelles l’ID cust est égal à la valeur \_ de customer.cust \_ id. Par défaut, les **jeux d’enregistrements** enfant sont mis en cache sur le client jusqu’à ce que toutes les références au **jeu d’enregistrements** parent soient extraites. Pour modifier ce comportement, définissez la propriété dynamique **Recordset** [](ado-dynamic-property-index.md)**Cache Child Rows** sur **False**.

5.  Une référence aux lignes enfant extraites (c'est-à-dire le chapitre du **jeu d'enregistrements** enfant) est placée dans la colonne de chapitre de la ligne active du **jeu d'enregistrements** parent.

6.  Les étapes 3 à 5 sont répétées lorsque vous accédez à la colonne de chapitre d'une autre ligne.

La propriété dynamique **Cache Child Rows** est définie sur **True** par défaut. Le comportement de mise en cache varie en fonction des valeurs de paramètre de la requête. Dans une requête à paramètre unique, le **jeu d'enregistrements** enfant d'une valeur de paramètre donnée est mis en cache entre les requêtes pour un enfant avec la même valeur. Ceci est illustré dans le code suivant :

```vb
... 
SCmd = "SHAPE {select * from customer} " & _ 
 "APPEND({select * from orders where cust_id = ?} " & _ 
 "RELATE cust_id TO PARAMETER 0) AS chpCustOrder" 
Rst1.Open sCmd, Cnn1 
Set RstChild = Rst1("chpCustOrder").Value 
Rst1.MoveNext ' Next cust_id passed to Param 0, & new rs fetched 
 ' into RstChild. 
Rst1.MovePrevious ' RstChild now holds cached rs, saving round trip. 
... 
```

Dans une requête avec deux paramètres ou plus, un enfant mis en cache est utilisé uniquement si toutes les valeurs de paramètre correspondent aux valeurs mises en cache.

## <a name="parameterized-commands-and-complex-parent-child-relations"></a>Commandes paramétisées et relations enfants parent complexes

Les commandes paramétrées permettent non seulement d'améliorer les performances en terme de hiérarchie de type équi-jointure, mais elles peuvent également être utilisées pour la prise en charge de relations parent-enfant plus complexes. Par exemple, envisagez une base de données Little League avec deux tables : l’une constituée des équipes (ID d’équipe, nom de l’équipe) et l’autre des jeux (date, équipe à domicile, équipe de \_ \_ \_ \_ visite).

Avec une hiérarchie non paramétrée, vous ne pouvez en aucun cas relier les deux tables de telle sorte que le **jeu d'enregistrements** enfant de chaque équipe contienne l'ensemble de son calendrier. Vous pouvez créer des chapitres contenant le calendrier à domicile ou le calendrier à l'extérieur, mais pas les deux. Ceci s'explique par le fait que la clause RELATE vous limite à des relations parent-enfant de type (pc1=cc1) AND (pc2=pc2). Ainsi, si votre commande incluait « RELATE \_ team id TO home team, team id TO visiting team », vous n’obtenez que les jeux où une équipe joue \_ elle-même. \_ \_ Ce que vous souhaitez, c’est « (team \_ id=home \_ team) OR (team \_ id=visiting team) », mais le fournisseur Shape ne prend pas en charge la \_ clause OR.

Pour obtenir le résultat souhaité, vous pouvez utiliser une commande paramétrée. Par exemple :

```vb 
 
SHAPE {SELECT * FROM teams} 
APPEND ({SELECT * FROM games WHERE home_team = ? OR visiting_team = ?} 
 RELATE team_id TO PARAMETER 0, 
 team_id TO PARAMETER 1) 
```

Cet exemple exploite la plus grande flexibilité de la clause SQL WHERE pour obtenir le résultat escompté.

