---
title: Utilisation d'ADO avec ADO MD
TOCTitle: Using ADO with ADO MD
ms:assetid: 93d1d270-b8d0-4489-d441-11a61887291c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249655(v=office.15)
ms:contentKeyID: 48546405
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 80c87f57a96f98de704e3cfa9b7689a522e4a7af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312746"
---
# <a name="using-ado-with-ado-md"></a><span data-ttu-id="46b6b-102">Utilisation d’ADO avec ADO MD</span><span class="sxs-lookup"><span data-stu-id="46b6b-102">Using ADO with ADO MD</span></span>


<span data-ttu-id="46b6b-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="46b6b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="46b6b-p101">ADO et ADO MD sont des modèles d'objet apparentés mais distincts. ADO fournit des objets pour la connexion aux sources de données, l'exécution de commandes, la récupération de données tabulaires et de métadonnées de schéma sous forme de tableau et l'affichage des informations d'erreur du fournisseur. ADO MD fournit des objets pour l'extraction de données multidimensionnelles et l'affichage de métadonnées de schéma multidimensionnelles.</span><span class="sxs-lookup"><span data-stu-id="46b6b-p101">ADO and ADO MD are related but separate object models. ADO provides objects for connecting to data sources, executing commands, retrieving tabular data and schema metadata in a tabular format, and viewing provider error information. ADO MD provides objects for retrieving multidimensional data and viewing multidimensional schema metadata.</span></span>

<span data-ttu-id="46b6b-p102">Si vous travaillez avec un fournisseur de données multidimensionnelles (MDP), vous pouvez choisir d'utiliser ADO, ADO MD ou les deux avec votre application. En référençant les deux bibliothèques dans votre projet, vous aurez accès à toutes les fonctionnalités fournies par votre fournisseur MDP.</span><span class="sxs-lookup"><span data-stu-id="46b6b-p102">When working with an MDP you may choose to use ADO, ADO MD, or both with your application. By referencing both libraries within your project, you will have full access to the functionality provided by your MDP.</span></span>

<span data-ttu-id="46b6b-p103">Il peut souvent s’avérer utile d’obtenir une vue tabulaire et bidimensionnelle d’un jeu de données multidimensionnel. Pour cela, il vous suffit d’utiliser l’objet ADO [Recordset](recordset-object-ado.md). Spécifiez la source de votre objet [Cellset](cellset-object-ado-md.md) comme paramètre ***Source*** de la méthode [Open](open-method-ado-recordset.md) d’un objet **Recordset**, et non comme source d’un objet **Cellset** ADO MD.</span><span class="sxs-lookup"><span data-stu-id="46b6b-p103">It is often useful for consumers to get a flattened, tabular view of a multidimensional dataset. You can do this by using the ADO [Recordset](recordset-object-ado.md) object. Specify the source for your [Cellset](cellset-object-ado-md.md) as the ***Source*** parameter for the [Open](open-method-ado-recordset.md) method of a **Recordset**, rather than as the source for an ADO MD **Cellset**.</span></span>

<span data-ttu-id="46b6b-p104">Il peut également s’avérer utile de voir les métadonnées de schéma sous la forme d’un tableau au lieu d’une hiérarchie d’objets. La méthode [OpenSchema](openschema-method-ado.md) ADO de l’objet [Connection](connection-object-ado.md) vous permet d’ouvrir un objet **Recordset** contenant des informations de schéma. Le paramètre ***QueryType*** de la méthode **OpenSchema** comporte plusieurs valeurs [SchemaEnum](schemaenum.md) qui se rapportent aux fournisseurs MDP. Il s’agit des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="46b6b-p104">It may also be useful to view the schema metadata in a tabular view rather than as a hierarchy of objects. The ADO [OpenSchema](openschema-method-ado.md) method on the [Connection](connection-object-ado.md) object allows the user to open a **Recordset** containing schema information. The ***QueryType*** parameter of the **OpenSchema** method has several [SchemaEnum](schemaenum.md) values that relate specifically to MDPs. These values are:</span></span>

  - <span data-ttu-id="46b6b-116">**adSchemaCubes**</span><span class="sxs-lookup"><span data-stu-id="46b6b-116">**adSchemaCubes**</span></span>

  - <span data-ttu-id="46b6b-117">**adSchemaDimensions**</span><span class="sxs-lookup"><span data-stu-id="46b6b-117">**adSchemaDimensions**</span></span>

  - <span data-ttu-id="46b6b-118">**adSchemaHierarchies**</span><span class="sxs-lookup"><span data-stu-id="46b6b-118">**adSchemaHierarchies**</span></span>

  - <span data-ttu-id="46b6b-119">**adSchemaLevels**</span><span class="sxs-lookup"><span data-stu-id="46b6b-119">**adSchemaLevels**</span></span>

  - <span data-ttu-id="46b6b-120">**adSchemaMeasures**</span><span class="sxs-lookup"><span data-stu-id="46b6b-120">**adSchemaMeasures**</span></span>

  - <span data-ttu-id="46b6b-121">**adSchemaMembers**</span><span class="sxs-lookup"><span data-stu-id="46b6b-121">**adSchemaMembers**</span></span>

<span data-ttu-id="46b6b-p105">Pour utiliser les valeurs d'énumération ADO avec les propriétés ou méthodes ADO MD, votre projet doit référencer les deux bibliothèques, ADO et ADO MD. Par exemple, vous pouvez utiliser la valeur d'énumération **adState** ADO avec la propriété [State](state-property-ado-md.md) ADO MD. Pour plus d'informations sur la création de références à des bibliothèques, consultez la documentation de votre outil de développement.</span><span class="sxs-lookup"><span data-stu-id="46b6b-p105">To use ADO enum values with ADO MD properties or methods, your project must reference both the ADO and ADO MD libraries. For example, you can use the ADO **adState** enum values with the ADO MD [State](state-property-ado-md.md) property. For more information about establishing references to libraries, see the documentation of your development tool.</span></span>

<span data-ttu-id="46b6b-125">Pour plus d'informations sur les objets et méthodes ADO, consultez la rubrique [Référence des API ADO](ado-api-reference.md).</span><span class="sxs-lookup"><span data-stu-id="46b6b-125">For more information about the ADO objects and methods, see the [ADO API Reference](ado-api-reference.md).</span></span>

