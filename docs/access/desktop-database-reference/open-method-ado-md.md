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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288398"
---
# <a name="open-method-ado-md"></a><span data-ttu-id="ed577-102">Open, méthode (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="ed577-102">Open method (ADO MD)</span></span>

<span data-ttu-id="ed577-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ed577-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ed577-104">Récupère les résultats d'une requête multidimensionnelle et renvoie les résultats dans un ensemble de cellules.</span><span class="sxs-lookup"><span data-stu-id="ed577-104">Retrieves the results of a multidimensional query and returns the results to a cellset.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed577-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ed577-105">Syntax</span></span>

<span data-ttu-id="ed577-106">*Cellset*. Open *Source*, *ActiveConnection*</span><span class="sxs-lookup"><span data-stu-id="ed577-106">*Cellset*.Open *Source*, *ActiveConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="ed577-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ed577-107">Parameters</span></span>

|<span data-ttu-id="ed577-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ed577-108">Parameter</span></span>|<span data-ttu-id="ed577-109">Description</span><span class="sxs-lookup"><span data-stu-id="ed577-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="ed577-110">*Source*</span><span class="sxs-lookup"><span data-stu-id="ed577-110">*Source*</span></span> |<span data-ttu-id="ed577-p101">Facultatif. Valeur de type **Variant** qui correspond à une requête multidimensionnelle valide, telle que la requête MDX (Multidimensional Expression). L’argument *Source* correspond à la propriété [Source](source-property-ado-md.md). Pour plus d’informations sur MDX, voir la documentation relative à OLE DB pour OLAP dans le kit de développement logiciel Microsoft Data Access Components SDK.</span><span class="sxs-lookup"><span data-stu-id="ed577-p101">Optional. A **Variant** that evaluates to a valid multidimensional query, such as a Multidimensional Expression (MDX) query. The *Source* argument corresponds to the [Source](source-property-ado-md.md) property. For more information about MDX, see the OLE DB for OLAP documentation in the Microsoft Data Access Components SDK.</span></span>|
|<span data-ttu-id="ed577-115">*ActiveConnection*</span><span class="sxs-lookup"><span data-stu-id="ed577-115">*ActiveConnection*</span></span> |<span data-ttu-id="ed577-p102">Facultatif. Valeur de type **Variant** qui correspond à une chaîne spécifiant soit un nom de variable objet [Connection](connection-object-ado.md) ADO valide, soit une définition d’une connexion. L’argument *ActiveConnection* spécifie la connexion avec laquelle l’objet [Cellset](cellset-object-ado-md.md) doit être ouvert. Si vous passez une définition de connexion pour cet argument, ADO ouvre une nouvelle connexion à l’aide des paramètres spécifiés. L’argument *ActiveConnection* correspond à la propriété [ActiveConnection](activeconnection-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="ed577-p102">Optional. A **Variant** that evaluates to a string specifying either a valid ADO [Connection](connection-object-ado.md) object variable name or a definition for a connection. The *ActiveConnection* argument specifies the connection in which to open the [Cellset](cellset-object-ado-md.md) object. If you pass a connection definition for this argument, ADO opens a new connection using the specified parameters. The *ActiveConnection* argument corresponds to the [ActiveConnection](activeconnection-property-ado-md.md) property.</span></span>|

## <a name="remarks"></a><span data-ttu-id="ed577-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="ed577-121">Remarks</span></span>

<span data-ttu-id="ed577-122">La méthode **Open** génère une erreur si l'un de ses paramètres est omis et que sa propriété correspondante n'a pas été définie avant la tentative d'ouverture de l'objet **Cellset**.</span><span class="sxs-lookup"><span data-stu-id="ed577-122">The **Open** method generates an error if either of its parameters is omitted and its corresponding property value has not been set prior to attempting to open the **Cellset**.</span></span>

