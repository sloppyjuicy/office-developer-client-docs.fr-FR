---
title: COMPUTE, clause de commande SHAPE
TOCTitle: Shape Compute Clause
ms:assetid: f4fee4a6-ec9e-c0b6-40e0-258f76c4696f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250245(v=office.15)
ms:contentKeyID: 48548699
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8e35cfc7bc5df144fa1938f794cb705bf2f1448c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889930"
---
# <a name="shape-compute-clause"></a>COMPUTE, clause de commande SHAPE

**S’applique à**: Access 2013, Office 2013

Une clause COMPUTE de commande SHAPE génère un objet **Recordset** parent dont les colonnes se composent d'une référence à l'objet **Recordset** enfant, de colonnes facultatives contenant des colonnes de chapitre, des nouvelles colonnes ou des colonnes calculées ou encore le résultat de l'exécution de fonctions d'agrégation sur l'objet **Recordset** enfant ou un objet **Recordset** précédemment mis en forme et de toutes colonnes provenant de l'objet **Recordset** enfant répertoriées dans la clause BY facultative.

## <a name="syntax"></a>Syntaxe

```vb 
 
SHAPE child-command [AS] child-alias 
   COMPUTE child-alias [[AS] name], [appended-column-list] 
   [BY grp-field-list] 
```

## <a name="description"></a>Description

Cette clause comporte les parties suivantes :

- *child-command*

  - Est constituée de l'un des éléments suivants :
    
    - Commande de requête entre accolades (« {} ») qui retourne un objet **Recordset** enfant. La commande est transmise au fournisseur de données sous-jacent et sa syntaxe dépend des exigences du fournisseur. Elle est en général écrite en langage SQL, même si ADO n'exige pas de langage de requête particulier.
    
    - Nom d'un objet **Recordset** mis en forme existant.
    
    - Autre commande SHAPE.
    
    - Mot-clé TABLE, suivi du nom d'une table du fournisseur de données.

- *child-alias*

  - Alias utilisé pour faire référence à l' **objet Recordset** renvoyé par la *commande child-command.* L' *alias-enfant* est requise dans la liste des colonnes dans la clause COMPUTE et définit la relation entre les objets **Recordset** parent et enfant.

- *appended-column-list*

  - Liste dans laquelle chaque élément définit une colonne dans le parent généré. Chaque élément contient une colonne de chapitre, une nouvelle colonne, une colonne calculée ou une valeur résultant d'une fonction d'agrégation exécutée sur l'objet **Recordset** enfant.

- *grp-field-list*

  - Une liste de colonnes dans les objets **Recordset** parent et enfant qui spécifie la façon dont les lignes doivent être regroupés dans l’enfant. Pour chaque colonne dans le *groupe champ liste,* il existe une colonne correspondante dans les objets **Recordset** parent et enfant. Ont des valeurs uniques pour chaque ligne dans **l’objet Recordset**parent, les colonnes de la *liste de champs de groupe* et l’enfant **Recordset** référencé par la ligne parente se compose uniquement d’enfants dont la *liste de champs de groupe* de lignes colonnes ont la même valeur que la ligne parente.

Si la clause BY est incluse, les lignes de l'objet **Recordset** enfant sont groupées en fonction des colonnes dans la clause COMPUTE. L'objet **Recordset** parent contiendra une ligne pour chaque groupe de lignes de l'objet **Recordset** enfant.

En revanche, si la clause BY est omise, l'intégralité de l'objet **Recordset** enfant est traité comme un seul groupe et l'objet **Recordset** parent contient exactement une ligne. Cette ligne référence tout l'objet **Recordset** enfant. L'omission de la clause BY vous permet de calculer des agrégats de « totaux » pour tout l'objet **Recordset** enfant.

Par exemple :

```vb
    SHAPE {select * from Orders} AS orders
       COMPUTE orders, SUM(orders.OrderAmount) as TotalSales
```

Quelle que soit la façon dont l'objet **Recordset** parent est formé (à l'aide de la clause COMPUTE ou APPEND), celui-ci contiendra une colonne de chapitre utilisée pour établir une relation avec un objet **Recordset** enfant. Si vous le souhaitez, l'objet **Recordset** parent peut également contenir des colonnes comportant des agrégats (SUM, MIN, MAX, etc.) sur les lignes enfants. Les objets **Recordset** parent et enfant peuvent tous deux contenir des colonnes comportant une expression sur la ligne dans l'objet **Recordset** ainsi que des nouvelles colonnes, initialement vides.

## <a name="operation"></a>Déroulement de l'opération

La *commande child-command* est transmise au fournisseur, qui renvoie un **objet Recordset**enfant.

La clause COMPUTE spécifie les colonnes de l'objet **Recordset** parent, par exemple une référence à l'objet **Recordset** enfant, un ou plusieurs agrégats, une expression calculée ou de nouvelles colonnes. Si une clause BY est employée, les colonnes qu'elle définit sont également ajoutées à l'objet **Recordset** parent. La clause BY spécifie la façon dont les lignes d'un objet **Recordset** enfant sont groupées.

Par exemple, supposons que nous disposons d'une table, Demographics, comportant les champs State, City et Population (les chiffres ne sont donnés qu'à titre d'exemple).

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>State</p></th>
<th><p>City</p></th>
<th><p>Population</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>WA</p></td>
<td><p>Seattle</p></td>
<td><p>700 000</p></td>
</tr>
<tr class="even">
<td><p>OR</p></td>
<td><p>Medford</p></td>
<td><p>200 000</p></td>
</tr>
<tr class="odd">
<td><p>OR</p></td>
<td><p>Portland</p></td>
<td><p>400 000</p></td>
</tr>
<tr class="even">
<td><p>CA</p></td>
<td><p>Los Angeles</p></td>
<td><p>800 000</p></td>
</tr>
<tr class="odd">
<td><p>CA</p></td>
<td><p>San Diego</p></td>
<td><p>600 000</p></td>
</tr>
<tr class="even">
<td><p>WA</p></td>
<td><p>Tacoma</p></td>
<td><p>500 000</p></td>
</tr>
<tr class="odd">
<td><p>OR</p></td>
<td><p>Corvallis</p></td>
<td><p>300 000</p></td>
</tr>
</tbody>
</table>


Émettez à présent cette commande SHAPE :

```vb 
 
rst.Open  "SHAPE {select * from demographics} AS rs "  & _ 
          "COMPUTE rs, SUM(rs.population) BY state", _ 
           objConnection 
```

Cette commande ouvre un objet **Recordset** mis en forme comportant deux niveaux. Le niveau parent est un **jeu d’enregistrements** de généré avec une colonne agrégée (SUM(rs.population)), une colonne référençant l' **objet Recordset** (rs) enfant et une colonne permettant de grouper l’enfant du **jeu d’enregistrements** (état). Le niveau enfant est le **jeu d’enregistrements** renvoyé par la commande de requête (), une colonne référençant l' **objet Recordset** (rs) enfant et une colonne permettant de grouper l’enfant du **jeu d’enregistrements** (état). Le niveau enfant est l' **objet Recordset** renvoyé par la commande de requête (sélectionnez \* à partir de données démographiques).

Les lignes de détail de l'objet **Recordset** sont groupées en fonction de la colonne State, mais dans aucun ordre particulier. En d'autres termes, les groupes ne sont pas classés par ordre alphabétique ou numérique. Si vous voulez trier l'objet **Recordset** parent, utilisez la méthode **Sort** **Recordset** pour trier l'objet **Recordset** parent.

Vous pouvez désormais parcourir l'objet **Recordset** parent et accéder aux objets **Recordset** de détail enfants. Pour plus d'informations, consultez [Accès aux lignes d'un jeu d'enregistrements hiérarchique](accessing-rows-in-a-hierarchical-recordset.md).

**Objets Recordset parent et enfants résultants**

**Parent**

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>SUM (rs.Population)</p></th>
<th><p>rs</p></th>
<th><p>State</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1,300,000</p></td>
<td><p>Référence à Enfant 1</p></td>
<td><p>CA</p></td>
</tr>
<tr class="even">
<td><p>1,200,000</p></td>
<td><p>Référence à Enfant 2</p></td>
<td><p>WA</p></td>
</tr>
<tr class="odd">
<td><p>1,100,000</p></td>
<td><p>Référence à Enfant 3</p></td>
<td><p>OR</p></td>
</tr>
</tbody>
</table>


**Enfant 1**

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>State</p></th>
<th><p>City</p></th>
<th><p>Population</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>CA</p></td>
<td><p>Los Angeles</p></td>
<td><p>800 000</p></td>
</tr>
<tr class="even">
<td><p>CA</p></td>
<td><p>San Diego</p></td>
<td><p>600 000</p></td>
</tr>
</tbody>
</table>


**Enfant 2**

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>State</p></th>
<th><p>City</p></th>
<th><p>Population</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>WA</p></td>
<td><p>Seattle</p></td>
<td><p>700 000</p></td>
</tr>
<tr class="even">
<td><p>WA</p></td>
<td><p>Tacoma</p></td>
<td><p>500 000</p></td>
</tr>
</tbody>
</table>


**Enfant 3**

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>State</p></th>
<th><p>City</p></th>
<th><p>Population</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>OR</p></td>
<td><p>Medford</p></td>
<td><p>200 000</p></td>
</tr>
<tr class="even">
<td><p>OR</p></td>
<td><p>Portland</p></td>
<td><p>400 000</p></td>
</tr>
<tr class="odd">
<td><p>OR</p></td>
<td><p>Corvallis</p></td>
<td><p>300 000</p></td>
</tr>
</tbody>
</table>

