---
title: Service de curseur Microsoft pour OLE DB (composant du service ADO)
TOCTitle: Microsoft Cursor Service for OLE DB (ADO Service Component)
ms:assetid: 6818fc05-9c9f-9b67-07d2-e622c93133c2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249405(v=office.15)
ms:contentKeyID: 48545376
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: cebf2de36d7f15dcfdf54f6d96a339791e72fd75
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63632776"
---
# <a name="microsoft-cursor-service-for-ole-db-ado-service-component"></a>Service de curseur Microsoft pour OLE DB (composant de service ADO)


**S’applique à** : Access 2013, Office 2013

Le service de curseur Microsoft pour OLE DB complète les fonctions de prise en charge du curseur des fournisseurs de données. L'utilisateur a ainsi une perception relativement uniforme des fonctionnalités des différents fournisseurs de données.

Le service de curseur rend les propriétés dynamiques accessibles et améliore le comportement de certaines méthodes. Par exemple, la propriété dynamique [Optimize](optimize-property-dynamic-ado.md) permet la création d'index temporaires qui facilitent certaines opérations comme la méthode [Find](find-method-ado.md).

Dans tous les cas, le service de curseur prend en charge la mise à jour en lot. Il simule également des types de curseurs plus puissants comme les curseurs dynamiques lorsqu'un fournisseur de données ne peut fournir que des curseurs d'une capacité moindre comme les curseurs statiques.

## <a name="keyword"></a>Keyword

Pour appeler ce composant de service, définissez la propriété [CursorLocation](cursorlocation-property-ado.md) de l’objet [Recordset](recordset-object-ado.md) ou [Connection](connection-object-ado.md) sur **adUseClient**.

`connection.CursorLocation=adUseClientrecordset.CursorLocation=adUseClient`

## <a name="dynamic-properties"></a>Propriétés dynamiques

Lorsque le service de curseur pour OLE DB est appelé, les propriétés dynamiques suivantes sont ajoutées à la collection [Properties](properties-collection-ado.md) de l’objet **Recordset**. La liste complète des propriétés dynamiques des objets **Connection** et **Recordset** apparaît dans l’[Index des propriétés dynamiques ADO](ado-dynamic-property-index.md). Les noms de propriété OLE DB associés sont, le cas échéant, insérés entre parenthèses après le nom de propriété ADO.

Après l'appel du service de curseur, les modifications apportées à certaines propriétés dynamiques sont invisibles pour la source de données sous-jacente. Par exemple, la définition de la propriété *Command Time out* sur un **Recordset** reste invisible pour le fournisseur de données sous-jacent.

```vb 
... 
Recordset1.CursorLocation = adUseClient 'invokes cursor service 
Recordset1.Open "authors", _ 
 "Provider=SQLOLEDB;Data Source=DBServer;User Id=usr;" & _ 
 "Password=pwd;Initial Catalog=pubs;",,adCmdTable 
Recordset1.Properties.Item("Command Time out") = 50 
' 'Command Time out' property on DBServer is still default (30). 
... 

```

Si votre application nécessite le service de curseur et que vous avez besoin de définir des propriétés dynamiques sur le fournisseur sous-jacent, définissez ces propriétés avant d'invoquer le service de curseur. Les paramètres de propriété d'objet de commande sont toujours transmis au fournisseur de données sous-jacent quel que soit l'emplacement du curseur. Par conséquent, vous pouvez également utiliser un objet de commande pour définir à tout moment les propriétés.

> [!NOTE]
> [!REMARQUE] La propriété dynamique DBPROP_SERVERDATAONINSERT n'est pas prise en charge par le service de curseur, même si elle est prise en charge par le fournisseur de données sous-jacent.



<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom de la propriété</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Auto Recalc<br />
(DBPROP_ADC_AUTORECALC)</p></td>
<td><p>Pour les jeux d'enregistrement créés avec Microsoft Data Shaping Service, cette valeur indique la fréquence de calcul des colonnes calculées et agrégées. La valeur par défaut (value=1) indique qu'un nouveau calcul doit être effectué chaque fois que Microsoft Data Shaping Service détecte une modification des valeurs. Si la valeur est égale à 0, les colonnes calculées et agrégées ne sont calculées que lors de la composition initiale de la hiérarchie.</p></td>
</tr>
<tr class="even">
<td><p>Batch Size<br />
(DBPROP_ADC_BATCHSIZE)</p></td>
<td><p>Indique le nombre d'instructions de mise à jour pouvant être insérées dans un même lot pour leur envoi au magasin de données. Plus le lot contient d'instructions, moins les allers-retours au magasin de données seront nombreux.</p></td>
</tr>
<tr class="odd">
<td><p>Cache Child Rows<br />
(DBPROP_ADC_CACHECHILDROWS)</p></td>
<td><p>Pour les jeux d'enregistrements créés avec Microsoft Data Shaping Service, cette valeur indique si les jeux d'enregistrements enfants sont stockés en cache en vue d'une utilisation ultérieure.</p></td>
</tr>
<tr class="even">
<td><p>Cursor Engine Version<br />
(DBPROP_ADC_CEVER)</p></td>
<td><p>Indique la version du service de curseur utilisée.</p></td>
</tr>
<tr class="odd">
<td><p>Maintain Change Status<br />
(DBPROP_ADC_MAINTAINCHANGESTATUS)</p></td>
<td><p>Indique le texte de la commande à utiliser pour resynchroniser une ou plusieurs lignes dans une jointure de plusieurs tables.</p></td>
</tr>
<tr class="even">
<td><p><a href="optimize-property-dynamic-ado.md">Optimiser</a></p></td>
<td><p>Indique s'il faut créer un index. Si cette propriété est définie sur <strong>True</strong>, la création temporaire d'index est autorisée pour améliorer l'exécution de certaines opérations.</p></td>
</tr>
<tr class="odd">
<td><p><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></p></td>
<td><p>Indique le nom du <strong>Recordset</strong>. Peut être référencé dans les commandes actuelles ou suivantes de mise en forme des données.</p></td>
</tr>
<tr class="even">
<td><p><a href="resync-command-property-dynamic-ado.md">Resync Command</a></p></td>
<td><p>Indique une chaîne de commande personnalisée utilisée par la méthode <a href="resync-method-ado.md">Resync</a> lorsque la propriété <a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table</a> est en vigueur.</p></td>
</tr>
<tr class="odd">
<td><p><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Catalog</a></p></td>
<td><p>Indique le nom de la base de données contenant la table référencée dans la propriété <strong>Unique Table</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Schema</a></p></td>
<td><p>Indique le nom du propriétaire de la table référencée dans la propriété <strong>Unique Table</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table</a></p></td>
<td><p>Indique le nom de la table unique dans un <strong>Recordset</strong> créé à partir de plusieurs tables modifiables par insertion, mise à jour ou suppression.</p></td>
</tr>
<tr class="even">
<td><p>Update Criteria<br />
(DBPROP_ADC_UPDATECRITERIA)</p></td>
<td><p>Indique les champs de la clause <strong>WHERE</strong> utilisés pour gérer les collisions survenant lors des mises à jour.</p></td>
</tr>
<tr class="odd">
<td><p><a href="update-resync-property-dynamic-ado.md">Update Resync</a>(DBPROP_ADC_UPDATERESYNC)</p></td>
<td><p>Indique si la méthode <strong>Resync</strong> est implicitement appelée après la méthode <a href="updatebatch-method-ado.md">UpdateBatch </a> (et son comportement) lorsque la propriété <strong>Unique Table</strong> est en vigueur.</p></td>
</tr>
</tbody>
</table>


Vous pouvez également définir ou extraire une propriété dynamique en spécifiant son nom en tant qu’index de la collection **Properties**. Par exemple, vous pouvez obtenir et imprimer la valeur actuelle de la propriété dynamique [Optimize](optimize-property-dynamic-ado.md), puis définir une nouvelle valeur de la façon suivante :

```vb 
 
Debug.Print rs.Properties("Optimize") 
rs.Properties("Optimize") = True 
```

## <a name="built-in-property-behavior"></a>Comportement des propriétés intégrées

Le service de curseur pour OLE DB affecte également le comportement de certaines propriétés intégrées.

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom de la propriété</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="cursortype-property-ado.md">CursorType</a></p></td>
<td><p>Complète les types de curseurs disponibles pour un <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="locktype-property-ado.md">LockType</a></p></td>
<td><p>Complète les types de verrous disponibles pour un <strong>Recordset</strong>. Permet la mise à jour en lot.</p></td>
</tr>
<tr class="odd">
<td><p><a href="sort-property-ado.md">Sort</a></p></td>
<td><p>Indique le ou les noms de champ utilisés pour trier le <strong>Recordset</strong> ; indique également pour chaque champ si le tri doit s'effectuer dans l'ordre croissant ou dans l'ordre décroissant.</p></td>
</tr>
</tbody>
</table>


## <a name="method-behavior"></a>Comportement des méthodes

Le service de curseur pour OLE DB active ou affecte le comportement de la méthode [Append](append-method-ado.md) de l’objet [Field](field-object-ado.md) et des méthodes [Open](open-method-ado-recordset.md), [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) et [Save](save-method-ado.md) de l’objet **Recordset**.

