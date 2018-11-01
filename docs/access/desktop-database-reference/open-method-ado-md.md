---
title: Open, méthode (ADO MD)
TOCTitle: Open Method (ADO MD)
ms:assetid: 12395ff6-fe07-325a-2b69-007aa0b11ee6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248894(v=office.15)
ms:contentKeyID: 48543335
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d9b39fa77700fcd1553738d359b8efd7097c183a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870274"
---
# <a name="open-method-ado-md"></a><span data-ttu-id="73fb4-102">Open, méthode (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="73fb4-102">Open Method (ADO MD)</span></span>


<span data-ttu-id="73fb4-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="73fb4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="73fb4-104">Récupère les résultats d'une requête multidimensionnelle et renvoie les résultats dans un ensemble de cellules.</span><span class="sxs-lookup"><span data-stu-id="73fb4-104">Retrieves the results of a multidimensional query and returns the results to a cellset.</span></span>

## <a name="syntax"></a><span data-ttu-id="73fb4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="73fb4-105">Syntax</span></span>

<span data-ttu-id="73fb4-106">*Ensemble de cellules*. Ouvrir la*Source*, *ActiveConnection*</span><span class="sxs-lookup"><span data-stu-id="73fb4-106">*Cellset*.Open*Source*, *ActiveConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="73fb4-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="73fb4-107">Parameters</span></span>

  - <span data-ttu-id="73fb4-108">*Source*</span><span class="sxs-lookup"><span data-stu-id="73fb4-108">*Source*</span></span>

  - <span data-ttu-id="73fb4-109">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="73fb4-109">Optional.</span></span> <span data-ttu-id="73fb4-110">Valeur de type **Variant** qui correspond à une requête multidimensionnelle valide, telle que la requête MDX (Multidimensional Expression).</span><span class="sxs-lookup"><span data-stu-id="73fb4-110">A **Variant** that evaluates to a valid multidimensional query, such as a Multidimensional Expression (MDX) query.</span></span> <span data-ttu-id="73fb4-111">L’argument *Source* correspond à la propriété [Source](source-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="73fb4-111">The *Source* argument corresponds to the [Source](source-property-ado-md.md) property.</span></span> <span data-ttu-id="73fb4-112">Pour plus d'informations sur MDX, voir la documentation relative à OLE DB pour OLAP dans le kit de développement logiciel Microsoft Data Access Components SDK.</span><span class="sxs-lookup"><span data-stu-id="73fb4-112">For more information about MDX, see the OLE DB for OLAP documentation in the Microsoft Data Access Components SDK.</span></span>

  - <span data-ttu-id="73fb4-113">*ActiveConnection*</span><span class="sxs-lookup"><span data-stu-id="73fb4-113">*ActiveConnection*</span></span>

  - <span data-ttu-id="73fb4-114">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="73fb4-114">Optional.</span></span> <span data-ttu-id="73fb4-115">Valeur de type **Variant** qui correspond à une chaîne spécifiant soit un nom de variable objet [Connection](connection-object-ado.md) ADO valide, soit une définition d'une connexion.</span><span class="sxs-lookup"><span data-stu-id="73fb4-115">A **Variant** that evaluates to a string specifying either a valid ADO [Connection](connection-object-ado.md) object variable name or a definition for a connection.</span></span> <span data-ttu-id="73fb4-116">L’argument *ActiveConnection* spécifie la connexion dans laquelle ouvrir l’objet [Cellset](cellset-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="73fb4-116">The *ActiveConnection* argument specifies the connection in which to open the [Cellset](cellset-object-ado-md.md) object.</span></span> <span data-ttu-id="73fb4-117">Si vous passez une définition de connexion pour cet argument, ADO ouvre une nouvelle connexion à l'aide des paramètres spécifiés.</span><span class="sxs-lookup"><span data-stu-id="73fb4-117">If you pass a connection definition for this argument, ADO opens a new connection using the specified parameters.</span></span> <span data-ttu-id="73fb4-118">L’argument *ActiveConnection* correspond à la propriété [ActiveConnection](activeconnection-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="73fb4-118">The *ActiveConnection* argument corresponds to the [ActiveConnection](activeconnection-property-ado-md.md) property.</span></span>

## <a name="remarks"></a><span data-ttu-id="73fb4-119">Notes</span><span class="sxs-lookup"><span data-stu-id="73fb4-119">Remarks</span></span>

<span data-ttu-id="73fb4-120">La méthode **Open** génère une erreur si l'un de ses paramètres est omis et que sa propriété correspondante n'a pas été définie avant la tentative d'ouverture de l'objet **Cellset**.</span><span class="sxs-lookup"><span data-stu-id="73fb4-120">The **Open** method generates an error if either of its parameters is omitted and its corresponding property value has not been set prior to attempting to open the **Cellset**.</span></span>

