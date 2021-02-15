---
title: Create, méthode (ADOX)
TOCTitle: Create method (ADOX)
ms:assetid: d4072ee7-a0b9-7780-7be0-1d64b42b437c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250060(v=office.15)
ms:contentKeyID: 48547924
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e98854665185d682b9049b000bf4b600040ba624
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295421"
---
# <a name="create-method-adox"></a><span data-ttu-id="1cc5a-102">Create, méthode (ADOX)</span><span class="sxs-lookup"><span data-stu-id="1cc5a-102">Create method (ADOX)</span></span>

<span data-ttu-id="1cc5a-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1cc5a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1cc5a-104">Crée un catalogue.</span><span class="sxs-lookup"><span data-stu-id="1cc5a-104">Creates a new catalog.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cc5a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1cc5a-105">Syntax</span></span>

<span data-ttu-id="1cc5a-106">*Catalogue*. Créer *ConnectString*</span><span class="sxs-lookup"><span data-stu-id="1cc5a-106">*Catalog*.Create *ConnectString*</span></span>

## <a name="parameters"></a><span data-ttu-id="1cc5a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1cc5a-107">Parameters</span></span>

|<span data-ttu-id="1cc5a-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="1cc5a-108">Parameter</span></span>|<span data-ttu-id="1cc5a-109">Description</span><span class="sxs-lookup"><span data-stu-id="1cc5a-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="1cc5a-110">*ConnectString*</span><span class="sxs-lookup"><span data-stu-id="1cc5a-110">*ConnectString*</span></span> |<span data-ttu-id="1cc5a-111">Valeur de type **String** utilisée pour se connecter à la source de données.</span><span class="sxs-lookup"><span data-stu-id="1cc5a-111">A **String** value used to connect to the data source.</span></span>|

## <a name="remarks"></a><span data-ttu-id="1cc5a-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="1cc5a-112">Remarks</span></span>

<span data-ttu-id="1cc5a-p101">La méthode **Create** crée et ouvre un nouvel objet ADO [Connection](connection-object-ado.md) à la source de données spécifiée dans le paramètre *ConnectString*. En cas de réussite, le nouvel objet **Connection** est affecté à la propriété [ActiveConnection](activeconnection-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="1cc5a-p101">The **Create** method creates and opens a new ADO [Connection](connection-object-ado.md) to the data source specified in *ConnectString*. If successful, the new **Connection** object is assigned to the [ActiveConnection](activeconnection-property-adox.md) property.</span></span>

<span data-ttu-id="1cc5a-115">Une erreur se produit si le fournisseur ne prend pas en charge la création de catalogues.</span><span class="sxs-lookup"><span data-stu-id="1cc5a-115">An error will occur if the provider does not support creating new catalogs.</span></span>

