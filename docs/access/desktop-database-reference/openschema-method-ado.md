---
title: OpenSchema, méthode (ADO)
TOCTitle: OpenSchema Method (ADO)
ms:assetid: 57771163-a14e-207a-2942-849acb79a9a1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249294(v=office.15)
ms:contentKeyID: 48544970
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ddd823baf153ebc78fc34ca838184f415edd29ef
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605918"
---
# <a name="openschema-method-ado"></a><span data-ttu-id="493f0-102">OpenSchema, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="493f0-102">OpenSchema Method (ADO)</span></span>


<span data-ttu-id="493f0-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="493f0-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="493f0-104">Obtient du fournisseur les informations du schéma de base de données.</span><span class="sxs-lookup"><span data-stu-id="493f0-104">Obtains database schema information from the provider .</span></span>

## <a name="syntax"></a><span data-ttu-id="493f0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="493f0-105">Syntax</span></span>

<span data-ttu-id="493f0-106">**Définir \*\*\* recordset* = *connexion*. OpenSchema (* QueryType \*, *critères*, *IDSchéma doit être utilisé*)</span><span class="sxs-lookup"><span data-stu-id="493f0-106">**Set\*\*\*recordset* = *connection*.OpenSchema (* QueryType\*, *Criteria*, *SchemaID*)</span></span>

<span data-ttu-id="493f0-107"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="493f0-107"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="493f0-108">Valeurs renvoyées</span><span class="sxs-lookup"><span data-stu-id="493f0-108">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="493f0-109">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="493f0-109">Return values</span></span>
>>>>>>> <span data-ttu-id="493f0-110">master</span><span class="sxs-lookup"><span data-stu-id="493f0-110">master</span></span>

<span data-ttu-id="493f0-111">Retourne un objet [Recordset](recordset-object-ado.md) qui contient les informations de schéma.</span><span class="sxs-lookup"><span data-stu-id="493f0-111">Returns a [Recordset](recordset-object-ado.md) object that contains schema information.</span></span> <span data-ttu-id="493f0-112">L'objet **Recordset** est ouvert en tant que curseur statique, en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="493f0-112">The **Recordset** will be opened as a read-only, static cursor .</span></span> <span data-ttu-id="493f0-113">Le *QueryType* détermine les colonnes qui apparaissent dans le **jeu d’enregistrements**.</span><span class="sxs-lookup"><span data-stu-id="493f0-113">The *QueryType* determines what columns appear in the **Recordset**.</span></span>

## <a name="parameters"></a><span data-ttu-id="493f0-114">Paramètres</span><span class="sxs-lookup"><span data-stu-id="493f0-114">Parameters</span></span>

  - <span data-ttu-id="493f0-115">*QueryType*</span><span class="sxs-lookup"><span data-stu-id="493f0-115">*QueryType*</span></span>

  - <span data-ttu-id="493f0-116">Valeur [SchemaEnum](schemaenum.md) qui représente le type de requête de schéma à exécuter.</span><span class="sxs-lookup"><span data-stu-id="493f0-116">Any [SchemaEnum](schemaenum.md) value that represents the type of schema query to run.</span></span>

  - <span data-ttu-id="493f0-117">*Critères*</span><span class="sxs-lookup"><span data-stu-id="493f0-117">*Criteria*</span></span>

  - <span data-ttu-id="493f0-118">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="493f0-118">Optional.</span></span> <span data-ttu-id="493f0-119">Tableau de contraintes de requête pour chaque option *QueryType* , répertoriée dans **SchemaEnum**.</span><span class="sxs-lookup"><span data-stu-id="493f0-119">An array of query constraints for each *QueryType* option, as listed in **SchemaEnum**.</span></span>

  - <span data-ttu-id="493f0-120">*Si IDSchéma*</span><span class="sxs-lookup"><span data-stu-id="493f0-120">*SchemaID*</span></span>

  - <span data-ttu-id="493f0-121">GUID d'une requête d'un schéma de fournisseur non définie par la spécification OLE DB.</span><span class="sxs-lookup"><span data-stu-id="493f0-121">The GUID for a provider-schema query not defined by the OLE DB specification.</span></span> <span data-ttu-id="493f0-122">Ce paramètre est requis si *QueryType* a la valeur **adSchemaProviderSpecific**; dans le cas contraire, il n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="493f0-122">This parameter is required if *QueryType* is set to **adSchemaProviderSpecific**; otherwise, it is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="493f0-123">Notes</span><span class="sxs-lookup"><span data-stu-id="493f0-123">Remarks</span></span>

<span data-ttu-id="493f0-124">La méthode **OpenSchema** renvoie des informations autodescriptives sur la source de données, telles que les tables figurant dans la source de données, les colonnes des tables et les type de données pris en charge.</span><span class="sxs-lookup"><span data-stu-id="493f0-124">The **OpenSchema** method returns self-descriptive information about the data source, such as what tables are in the data source, the columns in the tables, and the data types supported.</span></span>

<span data-ttu-id="493f0-125">L’argument *QueryType* est un GUID qui indique les colonnes (schémas) retournés.</span><span class="sxs-lookup"><span data-stu-id="493f0-125">The *QueryType* argument is a GUID that indicates the columns (schemas) returned.</span></span> <span data-ttu-id="493f0-126">La spécification OLE DB comporte une liste complète de schémas.</span><span class="sxs-lookup"><span data-stu-id="493f0-126">The OLE DB specification has a full list of schemas.</span></span>

<span data-ttu-id="493f0-p105">L'argument *Critères* limite les résultats d'une requête de schéma. *Critères* spécifie un tableau de valeurs qui doivent apparaître dans un sous-ensemble correspondant de colonnes, appelées *colonnes de contraintes* dans l'objet **Recordset** résultant.</span><span class="sxs-lookup"><span data-stu-id="493f0-p105">The *Criteria* argument limits the results of a schema query. *Criteria* specifies an array of values that must occur in a corresponding subset of columns, called *constraint columns*, in the resulting **Recordset**.</span></span>

<span data-ttu-id="493f0-129">La constante **adSchemaProviderSpecific** est utilisée pour l’argument *QueryType* si le fournisseur définit ses propres requêtes de schéma non standard en dehors de celles répertoriées ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="493f0-129">The constant **adSchemaProviderSpecific** is used for the *QueryType* argument if the provider defines its own nonstandard schema queries outside those listed above.</span></span> <span data-ttu-id="493f0-130">Lorsque cette constante est utilisée, l’argument *IDSchéma doit être utilisé* est requise pour transmettre le GUID de la requête de schéma à exécuter.</span><span class="sxs-lookup"><span data-stu-id="493f0-130">When this constant is used, the *SchemaID* argument is required to pass the GUID of the schema query to execute.</span></span> <span data-ttu-id="493f0-131">Si *QueryType* a la valeur **adSchemaProviderSpecific** mais *si IDSchéma* n’est pas spécifié, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="493f0-131">If *QueryType* is set to **adSchemaProviderSpecific** but *SchemaID* is not provided, an error will result.</span></span>

<span data-ttu-id="493f0-132">Les fournisseurs ne doivent pas obligatoirement prendre en charge toutes les requêtes de schéma standard OLE DB.</span><span class="sxs-lookup"><span data-stu-id="493f0-132">Providers are not required to support all of the OLE DB standard schema queries.</span></span> <span data-ttu-id="493f0-133">En fait, seules les requêtes **adSchemaTables**, **adSchemaColumns** et **adSchemaProviderTypes** sont requises par la spécification OLE DB.</span><span class="sxs-lookup"><span data-stu-id="493f0-133">Specifically, only **adSchemaTables**, **adSchemaColumns**, and **adSchemaProviderTypes** are required by the OLE DB specification.</span></span> <span data-ttu-id="493f0-134">Toutefois, le fournisseur n’est pas requis pour prendre en charge les contraintes de *critères* ci-dessus pour ces requêtes de schéma.</span><span class="sxs-lookup"><span data-stu-id="493f0-134">However, the provider is not required to support the *Criteria* constraints listed above for those schema queries.</span></span>

<span data-ttu-id="493f0-135">**L’utilisation du Service de données à distance** La méthode **OpenSchema** n’est pas disponible sur un objet de [connexion](connection-object-ado.md) côté client.</span><span class="sxs-lookup"><span data-stu-id="493f0-135">**Remote Data Service Usage**The **OpenSchema** method is not available on a client-side [Connection](connection-object-ado.md) object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="493f0-p108">Dans Visual Basic, les colonnes qui possèdent un entier non signé de quatre octets (DBTYPE UI4) dans l'objet <STRONG>Recordset</STRONG> retourné par la méthode <STRONG>OpenSchema</STRONG> de l'objet <STRONG>Connection</STRONG> ne peuvent pas être comparées à d'autres variables. Pour plus d'informations sur les types de données OLE DB, consultez le chapitre 13 et l'Annexe A du <EM>Guide de référence du programmeur Microsoft OLE DB</EM>.</span><span class="sxs-lookup"><span data-stu-id="493f0-p108">In Visual Basic, columns that have a four-byte unsigned integer (DBTYPE UI4) in the <STRONG>Recordset</STRONG> returned from the <STRONG>OpenSchema</STRONG> method on the <STRONG>Connection</STRONG> object cannot be compared to other variables. For more information about OLE DB data types, see Chapter 13 and Appendix A of the <EM>Microsoft OLE DB Programmer's Reference</EM>.</span></span></P>


