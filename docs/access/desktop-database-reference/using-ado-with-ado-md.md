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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721936"
---
# <a name="using-ado-with-ado-md"></a><span data-ttu-id="0cf65-102">Utilisation d'ADO avec ADO MD</span><span class="sxs-lookup"><span data-stu-id="0cf65-102">Using ADO with ADO MD</span></span>


<span data-ttu-id="0cf65-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0cf65-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0cf65-p101">ADO et ADO MD sont des modèles d'objet apparentés mais distincts. ADO fournit des objets pour la connexion aux sources de données, l'exécution de commandes, la récupération de données tabulaires et de métadonnées de schéma sous forme de tableau et l'affichage des informations d'erreur du fournisseur. ADO MD fournit des objets pour l'extraction de données multidimensionnelles et l'affichage de métadonnées de schéma multidimensionnelles.</span><span class="sxs-lookup"><span data-stu-id="0cf65-p101">ADO and ADO MD are related but separate object models. ADO provides objects for connecting to data sources, executing commands, retrieving tabular data and schema metadata in a tabular format, and viewing provider error information. ADO MD provides objects for retrieving multidimensional data and viewing multidimensional schema metadata.</span></span>

<span data-ttu-id="0cf65-p102">Si vous travaillez avec un fournisseur de données multidimensionnelles (MDP), vous pouvez choisir d'utiliser ADO, ADO MD ou les deux avec votre application. En référençant les deux bibliothèques dans votre projet, vous aurez accès à toutes les fonctionnalités fournies par votre fournisseur MDP.</span><span class="sxs-lookup"><span data-stu-id="0cf65-p102">When working with an MDP you may choose to use ADO, ADO MD, or both with your application. By referencing both libraries within your project, you will have full access to the functionality provided by your MDP.</span></span>

<span data-ttu-id="0cf65-109">Il peut souvent s'avérer utile d'obtenir une vue tabulaire et bidimensionnelle d'un jeu de données multidimensionnel.</span><span class="sxs-lookup"><span data-stu-id="0cf65-109">It is often useful for consumers to get a flattened, tabular view of a multidimensional dataset.</span></span> <span data-ttu-id="0cf65-110">Pour cela, il vous suffit d'utiliser l'objet ADO [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="0cf65-110">You can do this by using the ADO [Recordset](recordset-object-ado.md) object.</span></span> <span data-ttu-id="0cf65-111">Spécifier la source pour votre [ensemble de cellules](cellset-object-ado-md.md) en tant que le paramètre ***Source*** de la méthode [Open](open-method-ado-recordset.md) d’un **objet Recordset**, plutôt que comme source d’un **ensemble de cellules**de ADO MD.</span><span class="sxs-lookup"><span data-stu-id="0cf65-111">Specify the source for your [Cellset](cellset-object-ado-md.md) as the ***Source*** parameter for the [Open](open-method-ado-recordset.md) method of a **Recordset**, rather than as the source for an ADO MD **Cellset**.</span></span>

<span data-ttu-id="0cf65-112">Il peut également s'avérer utile de voir les métadonnées de schéma sous la forme d'un tableau au lieu d'une hiérarchie d'objets.</span><span class="sxs-lookup"><span data-stu-id="0cf65-112">It may also be useful to view the schema metadata in a tabular view rather than as a hierarchy of objects.</span></span> <span data-ttu-id="0cf65-113">La méthode [OpenSchema](openschema-method-ado.md) ADO de l'objet [Connection](connection-object-ado.md) vous permet d'ouvrir un objet **Recordset** contenant des informations de schéma.</span><span class="sxs-lookup"><span data-stu-id="0cf65-113">The ADO [OpenSchema](openschema-method-ado.md) method on the [Connection](connection-object-ado.md) object allows the user to open a **Recordset** containing schema information.</span></span> <span data-ttu-id="0cf65-114">Le paramètre ***QueryType*** de la méthode **OpenSchema** comporte plusieurs valeurs [SchemaEnum](schemaenum.md) qui se rapportent aux fournisseurs MDP.</span><span class="sxs-lookup"><span data-stu-id="0cf65-114">The ***QueryType*** parameter of the **OpenSchema** method has several [SchemaEnum](schemaenum.md) values that relate specifically to MDPs.</span></span> <span data-ttu-id="0cf65-115">Il s'agit des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="0cf65-115">These values are:</span></span>

  - <span data-ttu-id="0cf65-116">**adSchemaCubes**</span><span class="sxs-lookup"><span data-stu-id="0cf65-116">**adSchemaCubes**</span></span>

  - <span data-ttu-id="0cf65-117">**adSchemaDimensions**</span><span class="sxs-lookup"><span data-stu-id="0cf65-117">**adSchemaDimensions**</span></span>

  - <span data-ttu-id="0cf65-118">**adSchemaHierarchies**</span><span class="sxs-lookup"><span data-stu-id="0cf65-118">**adSchemaHierarchies**</span></span>

  - <span data-ttu-id="0cf65-119">**adSchemaLevels**</span><span class="sxs-lookup"><span data-stu-id="0cf65-119">**adSchemaLevels**</span></span>

  - <span data-ttu-id="0cf65-120">**adSchemaMeasures**</span><span class="sxs-lookup"><span data-stu-id="0cf65-120">**adSchemaMeasures**</span></span>

  - <span data-ttu-id="0cf65-121">**adSchemaMembers**</span><span class="sxs-lookup"><span data-stu-id="0cf65-121">**adSchemaMembers**</span></span>

<span data-ttu-id="0cf65-p105">Pour utiliser les valeurs d'énumération ADO avec les propriétés ou méthodes ADO MD, votre projet doit référencer les deux bibliothèques, ADO et ADO MD. Par exemple, vous pouvez utiliser la valeur d'énumération **adState** ADO avec la propriété [State](state-property-ado-md.md) ADO MD. Pour plus d'informations sur la création de références à des bibliothèques, consultez la documentation de votre outil de développement.</span><span class="sxs-lookup"><span data-stu-id="0cf65-p105">To use ADO enum values with ADO MD properties or methods, your project must reference both the ADO and ADO MD libraries. For example, you can use the ADO **adState** enum values with the ADO MD [State](state-property-ado-md.md) property. For more information about establishing references to libraries, see the documentation of your development tool.</span></span>

<span data-ttu-id="0cf65-125">Pour plus d'informations sur les objets et méthodes ADO, consultez la rubrique [Référence des API ADO](ado-api-reference.md).</span><span class="sxs-lookup"><span data-stu-id="0cf65-125">For more information about the ADO objects and methods, see the [ADO API Reference](ado-api-reference.md).</span></span>

