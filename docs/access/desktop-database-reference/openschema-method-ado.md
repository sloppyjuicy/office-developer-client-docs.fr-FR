---
title: OpenSchema, méthode (ADO)
TOCTitle: OpenSchema method (ADO)
ms:assetid: 57771163-a14e-207a-2942-849acb79a9a1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249294(v=office.15)
ms:contentKeyID: 48544970
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 846d1c0f73ba4a17f166fffc7c1bb4682ad31d49
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921165"
---
# <a name="openschema-method-ado"></a><span data-ttu-id="c57fe-102">OpenSchema, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="c57fe-102">OpenSchema method (ADO)</span></span>


<span data-ttu-id="c57fe-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c57fe-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="c57fe-104">Obtient du fournisseur les informations du schéma de base de données.</span><span class="sxs-lookup"><span data-stu-id="c57fe-104">Obtains database schema information from the provider .</span></span>

## <a name="syntax"></a><span data-ttu-id="c57fe-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c57fe-105">Syntax</span></span>

<span data-ttu-id="c57fe-106">**Définir \*\*\* recordset* = *connexion*. OpenSchema (* QueryType \*, *critères*, *IDSchéma doit être utilisé*)</span><span class="sxs-lookup"><span data-stu-id="c57fe-106">**Set\*\*\*recordset* = *connection*.OpenSchema (* QueryType\*, *Criteria*, *SchemaID*)</span></span>

## <a name="return-values"></a><span data-ttu-id="c57fe-107">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="c57fe-107">Return values</span></span>

<span data-ttu-id="c57fe-108">Retourne un objet [Recordset](recordset-object-ado.md) qui contient les informations de schéma.</span><span class="sxs-lookup"><span data-stu-id="c57fe-108">Returns a [Recordset](recordset-object-ado.md) object that contains schema information.</span></span> <span data-ttu-id="c57fe-109">L'objet **Recordset** est ouvert en tant que curseur statique, en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c57fe-109">The **Recordset** will be opened as a read-only, static cursor .</span></span> <span data-ttu-id="c57fe-110">Le *QueryType* détermine les colonnes qui apparaissent dans le **jeu d’enregistrements**.</span><span class="sxs-lookup"><span data-stu-id="c57fe-110">The *QueryType* determines what columns appear in the **Recordset**.</span></span>

## <a name="parameters"></a><span data-ttu-id="c57fe-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c57fe-111">Parameters</span></span>

  - <span data-ttu-id="c57fe-112">*QueryType*</span><span class="sxs-lookup"><span data-stu-id="c57fe-112">*QueryType*</span></span>

  - <span data-ttu-id="c57fe-113">Valeur [SchemaEnum](schemaenum.md) qui représente le type de requête de schéma à exécuter.</span><span class="sxs-lookup"><span data-stu-id="c57fe-113">Any [SchemaEnum](schemaenum.md) value that represents the type of schema query to run.</span></span>

  - <span data-ttu-id="c57fe-114">*Critères*</span><span class="sxs-lookup"><span data-stu-id="c57fe-114">*Criteria*</span></span>

  - <span data-ttu-id="c57fe-115">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="c57fe-115">Optional.</span></span> <span data-ttu-id="c57fe-116">Tableau de contraintes de requête pour chaque option *QueryType* , répertoriée dans **SchemaEnum**.</span><span class="sxs-lookup"><span data-stu-id="c57fe-116">An array of query constraints for each *QueryType* option, as listed in **SchemaEnum**.</span></span>

  - <span data-ttu-id="c57fe-117">*Si IDSchéma*</span><span class="sxs-lookup"><span data-stu-id="c57fe-117">*SchemaID*</span></span>

  - <span data-ttu-id="c57fe-118">GUID d'une requête d'un schéma de fournisseur non définie par la spécification OLE DB.</span><span class="sxs-lookup"><span data-stu-id="c57fe-118">The GUID for a provider-schema query not defined by the OLE DB specification.</span></span> <span data-ttu-id="c57fe-119">Ce paramètre est requis si *QueryType* a la valeur **adSchemaProviderSpecific**; dans le cas contraire, il n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="c57fe-119">This parameter is required if *QueryType* is set to **adSchemaProviderSpecific**; otherwise, it is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="c57fe-120">Notes</span><span class="sxs-lookup"><span data-stu-id="c57fe-120">Remarks</span></span>

<span data-ttu-id="c57fe-121">La méthode **OpenSchema** renvoie des informations autodescriptives sur la source de données, telles que les tables figurant dans la source de données, les colonnes des tables et les type de données pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c57fe-121">The **OpenSchema** method returns self-descriptive information about the data source, such as what tables are in the data source, the columns in the tables, and the data types supported.</span></span>

<span data-ttu-id="c57fe-122">L’argument *QueryType* est un GUID qui indique les colonnes (schémas) retournés.</span><span class="sxs-lookup"><span data-stu-id="c57fe-122">The *QueryType* argument is a GUID that indicates the columns (schemas) returned.</span></span> <span data-ttu-id="c57fe-123">La spécification OLE DB comporte une liste complète de schémas.</span><span class="sxs-lookup"><span data-stu-id="c57fe-123">The OLE DB specification has a full list of schemas.</span></span>

<span data-ttu-id="c57fe-p105">L'argument *Critères* limite les résultats d'une requête de schéma. *Critères* spécifie un tableau de valeurs qui doivent apparaître dans un sous-ensemble correspondant de colonnes, appelées *colonnes de contraintes* dans l'objet **Recordset** résultant.</span><span class="sxs-lookup"><span data-stu-id="c57fe-p105">The *Criteria* argument limits the results of a schema query. *Criteria* specifies an array of values that must occur in a corresponding subset of columns, called *constraint columns*, in the resulting **Recordset**.</span></span>

<span data-ttu-id="c57fe-126">La constante **adSchemaProviderSpecific** est utilisée pour l’argument *QueryType* si le fournisseur définit ses propres requêtes de schéma non standard en dehors de celles répertoriées ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="c57fe-126">The constant **adSchemaProviderSpecific** is used for the *QueryType* argument if the provider defines its own nonstandard schema queries outside those listed above.</span></span> <span data-ttu-id="c57fe-127">Lorsque cette constante est utilisée, l’argument *IDSchéma doit être utilisé* est requise pour transmettre le GUID de la requête de schéma à exécuter.</span><span class="sxs-lookup"><span data-stu-id="c57fe-127">When this constant is used, the *SchemaID* argument is required to pass the GUID of the schema query to execute.</span></span> <span data-ttu-id="c57fe-128">Si *QueryType* a la valeur **adSchemaProviderSpecific** mais *si IDSchéma* n’est pas spécifié, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="c57fe-128">If *QueryType* is set to **adSchemaProviderSpecific** but *SchemaID* is not provided, an error will result.</span></span>

<span data-ttu-id="c57fe-129">Les fournisseurs ne doivent pas obligatoirement prendre en charge toutes les requêtes de schéma standard OLE DB.</span><span class="sxs-lookup"><span data-stu-id="c57fe-129">Providers are not required to support all of the OLE DB standard schema queries.</span></span> <span data-ttu-id="c57fe-130">En fait, seules les requêtes **adSchemaTables**, **adSchemaColumns** et **adSchemaProviderTypes** sont requises par la spécification OLE DB.</span><span class="sxs-lookup"><span data-stu-id="c57fe-130">Specifically, only **adSchemaTables**, **adSchemaColumns**, and **adSchemaProviderTypes** are required by the OLE DB specification.</span></span> <span data-ttu-id="c57fe-131">Toutefois, le fournisseur n’est pas requis pour prendre en charge les contraintes de *critères* ci-dessus pour ces requêtes de schéma.</span><span class="sxs-lookup"><span data-stu-id="c57fe-131">However, the provider is not required to support the *Criteria* constraints listed above for those schema queries.</span></span>

<span data-ttu-id="c57fe-132">**L’utilisation du Service de données à distance** La méthode **OpenSchema** n’est pas disponible sur un objet de [connexion](connection-object-ado.md) côté client.</span><span class="sxs-lookup"><span data-stu-id="c57fe-132">**Remote Data Service Usage**The **OpenSchema** method is not available on a client-side [Connection](connection-object-ado.md) object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="c57fe-p108">Dans Visual Basic, les colonnes qui possèdent un entier non signé de quatre octets (DBTYPE UI4) dans l'objet <STRONG>Recordset</STRONG> retourné par la méthode <STRONG>OpenSchema</STRONG> de l'objet <STRONG>Connection</STRONG> ne peuvent pas être comparées à d'autres variables. Pour plus d'informations sur les types de données OLE DB, consultez le chapitre 13 et l'Annexe A du <EM>Guide de référence du programmeur Microsoft OLE DB</EM>.</span><span class="sxs-lookup"><span data-stu-id="c57fe-p108">In Visual Basic, columns that have a four-byte unsigned integer (DBTYPE UI4) in the <STRONG>Recordset</STRONG> returned from the <STRONG>OpenSchema</STRONG> method on the <STRONG>Connection</STRONG> object cannot be compared to other variables. For more information about OLE DB data types, see Chapter 13 and Appendix A of the <EM>Microsoft OLE DB Programmer's Reference</EM>.</span></span></P>


