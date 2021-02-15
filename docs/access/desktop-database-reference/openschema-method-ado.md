---
title: OpenSchema, méthode (ADO)
TOCTitle: OpenSchema method (ADO)
ms:assetid: 57771163-a14e-207a-2942-849acb79a9a1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249294(v=office.15)
ms:contentKeyID: 48544970
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 43ca69b9d761629d42138780517f8de806ed7e8c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288335"
---
# <a name="openschema-method-ado"></a><span data-ttu-id="6a97f-102">OpenSchema, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="6a97f-102">OpenSchema method (ADO)</span></span>

<span data-ttu-id="6a97f-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6a97f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6a97f-104">Obtient du fournisseur les informations du schéma de base de données.</span><span class="sxs-lookup"><span data-stu-id="6a97f-104">Obtains database schema information from the provider .</span></span>

## <a name="syntax"></a><span data-ttu-id="6a97f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a97f-105">Syntax</span></span>

<span data-ttu-id="6a97f-106">**Jeu d’enregistrements*  =  Set*\*\* *.* OpenSchema (\* QueryType\*, *Criteria*, *SchemaID*)</span><span class="sxs-lookup"><span data-stu-id="6a97f-106">**Set\*\*\*recordset* = *connection*.OpenSchema (* QueryType\*, *Criteria*, *SchemaID*)</span></span>

## <a name="return-values"></a><span data-ttu-id="6a97f-107">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="6a97f-107">Return values</span></span>

<span data-ttu-id="6a97f-108">Retourne un objet [Recordset](recordset-object-ado.md) qui contient les informations de schéma.</span><span class="sxs-lookup"><span data-stu-id="6a97f-108">Returns a [Recordset](recordset-object-ado.md) object that contains schema information.</span></span> <span data-ttu-id="6a97f-109">L'objet **Recordset** est ouvert en tant que curseur statique, en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="6a97f-109">The **Recordset** will be opened as a read-only, static cursor .</span></span> <span data-ttu-id="6a97f-110">Le paramètre *TypeRequête* détermine les colonnes qui apparaîtront dans l’objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="6a97f-110">The *QueryType* determines what columns appear in the **Recordset**.</span></span>

## <a name="parameters"></a><span data-ttu-id="6a97f-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6a97f-111">Parameters</span></span>

|<span data-ttu-id="6a97f-112">Paramètre</span><span class="sxs-lookup"><span data-stu-id="6a97f-112">Parameter</span></span>|<span data-ttu-id="6a97f-113">Description</span><span class="sxs-lookup"><span data-stu-id="6a97f-113">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="6a97f-114">*QueryType*</span><span class="sxs-lookup"><span data-stu-id="6a97f-114">*QueryType*</span></span> |<span data-ttu-id="6a97f-115">Valeur [SchemaEnum](schemaenum.md) qui représente le type de requête de schéma à exécuter.</span><span class="sxs-lookup"><span data-stu-id="6a97f-115">Any [SchemaEnum](schemaenum.md) value that represents the type of schema query to run.</span></span>|
|<span data-ttu-id="6a97f-116">*Critères*</span><span class="sxs-lookup"><span data-stu-id="6a97f-116">*Criteria*</span></span> |<span data-ttu-id="6a97f-117">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="6a97f-117">Optional.</span></span> <span data-ttu-id="6a97f-118">Tableau de contraintes de requête pour chaque option *TypeRequête*, répertoriée dans **SchemaEnum**.</span><span class="sxs-lookup"><span data-stu-id="6a97f-118">An array of query constraints for each *QueryType* option, as listed in **SchemaEnum**.</span></span>|
|<span data-ttu-id="6a97f-119">*SchemaID*</span><span class="sxs-lookup"><span data-stu-id="6a97f-119">*SchemaID*</span></span> |<span data-ttu-id="6a97f-p103">GUID d'une requête d'un schéma de fournisseur non définie par la spécification OLE DB. Ce paramètre est obligatoire si *TypeRequête* a la valeur **adSchemaProviderSpecific** ; sinon, il n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="6a97f-p103">The GUID for a provider-schema query not defined by the OLE DB specification. This parameter is required if *QueryType* is set to **adSchemaProviderSpecific**; otherwise, it is not used.</span></span>|

## <a name="remarks"></a><span data-ttu-id="6a97f-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="6a97f-122">Remarks</span></span>

<span data-ttu-id="6a97f-123">La méthode **OpenSchema** renvoie des informations autodescriptives sur la source de données, telles que les tables figurant dans la source de données, les colonnes des tables et les type de données pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6a97f-123">The **OpenSchema** method returns self-descriptive information about the data source, such as what tables are in the data source, the columns in the tables, and the data types supported.</span></span>

<span data-ttu-id="6a97f-p104">L'argument *TypeRequête* est un GUID qui indique les colonnes (schémas) retournés. La spécification OLE DB comporte une liste complète de schémas.</span><span class="sxs-lookup"><span data-stu-id="6a97f-p104">The *QueryType* argument is a GUID that indicates the columns (schemas) returned. The OLE DB specification has a full list of schemas.</span></span>

<span data-ttu-id="6a97f-p105">L'argument *Critères* limite les résultats d'une requête de schéma. *Critères* spécifie un tableau de valeurs qui doivent apparaître dans un sous-ensemble correspondant de colonnes, appelées *colonnes de contraintes* dans l'objet **Recordset** résultant.</span><span class="sxs-lookup"><span data-stu-id="6a97f-p105">The *Criteria* argument limits the results of a schema query. *Criteria* specifies an array of values that must occur in a corresponding subset of columns, called *constraint columns*, in the resulting **Recordset**.</span></span>

<span data-ttu-id="6a97f-p106">La constante **adSchemaProviderSpecific** est utilisée comme argument *TypeRequête* si le fournisseur définit ses propres requêtes de schéma non standard, autres que celles répertoriées ci-dessus. Lorsque cette constante est utilisée, l'argument *IDSchéma* doit être utilisé pour passer le GUID de la requête de schéma à exécuter. Si *TypeRequête* a la valeur **adSchemaProviderSpecific** mais si *IDSchéma* n'est pas spécifié, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="6a97f-p106">The constant **adSchemaProviderSpecific** is used for the *QueryType* argument if the provider defines its own nonstandard schema queries outside those listed above. When this constant is used, the *SchemaID* argument is required to pass the GUID of the schema query to execute. If *QueryType* is set to **adSchemaProviderSpecific** but *SchemaID* is not provided, an error will result.</span></span>

<span data-ttu-id="6a97f-p107">Les fournisseurs ne doivent pas obligatoirement prendre en charge toutes les requêtes de schéma standard OLE DB. En fait, seules les requêtes **adSchemaTables**, **adSchemaColumns** et **adSchemaProviderTypes** sont requises par la spécification OLE DB. Le fournisseur ne doit pas non plus nécessairement prendre en charge les contraintes de l'argument *Critères* répertoriées ci-dessus pour ces requêtes de schéma.</span><span class="sxs-lookup"><span data-stu-id="6a97f-p107">Providers are not required to support all of the OLE DB standard schema queries. Specifically, only **adSchemaTables**, **adSchemaColumns**, and **adSchemaProviderTypes** are required by the OLE DB specification. However, the provider is not required to support the *Criteria* constraints listed above for those schema queries.</span></span>

<span data-ttu-id="6a97f-134">**Utilisation du service de données à distance** La **méthode OpenSchema** n’est pas disponible sur un objet [Connection](connection-object-ado.md) côté client.</span><span class="sxs-lookup"><span data-stu-id="6a97f-134">**Remote Data Service Usage** The **OpenSchema** method is not available on a client-side [Connection](connection-object-ado.md) object.</span></span>

> [!NOTE]
> <span data-ttu-id="6a97f-p108">Dans Visual Basic, les colonnes qui possèdent un entier non signé de quatre octets (DBTYPE UI4) dans l'objet **Recordset** retourné par la méthode **OpenSchema** de l'objet **Connection** ne peuvent pas être comparées à d'autres variables. Pour plus d'informations sur les types de données OLE DB, consultez le chapitre 13 et l'Annexe A du *Guide de référence du programmeur Microsoft OLE DB*.</span><span class="sxs-lookup"><span data-stu-id="6a97f-p108">In Visual Basic, columns that have a four-byte unsigned integer (DBTYPE UI4) in the **Recordset** returned from the **OpenSchema** method on the **Connection** object cannot be compared to other variables. For more information about OLE DB data types, see Chapter 13 and Appendix A of the *Microsoft OLE DB Programmer's Reference*.</span></span>


