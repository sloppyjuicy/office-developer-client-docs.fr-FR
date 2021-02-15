---
title: Service de curseur Microsoft pour OLE DB (composant du service ADO)
TOCTitle: Microsoft Cursor Service for OLE DB (ADO Service Component)
ms:assetid: 6818fc05-9c9f-9b67-07d2-e622c93133c2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249405(v=office.15)
ms:contentKeyID: 48545376
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d79d060922c6e7f28209242ebe82821c2ba97bfd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288987"
---
# <a name="microsoft-cursor-service-for-ole-db-ado-service-component"></a><span data-ttu-id="02298-102">Service de curseur Microsoft pour OLE DB (composant de service ADO)</span><span class="sxs-lookup"><span data-stu-id="02298-102">Microsoft Cursor Service for OLE DB (ADO Service Component)</span></span>


<span data-ttu-id="02298-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="02298-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="02298-p101">Le service de curseur Microsoft pour OLE DB complète les fonctions de prise en charge du curseur des fournisseurs de données. L'utilisateur a ainsi une perception relativement uniforme des fonctionnalités des différents fournisseurs de données.</span><span class="sxs-lookup"><span data-stu-id="02298-p101">The Microsoft Cursor Service for OLE DB supplements the cursor support functions of data providers. As a result, the user perceives relatively uniform functionality from all data providers.</span></span>

<span data-ttu-id="02298-p102">Le service de curseur rend les propriétés dynamiques accessibles et améliore le comportement de certaines méthodes. Par exemple, la propriété dynamique [Optimize](optimize-property-dynamic-ado.md) permet la création d'index temporaires qui facilitent certaines opérations comme la méthode [Find](find-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="02298-p102">The Cursor Service makes dynamic properties available and enhances the behavior of certain methods. For example, the [Optimize](optimize-property-dynamic-ado.md) dynamic property enables the creation of temporary indexes to facilitate certain operations, such as the [Find](find-method-ado.md) method.</span></span>

<span data-ttu-id="02298-p103">Dans tous les cas, le service de curseur prend en charge la mise à jour en lot. Il simule également des types de curseurs plus puissants comme les curseurs dynamiques lorsqu'un fournisseur de données ne peut fournir que des curseurs d'une capacité moindre comme les curseurs statiques.</span><span class="sxs-lookup"><span data-stu-id="02298-p103">The Cursor Service enables support for batch updating in all cases. It also simulates more capable cursor types, such as dynamic cursors, when a data provider can only supply less capable cursors, such as static cursors.</span></span>

## <a name="keyword"></a><span data-ttu-id="02298-110">Mot clé</span><span class="sxs-lookup"><span data-stu-id="02298-110">Keyword</span></span>

<span data-ttu-id="02298-111">Pour appeler ce composant de service, définissez la propriété [CursorLocation](cursorlocation-property-ado.md) de l’objet [Recordset](recordset-object-ado.md) ou [Connection](connection-object-ado.md) sur **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="02298-111">To invoke this service component, set the [Recordset](recordset-object-ado.md) or [Connection](connection-object-ado.md) object's [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient**.</span></span>

`connection.CursorLocation=adUseClientrecordset.CursorLocation=adUseClient`

## <a name="dynamic-properties"></a><span data-ttu-id="02298-112">Propriétés dynamiques</span><span class="sxs-lookup"><span data-stu-id="02298-112">Dynamic Properties</span></span>

<span data-ttu-id="02298-p104">Lorsque le service de curseur pour OLE DB est appelé, les propriétés dynamiques suivantes sont ajoutées à la collection [Properties](properties-collection-ado.md) de l’objet **Recordset**. La liste complète des propriétés dynamiques des objets **Connection** et **Recordset** apparaît dans l’[Index des propriétés dynamiques ADO](ado-dynamic-property-index.md). Les noms de propriété OLE DB associés sont, le cas échéant, insérés entre parenthèses après le nom de propriété ADO.</span><span class="sxs-lookup"><span data-stu-id="02298-p104">When the Cursor Service for OLE DB is invoked, the following dynamic properties are added to the **Recordset** object's [Properties](properties-collection-ado.md) collection. The full list of **Connection** and **Recordset** object dynamic properties is listed in the [ADO Dynamic Property Index](ado-dynamic-property-index.md). The associated OLE DB property names, where appropriate, are included in parenthesis after the ADO property name.</span></span>

<span data-ttu-id="02298-p105">Après l'appel du service de curseur, les modifications apportées à certaines propriétés dynamiques sont invisibles pour la source de données sous-jacente. Par exemple, la définition de la propriété *Command Time out* sur un **Recordset** reste invisible pour le fournisseur de données sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="02298-p105">Changes to some dynamic properties are not visible to the underlying data source after the Cursor Service has been invoked. For example, setting the *Command Time out* property on a **Recordset** will not be visible to the underlying data provider.</span></span>

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

<span data-ttu-id="02298-p106">Si votre application nécessite le service de curseur et que vous avez besoin de définir des propriétés dynamiques sur le fournisseur sous-jacent, définissez ces propriétés avant d'invoquer le service de curseur. Les paramètres de propriété d'objet de commande sont toujours transmis au fournisseur de données sous-jacent quel que soit l'emplacement du curseur. Par conséquent, vous pouvez également utiliser un objet de commande pour définir à tout moment les propriétés.</span><span class="sxs-lookup"><span data-stu-id="02298-p106">If your application requires the Cursor Service, but you need to set dynamic properties on the underlying provider, set the properties before invoking the Cursor Service. Command object property settings are always passed to the underlying data provider regardless of cursor location. Therefore, you can also use a command object to set the properties at any time.</span></span>

> [!NOTE]
> <span data-ttu-id="02298-121">[!REMARQUE] La propriété dynamique DBPROP_SERVERDATAONINSERT n'est pas prise en charge par le service de curseur, même si elle est prise en charge par le fournisseur de données sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="02298-121">The dynamic property DBPROP_SERVERDATAONINSERT is not supported by the cursor service, even if it is supported by the underlying data provider.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="02298-122">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="02298-122">Property Name</span></span></p></th>
<th><p><span data-ttu-id="02298-123">Description</span><span class="sxs-lookup"><span data-stu-id="02298-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="02298-124">Auto Recalc</span><span class="sxs-lookup"><span data-stu-id="02298-124">Auto Recalc</span></span><br />
<span data-ttu-id="02298-125">(DBPROP_ADC_AUTORECALC)</span><span class="sxs-lookup"><span data-stu-id="02298-125">(DBPROP_ADC_AUTORECALC)</span></span></p></td>
<td><p><span data-ttu-id="02298-p107">Pour les jeux d'enregistrement créés avec Microsoft Data Shaping Service, cette valeur indique la fréquence de calcul des colonnes calculées et agrégées. La valeur par défaut (value=1) indique qu'un nouveau calcul doit être effectué chaque fois que Microsoft Data Shaping Service détecte une modification des valeurs. Si la valeur est égale à 0, les colonnes calculées et agrégées ne sont calculées que lors de la composition initiale de la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="02298-p107">For recordsets created with the Data Shaping Service, this value indicates how often calculated and aggregate columns are calculated. The default (value=1) is to recalculate whenever the Data Shaping Service determines that the values have changed. If the value is 0, the calculated or aggregate columns are only calculated when the hierarchy is initially built.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02298-129">Batch Size</span><span class="sxs-lookup"><span data-stu-id="02298-129">Batch Size</span></span><br />
<span data-ttu-id="02298-130">(DBPROP_ADC_BATCHSIZE)</span><span class="sxs-lookup"><span data-stu-id="02298-130">(DBPROP_ADC_BATCHSIZE)</span></span></p></td>
<td><p><span data-ttu-id="02298-p108">Indique le nombre d'instructions de mise à jour pouvant être insérées dans un même lot pour leur envoi au magasin de données. Plus le lot contient d'instructions, moins les allers-retours au magasin de données seront nombreux.</span><span class="sxs-lookup"><span data-stu-id="02298-p108">Indicates the number of update statements that can be batched before being sent to the data store. The more statements in a batch, the fewer round trips to the data store.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02298-133">Cache Child Rows</span><span class="sxs-lookup"><span data-stu-id="02298-133">Cache Child Rows</span></span><br />
<span data-ttu-id="02298-134">(DBPROP_ADC_CACHECHILDROWS)</span><span class="sxs-lookup"><span data-stu-id="02298-134">(DBPROP_ADC_CACHECHILDROWS)</span></span></p></td>
<td><p><span data-ttu-id="02298-135">Pour les jeux d'enregistrements créés avec Microsoft Data Shaping Service, cette valeur indique si les jeux d'enregistrements enfants sont stockés en cache en vue d'une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="02298-135">For recordsets created with the Data Shaping Service, this value indicates whether child recordsets are stored in a cache for later use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02298-136">Cursor Engine Version</span><span class="sxs-lookup"><span data-stu-id="02298-136">Cursor Engine Version</span></span><br />
<span data-ttu-id="02298-137">(DBPROP_ADC_CEVER)</span><span class="sxs-lookup"><span data-stu-id="02298-137">(DBPROP_ADC_CEVER)</span></span></p></td>
<td><p><span data-ttu-id="02298-138">Indique la version du service de curseur utilisée.</span><span class="sxs-lookup"><span data-stu-id="02298-138">Indicates the version of the Cursor Service being used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02298-139">Maintain Change Status</span><span class="sxs-lookup"><span data-stu-id="02298-139">Maintain Change Status</span></span><br />
<span data-ttu-id="02298-140">(DBPROP_ADC_MAINTAINCHANGESTATUS)</span><span class="sxs-lookup"><span data-stu-id="02298-140">(DBPROP_ADC_MAINTAINCHANGESTATUS)</span></span></p></td>
<td><p><span data-ttu-id="02298-141">Indique le texte de la commande à utiliser pour resynchroniser une ou plusieurs lignes dans une jointure de plusieurs tables.</span><span class="sxs-lookup"><span data-stu-id="02298-141">Indicates the text of the command used for resynchronizing a one or more rows in a multiple table join.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02298-142"><a href="optimize-property-dynamic-ado.md">Optimiser</a></span><span class="sxs-lookup"><span data-stu-id="02298-142"><a href="optimize-property-dynamic-ado.md">Optimize</a></span></span></p></td>
<td><p><span data-ttu-id="02298-p109">Indique s'il faut créer un index. Si cette propriété est définie sur <strong>True</strong>, la création temporaire d'index est autorisée pour améliorer l'exécution de certaines opérations.</span><span class="sxs-lookup"><span data-stu-id="02298-p109">Indicates whether an index should be created. When set to <strong>True</strong>, authorizes the temporary creation of indexes to improve the execution of certain operations.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02298-145"><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></span><span class="sxs-lookup"><span data-stu-id="02298-145"><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></span></span></p></td>
<td><p><span data-ttu-id="02298-146">Indique le nom du <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="02298-146">Indicates the name of the <strong>Recordset</strong>.</span></span> <span data-ttu-id="02298-147">Peut être référencé dans les commandes actuelles ou suivantes de mise en forme des données.</span><span class="sxs-lookup"><span data-stu-id="02298-147">May be referenced within the current, or subsequent, data shaping commands.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02298-148"><a href="resync-command-property-dynamic-ado.md">Resync Command</a></span><span class="sxs-lookup"><span data-stu-id="02298-148"><a href="resync-command-property-dynamic-ado.md">Resync Command</a></span></span></p></td>
<td><p><span data-ttu-id="02298-149">Indique une chaîne de commande personnalisée utilisée par la méthode <a href="resync-method-ado.md">Resync</a> lorsque la propriété <a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table</a> est en vigueur.</span><span class="sxs-lookup"><span data-stu-id="02298-149">Indicates a custom command string that is used by the <a href="resync-method-ado.md">Resync</a> method when the <a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table</a> property is in effect.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02298-150"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Catalog</a></span><span class="sxs-lookup"><span data-stu-id="02298-150"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Catalog</a></span></span></p></td>
<td><p><span data-ttu-id="02298-151">Indique le nom de la base de données contenant la table référencée dans la propriété <strong>Unique Table</strong>.</span><span class="sxs-lookup"><span data-stu-id="02298-151">Indicates the name of the database containing the table referenced in the <strong>Unique Table</strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02298-152"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Schema</a></span><span class="sxs-lookup"><span data-stu-id="02298-152"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Schema</a></span></span></p></td>
<td><p><span data-ttu-id="02298-153">Indique le nom du propriétaire de la table référencée dans la propriété <strong>Unique Table</strong>.</span><span class="sxs-lookup"><span data-stu-id="02298-153">Indicates the name of the owner of the table referenced in the <strong>Unique Table</strong> property.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02298-154"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table</a></span><span class="sxs-lookup"><span data-stu-id="02298-154"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table</a></span></span></p></td>
<td><p><span data-ttu-id="02298-155">Indique le nom de la table unique dans un <strong>Recordset</strong> créé à partir de plusieurs tables modifiables par insertion, mise à jour ou suppression.</span><span class="sxs-lookup"><span data-stu-id="02298-155">Indicates the name of the one table in a <strong>Recordset</strong> created from multiple tables that may be modified by insertions, updates, or deletions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02298-156">Update Criteria</span><span class="sxs-lookup"><span data-stu-id="02298-156">Update Criteria</span></span><br />
<span data-ttu-id="02298-157">(DBPROP_ADC_UPDATECRITERIA)</span><span class="sxs-lookup"><span data-stu-id="02298-157">(DBPROP_ADC_UPDATECRITERIA)</span></span></p></td>
<td><p><span data-ttu-id="02298-158">Indique les champs de la clause <strong>WHERE</strong> utilisés pour gérer les collisions survenant lors des mises à jour.</span><span class="sxs-lookup"><span data-stu-id="02298-158">Indicates which fields in the <strong>WHERE</strong> clause are used to handle collisions occurring during an update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02298-159"><a href="update-resync-property-dynamic-ado.md">Update Resync</a>(DBPROP_ADC_UPDATERESYNC)</span><span class="sxs-lookup"><span data-stu-id="02298-159"><a href="update-resync-property-dynamic-ado.md">Update Resync</a>(DBPROP_ADC_UPDATERESYNC)</span></span></p></td>
<td><p><span data-ttu-id="02298-160">Indique si la méthode <strong>Resync</strong> est implicitement appelée après la méthode <a href="updatebatch-method-ado.md">UpdateBatch </a> (et son comportement) lorsque la propriété <strong>Unique Table</strong> est en vigueur.</span><span class="sxs-lookup"><span data-stu-id="02298-160">Indicates whether the <strong>Resync</strong> method is implicitly invoked after the <a href="updatebatch-method-ado.md">UpdateBatch</a> method (and its behavior), when the <strong>Unique Table</strong> property is in effect.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="02298-p111">Vous pouvez également définir ou extraire une propriété dynamique en spécifiant son nom en tant qu’index de la collection **Properties**. Par exemple, vous pouvez obtenir et imprimer la valeur actuelle de la propriété dynamique [Optimize](optimize-property-dynamic-ado.md), puis définir une nouvelle valeur de la façon suivante :</span><span class="sxs-lookup"><span data-stu-id="02298-p111">You may also set or retrieve a dynamic property by specifying its name as the index to the **Properties** collection. For example, get and print the current value of the [Optimize](optimize-property-dynamic-ado.md) dynamic property, then set a new value, like this:</span></span>

```vb 
 
Debug.Print rs.Properties("Optimize") 
rs.Properties("Optimize") = True 
```

## <a name="built-in-property-behavior"></a><span data-ttu-id="02298-163">Comportement des propriétés intégrées</span><span class="sxs-lookup"><span data-stu-id="02298-163">Built-in Property Behavior</span></span>

<span data-ttu-id="02298-164">Le service de curseur pour OLE DB affecte également le comportement de certaines propriétés intégrées.</span><span class="sxs-lookup"><span data-stu-id="02298-164">The Cursor Service for OLE DB also affects the behavior of certain built-in properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="02298-165">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="02298-165">Property Name</span></span></p></th>
<th><p><span data-ttu-id="02298-166">Description</span><span class="sxs-lookup"><span data-stu-id="02298-166">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="02298-167"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="02298-167"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="02298-168">Complète les types de curseurs disponibles pour un <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="02298-168">Supplements the types of cursors that are available for a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02298-169"><a href="locktype-property-ado.md">LockType</a></span><span class="sxs-lookup"><span data-stu-id="02298-169"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="02298-170">Complète les types de verrous disponibles pour un <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="02298-170">Supplements the types of locks available for a <strong>Recordset</strong>.</span></span> <span data-ttu-id="02298-171">Permet la mise à jour en lot.</span><span class="sxs-lookup"><span data-stu-id="02298-171">Enables batch updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02298-172"><a href="sort-property-ado.md">Sort</a></span><span class="sxs-lookup"><span data-stu-id="02298-172"><a href="sort-property-ado.md">Sort</a></span></span></p></td>
<td><p><span data-ttu-id="02298-173">Indique le ou les noms de champ utilisés pour trier le <strong>Recordset</strong> ; indique également pour chaque champ si le tri doit s'effectuer dans l'ordre croissant ou dans l'ordre décroissant.</span><span class="sxs-lookup"><span data-stu-id="02298-173">Specifies one or more field names that the <strong>Recordset</strong> is sorted on, and whether each field is sorted in ascending or descending order.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="method-behavior"></a><span data-ttu-id="02298-174">Comportement des méthodes</span><span class="sxs-lookup"><span data-stu-id="02298-174">Method Behavior</span></span>

<span data-ttu-id="02298-175">Le service de curseur pour OLE DB active ou affecte le comportement de la méthode [Append](append-method-ado.md) de l’objet [Field](field-object-ado.md) et des méthodes [Open](open-method-ado-recordset.md), [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) et [Save](save-method-ado.md) de l’objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="02298-175">The Cursor Service for OLE DB enables or affects the behavior of the [Field](field-object-ado.md) object's [Append](append-method-ado.md) method; and the **Recordset** object's [Open](open-method-ado-recordset.md), [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), and [Save](save-method-ado.md) methods.</span></span>

