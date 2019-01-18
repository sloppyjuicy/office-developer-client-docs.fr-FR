---
title: Autres méthodes pour se déplacer dans un recordset
TOCTitle: More ways to move in a Recordset
ms:assetid: ae49b20e-0050-c44b-67e9-7e39de5098c4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249822(v=office.15)
ms:contentKeyID: 48547067
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2d10a493aac39934a047c6fa311233fd6c9fac4e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710572"
---
# <a name="more-ways-to-move-in-a-recordset"></a>Autres méthodes pour se déplacer dans un recordset

**S’applique à**: Access 2013, Office 2013

Les quatre méthodes suivantes vous permettent de vous déplacer dans l'objet **Recordset** ou de parcourir celui-ci : [MoveFirst, MoveLast, MoveNext et MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md). Notez que certaines de ces méthodes ne sont pas disponibles avec des curseurs avant uniquement.

**MoveFirst** fait du premier enregistrement de l'objet **Recordset** l'enregistrement actif. **MoveLast** fait du dernier enregistrement de l'objet **Recordset** l'enregistrement actif. Pour pouvoir utiliser les méthodes **MoveFirst** ou **MoveLast**, l'objet **Recordset** doit prendre en charge les signets ou le déplacement de curseur arrière. Dans le cas contraire, l'appel de la méthode génère une erreur.

**MoveNext** fait avancer l'enregistrement actif d'une position. Si vous êtes au niveau du dernier enregistrement lors de l'appel de la méthode **MoveNext**, la propriété **EOF** prend la valeur **True**. **MovePrevious** fait reculer l'enregistrement actif d'une position. Si vous êtes au niveau du premier enregistrement lors de l'appel de la méthode **MovePrevious**, la propriété **BOF** prend la valeur **True**. Il est utile de vérifier la valeur des propriétés **EOF** et **BOF** lors de l'utilisation de ces méthodes, et de replacer le curseur à une position d'enregistrement actif valide si vous dépassez l'une des extrémités de l'objet **Recordset**, comme dans l'exemple suivant :

```vb
. . . 
oRs.MoveNext 
If oRs.EOF Then oRs.MoveLast 
. . . 
```

Ou, dans le cas de la méthode **MovePrevious**:

```vb
. . . 
oRs.MovePrevious 
If oRs.BOF Then oRs.MoveFirst 
. . . 
```

Dans le cas où l' **objet Recordset** a été filtré ou trié et données de l’enregistrement actif sont modifiées, la position peut également changer. Dans ce cas, la méthode **MoveNext** fonctionne normalement, mais vous oubliez pas que la position est déplacé d’un enregistrement à partir de la nouvelle position, pas de l’ancien. Modification des données dans l’enregistrement en cours, telles que l’enregistrement est déplacé à la fin du tri **jeu d’enregistrements**, par exemple, qui signifie que appelant **MoveNext** l'aboutit à ADO la définition de l’enregistrement actif sur la position après le dernier enregistrement dans le ** Jeu d’enregistrements** (**EOF** = **la valeur True**).

Le comportement des diverses méthodes Move de l’objet **Recordset** dépend, dans une certaine mesure, sur les données de l' **objet Recordset**. Nouveaux enregistrements ajoutés à l' **objet Recordset** sont initialement ajoutés dans un ordre particulier, qui est défini par la source de données et peut-être dépendre, implicitement ou explicitement des données dans le nouvel enregistrement. Par exemple, si un tri ou une jointure est effectuée dans la requête qui remplit l' **objet Recordset**, le nouvel enregistrement sera inséré dans l’emplacement approprié dans le **jeu d’enregistrements**. Si la commande n’est pas explicitement spécifié lors de la création de l' **objet Recordset**, les modifications dans l’implémentation de source de données peuvent entraîner l’ordre des lignes renvoyées modifier par inadvertance. En outre, le tri, filtrage et modification des fonctions de **l’objet Recordset** peuvent affectent l’ordre et l’affichage des lignes dans le jeu d’enregistrements.

Les méthodes **MoveNext**, **MovePrevious**, **MoveFirst**, **MoveLast** et **Move** sont donc sensibles aux autres opérations effectuées dans le même objet **Recordset**. Même si ADO tente toujours de conserver votre position active jusqu'à ce que vous la déplaciez explicitement, il arrive que les modifications intervenues rendent l'impact d'un changement ultérieur difficilement prévisible. Supposons, par exemple, que vous appeliez la méthode **MoveFirst** pour accéder à la première ligne d'un objet **Recordset** trié. Si vous changez l'ordre de tri ascendant en ordre descendant, vous êtes toujours sur la même ligne , mais il s'agit désormais de la dernière ligne de l'objet **Recordset**. La méthode **MoveFirst** vous permet d'accéder à une autre ligne (la nouvelle première ligne).

Autre exemple : vous êtes positionné sur une ligne donnée, au milieu d'un objet **Recordset**, et vous appelez la méthode **Delete**, puis la méthode **MoveNext**. Vous êtes donc au niveau de l'enregistrement qui suit directement l'enregistrement supprimé. Mais l'appel de la méthode **MovePrevious** fait de l'enregistrement précédant celui que vous avez supprimé l'enregistrement actif, car l'enregistrement supprimé n'est plus considéré comme un membre actif du **Recordset**.

Il est particulièrement difficile de définir une sémantique de déplacement cohérente entre tous les fournisseurs pour les méthodes qui exécutent des déplacements relatifs à l'enregistrement actif, à savoir **MovePrevious**, **MoveNext** et **Move** , en raison des modifications apportées aux données de l'enregistrement actif. Imaginons que vous utilisez un **Recordset** trié et filtré. Vous modifiez les données de l'enregistrement actif de telle sorte qu'il précède tous les autres enregistrements mais vos données modifiées ne correspondent plus au filtre. Dans ce cas, il est difficile de prévoir le résultat d'une opération **MoveNext**. En guise de conclusion, nous dirons donc que les déplacements relatifs au sein d'un objet **Recordset** sont plus risqués que les déplacements absolus (tels que les opérations **MoveFirst** ou **MoveLast**) lorsque les données sont modifiées par l'ajout, la suppression ou la modification des enregistrements. Il est conseillé de baser les opérations de tri et de filtrage sur une clé primaire ou un ID, car ce type de valeur reste inchangé.

