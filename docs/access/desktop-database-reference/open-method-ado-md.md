---
title: Open, méthode (ADO MD)
TOCTitle: Open method (ADO MD)
ms:assetid: 12395ff6-fe07-325a-2b69-007aa0b11ee6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248894(v=office.15)
ms:contentKeyID: 48543335
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54f7ce4d5d588e644707cd7b466c29f619850824
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703831"
---
# <a name="open-method-ado-md"></a><span data-ttu-id="f8bc5-102">Open, méthode (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="f8bc5-102">Open method (ADO MD)</span></span>

<span data-ttu-id="f8bc5-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f8bc5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f8bc5-104">Récupère les résultats d'une requête multidimensionnelle et renvoie les résultats dans un ensemble de cellules.</span><span class="sxs-lookup"><span data-stu-id="f8bc5-104">Retrieves the results of a multidimensional query and returns the results to a cellset.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8bc5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f8bc5-105">Syntax</span></span>

<span data-ttu-id="f8bc5-106">*Ensemble de cellules*. Ouvrir la*Source*, *ActiveConnection*</span><span class="sxs-lookup"><span data-stu-id="f8bc5-106">*Cellset*.Open*Source*, *ActiveConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="f8bc5-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="f8bc5-107">Parameters</span></span>

|<span data-ttu-id="f8bc5-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="f8bc5-108">Parameter</span></span>|<span data-ttu-id="f8bc5-109">Description</span><span class="sxs-lookup"><span data-stu-id="f8bc5-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="f8bc5-110">*Source*</span><span class="sxs-lookup"><span data-stu-id="f8bc5-110">*Source*</span></span> |<span data-ttu-id="f8bc5-111">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="f8bc5-111">Optional.</span></span> <span data-ttu-id="f8bc5-112">Valeur de type **Variant** qui correspond à une requête multidimensionnelle valide, telle que la requête MDX (Multidimensional Expression).</span><span class="sxs-lookup"><span data-stu-id="f8bc5-112">A **Variant** that evaluates to a valid multidimensional query, such as a Multidimensional Expression (MDX) query.</span></span> <span data-ttu-id="f8bc5-113">L’argument *Source* correspond à la propriété [Source](source-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="f8bc5-113">The *Source* argument corresponds to the [Source](source-property-ado-md.md) property.</span></span> <span data-ttu-id="f8bc5-114">Pour plus d'informations sur MDX, voir la documentation relative à OLE DB pour OLAP dans le kit de développement logiciel Microsoft Data Access Components SDK.</span><span class="sxs-lookup"><span data-stu-id="f8bc5-114">For more information about MDX, see the OLE DB for OLAP documentation in the Microsoft Data Access Components SDK.</span></span>|
|<span data-ttu-id="f8bc5-115">*ActiveConnection*</span><span class="sxs-lookup"><span data-stu-id="f8bc5-115">*ActiveConnection*</span></span> |<span data-ttu-id="f8bc5-116">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="f8bc5-116">Optional.</span></span> <span data-ttu-id="f8bc5-117">Valeur de type **Variant** qui correspond à une chaîne spécifiant soit un nom de variable objet [Connection](connection-object-ado.md) ADO valide, soit une définition d'une connexion.</span><span class="sxs-lookup"><span data-stu-id="f8bc5-117">A **Variant** that evaluates to a string specifying either a valid ADO [Connection](connection-object-ado.md) object variable name or a definition for a connection.</span></span> <span data-ttu-id="f8bc5-118">L’argument *ActiveConnection* spécifie la connexion dans laquelle ouvrir l’objet [Cellset](cellset-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="f8bc5-118">The *ActiveConnection* argument specifies the connection in which to open the [Cellset](cellset-object-ado-md.md) object.</span></span> <span data-ttu-id="f8bc5-119">Si vous passez une définition de connexion pour cet argument, ADO ouvre une nouvelle connexion à l'aide des paramètres spécifiés.</span><span class="sxs-lookup"><span data-stu-id="f8bc5-119">If you pass a connection definition for this argument, ADO opens a new connection using the specified parameters.</span></span> <span data-ttu-id="f8bc5-120">L’argument *ActiveConnection* correspond à la propriété [ActiveConnection](activeconnection-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="f8bc5-120">The *ActiveConnection* argument corresponds to the [ActiveConnection](activeconnection-property-ado-md.md) property.</span></span>|

## <a name="remarks"></a><span data-ttu-id="f8bc5-121">Notes</span><span class="sxs-lookup"><span data-stu-id="f8bc5-121">Remarks</span></span>

<span data-ttu-id="f8bc5-122">La méthode **Open** génère une erreur si l'un de ses paramètres est omis et que sa propriété correspondante n'a pas été définie avant la tentative d'ouverture de l'objet **Cellset**.</span><span class="sxs-lookup"><span data-stu-id="f8bc5-122">The **Open** method generates an error if either of its parameters is omitted and its corresponding property value has not been set prior to attempting to open the **Cellset**.</span></span>

