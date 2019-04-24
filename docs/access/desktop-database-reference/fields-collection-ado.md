---
title: Fields, collection (ADO)
TOCTitle: Fields collection (ADO)
ms:assetid: 029aa738-8726-54a6-1813-b152813948bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248791(v=office.15)
ms:contentKeyID: 48542962
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a537756483361733c087d5dc1c6bba6e649d17d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292572"
---
# <a name="fields-collection-ado"></a><span data-ttu-id="28a54-102">Fields, collection (ADO)</span><span class="sxs-lookup"><span data-stu-id="28a54-102">Fields collection (ADO)</span></span>


<span data-ttu-id="28a54-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="28a54-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="28a54-104">Contient tous les objets [Field](field-object-ado.md) d’un objet [Recordset](recordset-object-ado.md) ou [Record](record-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="28a54-104">Contains all the [Field](field-object-ado.md) objects of a [Recordset](recordset-object-ado.md) or [Record](record-object-ado.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="28a54-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="28a54-105">Remarks</span></span>

<span data-ttu-id="28a54-p101">Un objet **Recordset** possède une collection **Fields** composée d'objets **Field**. Chaque objet **Field** correspond à une colonne du **Recordset**. Vous pouvez remplir la collection **Fields** avant d'ouvrir l'objet **Recordset** en appelant la méthode [Refresh](refresh-method-ado.md) sur cette collection.</span><span class="sxs-lookup"><span data-stu-id="28a54-p101">A **Recordset** object has a **Fields** collection made up of **Field** objects. Each **Field** object corresponds to a column in the **Recordset**. You can populate the **Fields** collection before opening the **Recordset** by calling the [Refresh](refresh-method-ado.md) method on the collection.</span></span>

> [!NOTE]
> <span data-ttu-id="28a54-109">[!REMARQUE] Pour plus d'informations sur l'utilisation des objets **Field**, voir la rubrique traitant de l'objet **Field**.</span><span class="sxs-lookup"><span data-stu-id="28a54-109">See the **Field** object topic for a more detailed explanation of how to use **Field** objects.</span></span>

<span data-ttu-id="28a54-110">La collection **Fields** possède une méthode [Append](append-method-ado.md), qui crée et ajoute provisoirement un objet **Field** à la collection, ainsi qu'une méthode **Update**, qui finalise les ajouts et les suppressions.</span><span class="sxs-lookup"><span data-stu-id="28a54-110">The **Fields** collection has an [Append](append-method-ado.md) method, which provisionally creates and adds a **Field** object to the collection, and an **Update** method, which finalizes any additions or deletions.</span></span>

<span data-ttu-id="28a54-p102">Un objet **Record** possède deux champs spéciaux qui peuvent être indexés avec des constantes [FieldEnum](fieldenum.md). Une constante donnée accède à un champ contenant le flux par défaut de l' **enregistrement**, une autre accède à un champ contenant la chaîne URL absolue de l' **enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="28a54-p102">A **Record** object has two special fields that can be indexed with [FieldEnum](fieldenum.md) constants. One constant accesses a field containing the default stream for the **Record**, and the other accesses a field containing the absolute URL string for the **Record**.</span></span>

<span data-ttu-id="28a54-p103">Certains fournisseurs (par exemple, [Fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md)) peuvent remplir la collection **Fields** avec un sous-ensemble de champs disponibles pour l'objet **Record** ou **Recordset**. D'autres champs ne seront pas ajoutés à la collection tant qu'ils n'auront pas été référencés par leur nom ou indexés par votre code.</span><span class="sxs-lookup"><span data-stu-id="28a54-p103">Certain providers (for example, the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)) may populate the **Fields** collection with a subset of available fields for the **Record** or **Recordset**. Other fields will not be added to the collection until they are first referenced by name or indexed by your code.</span></span>

<span data-ttu-id="28a54-p104">Si vous essayez de référencer un champ inexistant par son nom, un nouvel objet **Field** sera ajouté à la collection **Fields** avec une propriété [Status](status-property-ado-field.md) définie sur **adFieldPendingInsert**. Lorsque vous appelez [Update](update-method-ado.md), ADO crée un nouveau champ dans votre source de données si cela est autorisé par votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="28a54-p104">If you attempt to reference a nonexistent field by name, a new **Field** object will be appended to the **Fields** collection with a [Status](status-property-ado-field.md) of **adFieldPendingInsert**. When you call [Update](update-method-ado.md), ADO will create a new field in your data source if allowed by your provider.</span></span>

