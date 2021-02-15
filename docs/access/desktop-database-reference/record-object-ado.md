---
title: Record, objet (ADO)
TOCTitle: Record object (ADO)
ms:assetid: 817aaf13-78d4-1134-aa94-997e92077c22
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249557(v=office.15)
ms:contentKeyID: 48545952
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 96ddc7fc1a93543f0eea2b42a3d423ec25a00636
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300902"
---
# <a name="record-object-ado"></a><span data-ttu-id="cda74-102">Record, objet (ADO)</span><span class="sxs-lookup"><span data-stu-id="cda74-102">Record object (ADO)</span></span>


<span data-ttu-id="cda74-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cda74-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cda74-104">Représente une ligne d’un [Recordset](recordset-object-ado.md) ou du fournisseur de données, ou un objet renvoyé par un fournisseur de données semi-structurées, comme un fichier ou un répertoire.</span><span class="sxs-lookup"><span data-stu-id="cda74-104">Represents a row from a [Recordset](recordset-object-ado.md) or the data provider, or an object returned by a semi-structured data provider, such as a file or directory.</span></span>

## <a name="remarks"></a><span data-ttu-id="cda74-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="cda74-105">Remarks</span></span>

<span data-ttu-id="cda74-p101">Un objet **Record** représente une ligne de données et partage des similarités de concept avec un **Recordset** monoligne. Selon les fonctionnalités offertes par le fournisseur, les objets **Record** peuvent être renvoyés directement par le fournisseur pour générer un **Recordset** à une seule ligne, par exemple lorsqu'une requête SQL ne sélectionnant qu'une ligne est exécutée. Il en est de même d'un objet **Record** qui peut être obtenu directement à partir d'un objet **Recordset**. Un **Record** peut aussi être renvoyé directement depuis un fournisseur pour fournir des données semi-structurées, comme c'est le cas avec le fournisseur Microsoft Exchange OLE DB.</span><span class="sxs-lookup"><span data-stu-id="cda74-p101">A **Record** object represents one row of data, and has some conceptual similarities with a one-row **Recordset**. Depending upon the capabilities of your provider, **Record** objects may be returned directly from your provider instead of a one-row **Recordset**, for example when an SQL query that selects only one row is executed. Or, a **Record** object can be obtained directly from a **Recordset** object. Or, a **Record** can be returned directly from a provider to semi-structured data, such as the Microsoft Exchange OLE DB provider.</span></span>

<span data-ttu-id="cda74-p102">Vous pouvez afficher les champs associés à l'objet **Record** par l'intermédiaire de la collection [Fields](fields-collection-ado.md) de l'objet **Record**. 8373ADO accepte l'emploi de colonnes dont les valeurs sont des objets, notamment **Recordset** ou **SafeArray** ou des valeurs scalaires, dans la collection **Fields** des objets **Record**.</span><span class="sxs-lookup"><span data-stu-id="cda74-p102">You can view the fields associated with the **Record** object by way of the [Fields](fields-collection-ado.md) collection on the **Record** object. ADO allows object-valued columns including **Recordset**, **SafeArray**, and scalar values in the **Fields** collection of **Record** objects.</span></span>

<span data-ttu-id="cda74-112">Si l'objet **Record** représente une ligne dans un **Recordset**, il est alors possible de revenir à ce **Recordset** d'origine avec la propriété [Source](source-property-ado-record.md).</span><span class="sxs-lookup"><span data-stu-id="cda74-112">If the **Record** object represents a row in a **Recordset**, then it is possible to return to that original **Recordset** with the [Source](source-property-ado-record.md) property.</span></span>

<span data-ttu-id="cda74-p103">L'objet **Record** peut également être utilisé par des fournisseurs de données semi-structurées comme [Fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md), pour modéliser des espaces de noms hiérarchiques. Chaque nœud de l'arborescence est un objet **Record** avec ses colonnes associées. Ces colonnes peuvent représenter les attributs de ce nœud et d'autres informations pertinentes. L'objet **Record** peut représenter un nœud feuille et un nœud branche dans l'arborescence. Les nœuds branche possèdent d'autres nœuds comme contenu, contrairement aux nœuds feuille. Ces derniers contiennent en général des flux binaires de données alors que les nœuds branche peuvent être associés à un flux binaire par défaut. Les propriétés de l'objet **Record** identifient le type de nœud.</span><span class="sxs-lookup"><span data-stu-id="cda74-p103">The **Record** object can also be used by semi-structured data providers such as the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md), to model tree-structured namespaces. Each node in the tree is a **Record** object with associated columns. The columns can represent the attributes of that node and other relevant information. The **Record** object can represent both a leaf node and a non-leaf node in the tree structure. Non-leaf nodes have other nodes as their contents while leaf nodes do not have such contents. Leaf nodes typically contain binary streams of data while non-leaf nodes may also have a default binary stream associated with them. Properties on the **Record** object identify the type of node.</span></span>

<span data-ttu-id="cda74-p104">L'objet **Record** peut aussi servir à naviguer dans des données organisées de manière hiérarchique. Un objet **Record** peut être créé pour représenter la racine d'une sous-arborescence spécifique dans une arborescence plus large, de nouveaux objets **Record** pouvant être ouverts pour représenter des nœuds enfants.</span><span class="sxs-lookup"><span data-stu-id="cda74-p104">The **Record** object also represents an alternative way for navigating hierarchically organized data. A **Record** object may be created to represent the root of a specific sub-tree in a large tree structure and new **Record** objects may be opened to represent child nodes.</span></span>

<span data-ttu-id="cda74-p105">Une ressource (par exemple, un fichier ou un répertoire) peut être identifiée de manière unique par une URL absolue. Un objet [Connection](connection-object-ado.md) est créé de manière implicite et défini sur l’objet **Record** quand cet objet **Record** est ouvert avec une URL absolue. Un objet **Connection** peut être défini de manière explicite sur l’objet **Record** via la propriété [ActiveConnection](activeconnection-property-ado.md). Les fichiers et répertoires accessibles via l’objet **Connection** définissent le *contexte* dans lequel des opérations **Record** peuvent se produire.</span><span class="sxs-lookup"><span data-stu-id="cda74-p105">A resource (for example, a file or directory) can be uniquely identified by an absolute URL. A [Connection](connection-object-ado.md) object is implicitly created and set to the **Record** object when the **Record** is opened with an absolute URL. A **Connection** object may explicitly be set to the **Record** object via the [ActiveConnection](activeconnection-property-ado.md) property. The files and directories accessible via the **Connection** object define the *context* in which **Record** operations may occur.</span></span>

<span data-ttu-id="cda74-126">Les méthodes de navigation et de modification des données portant sur l'objet **Record** acceptent également les URL relatives, qui localisent une ressource à l'aide d'une URL absolue ou du contexte de l'objet **Connection** comme point de départ.</span><span class="sxs-lookup"><span data-stu-id="cda74-126">Data modification and navigation methods on the **Record** object also accept a relative URL, which locates a resource using an absolute URL or the **Connection** object context as a starting point.</span></span>

> [!NOTE]
> <span data-ttu-id="cda74-127">[!REMARQUE] Les URL qui utilisent le modèle http appellent automatiquement [Fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="cda74-127">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="cda74-128">Pour plus d’informations, voir [URL absolues et relatives.](absolute-and-relative-urls.md)</span><span class="sxs-lookup"><span data-stu-id="cda74-128">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>



<span data-ttu-id="cda74-p107">Un objet **Connection** est associé à chaque objet **Record**. Par conséquent, les opérations sur les objets **Record** peuvent faire partie d'une transaction faisant appel aux méthodes de transaction des objets **Connection**.</span><span class="sxs-lookup"><span data-stu-id="cda74-p107">A **Connection** object is associated with each **Record** object. Therefore, **Record** object operations can be part of a transaction by invoking **Connection** object transaction methods.</span></span>

<span data-ttu-id="cda74-131">L'objet **Record** ne prend pas en charge les événements ADO et ne peut donc répondre aux notifications.</span><span class="sxs-lookup"><span data-stu-id="cda74-131">The **Record** object does not support ADO events, and therefore will not respond to notifications.</span></span>

<span data-ttu-id="cda74-132">Les méthodes et les propriétés d'un objet **Record** vous permettent d'effectuer diverses tâches :</span><span class="sxs-lookup"><span data-stu-id="cda74-132">With the methods and properties of a **Record** object, you can do the following:</span></span>

  - <span data-ttu-id="cda74-133">définir ou renvoyer l'objet **Connection** associé à l'aide de la propriété [ActiveConnection](activeconnection-property-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="cda74-133">Set or return the associated **Connection** object with the [ActiveConnection](activeconnection-property-ado.md) property.</span></span>

  - <span data-ttu-id="cda74-134">indiquer les autorisations d'accès à l'aide de la propriété [Mode](mode-property-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="cda74-134">Indicate access permissions with the [Mode](mode-property-ado.md) property.</span></span>

  - <span data-ttu-id="cda74-135">renvoyer l'URL du répertoire qui (le cas échéant) contient la ressource représentée par l'objet **Record**, à l'aide de la propriété [ParentURL](parenturl-property-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="cda74-135">Return the URL of the directory, if any, that contains the resource represented by the **Record** with the [ParentURL](parenturl-property-ado.md) property.</span></span>

  - <span data-ttu-id="cda74-136">indiquer l'URL absolue, l'URL relative ou l'objet **Recordset** dont provient l'objet **Record** au moyen de la propriété [Source](source-property-ado-record.md) ;</span><span class="sxs-lookup"><span data-stu-id="cda74-136">Indicate the absolute URL, relative URL, or **Recordset** from which the **Record** is derived with the [Source](source-property-ado-record.md) property.</span></span>

  - <span data-ttu-id="cda74-137">indiquer l’état actuel de l’objet **Record** à l’aide de la propriété [State](state-property-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="cda74-137">Indicate the current status of the **Record** with the [State](state-property-ado.md) property.</span></span>

  - <span data-ttu-id="cda74-138">indiquer le type d’objet **Record** (*simple*, *collection* ou *document structuré*) à l’aide de la propriété [RecordType](recordtype-property-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="cda74-138">Indicate the type of **Record** — *simple*, *collection*, or *structured document* — with the [RecordType](recordtype-property-ado.md) property.</span></span>

  - <span data-ttu-id="cda74-139">arrêter l’exécution d’une opération asynchrone à l’aide de la méthode [Cancel](cancel-method-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="cda74-139">Halt execution of an asynchronous operation with the [Cancel](cancel-method-ado.md) method.</span></span>

  - <span data-ttu-id="cda74-140">dissocier l'objet **Record** d'une source de données à l'aide de la méthode [Close](close-method-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="cda74-140">Disassociate the **Record** from a data source with the [Close](close-method-ado.md) method.</span></span>

  - <span data-ttu-id="cda74-141">copier le fichier ou le répertoire représenté par un objet **Record** dans un autre emplacement à l'aide de la méthode [CopyRecord](copyrecord-method-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="cda74-141">Copy the file or directory represented by a **Record** to another location with the [CopyRecord](copyrecord-method-ado.md) method.</span></span>

  - <span data-ttu-id="cda74-142">supprimer le fichier, ou le répertoire et ses sous-répertoires, représenté par un objet **Record**, à l'aide de la méthode [DeleteRecord](deleterecord-method-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="cda74-142">Delete the file, or directory and subdirectories, represented by a **Record** with the [DeleteRecord](deleterecord-method-ado.md) method.</span></span>

  - <span data-ttu-id="cda74-143">ouvrir un **Recordset** contenant des lignes qui représentent les sous-répertoires et les fichiers de l'entité représentée par l'objet **Record**, à l'aide de la méthode [GetChildren](getchildren-method-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="cda74-143">Open a **Recordset** containing rows that represent the subdirectories and files of the entity represented by the **Record** with the [GetChildren](getchildren-method-ado.md) method.</span></span>

  - <span data-ttu-id="cda74-144">déplacer (renommer) le fichier, ou le répertoire et ses sous-répertoires, représenté par l'objet **Record** vers un autre emplacement, à l'aide de la méthode [MoveRecord](moverecord-method-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="cda74-144">Move (rename) the file, or directory and subdirectories, represented by a **Record** to another location with the [MoveRecord](moverecord-method-ado.md) method.</span></span>

  - <span data-ttu-id="cda74-145">associer l'objet **Record** à une source de données existante, ou créer un nouveau fichier ou répertoire, à l'aide de la méthode [Open](open-method-ado-record.md).</span><span class="sxs-lookup"><span data-stu-id="cda74-145">Associate the **Record** with an existing data source, or create a new file or directory with the [Open](open-method-ado-record.md) method.</span></span>

