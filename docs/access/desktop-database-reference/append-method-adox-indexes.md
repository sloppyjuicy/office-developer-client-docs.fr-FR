---
title: Append, méthode (Index ADOX)
TOCTitle: Append method (ADOX Indexes)
ms:assetid: 015ebab4-5e9d-8777-ac82-4d20e957c274
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248784(v=office.15)
ms:contentKeyID: 48542933
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0b541512de9748e94d033bb56f27dd0941c7f5a7
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707555"
---
# <a name="append-method-adox-indexes"></a><span data-ttu-id="e0bb9-102">Append, méthode (Index ADOX)</span><span class="sxs-lookup"><span data-stu-id="e0bb9-102">Append method (ADOX Indexes)</span></span>


<span data-ttu-id="e0bb9-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e0bb9-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="e0bb9-104">Ajoute un nouvel objet [Index](index-object-adox.md) à la collection [Indexes](indexes-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="e0bb9-104">Adds a new [Index](index-object-adox.md) object to the [Indexes](indexes-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0bb9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e0bb9-105">Syntax</span></span>

<span data-ttu-id="e0bb9-106">*Index*. Ajouter des*Index* \[,*colonnes*\]</span><span class="sxs-lookup"><span data-stu-id="e0bb9-106">*Indexes*.Append*Index* \[,*Columns*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="e0bb9-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="e0bb9-107">Parameters</span></span>

|<span data-ttu-id="e0bb9-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="e0bb9-108">Parameter</span></span>|<span data-ttu-id="e0bb9-109">Description</span><span class="sxs-lookup"><span data-stu-id="e0bb9-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="e0bb9-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="e0bb9-110">*Index*</span></span> |<span data-ttu-id="e0bb9-111">Objet **Index** à ajouter ou nom de l'index à créer et à ajouter.</span><span class="sxs-lookup"><span data-stu-id="e0bb9-111">The **Index** object to append or the name of the index to create and append.</span></span>|
|<span data-ttu-id="e0bb9-112">*Columns*</span><span class="sxs-lookup"><span data-stu-id="e0bb9-112">*Columns*</span></span> |<span data-ttu-id="e0bb9-113">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="e0bb9-113">Optional.</span></span> <span data-ttu-id="e0bb9-114">Valeur de type **Variant** qui spécifie le ou les noms des colonne à indexer.</span><span class="sxs-lookup"><span data-stu-id="e0bb9-114">A **Variant** value that specifies the name(s) of the column(s) to be indexed.</span></span> <span data-ttu-id="e0bb9-115">Le paramètre *Columns* correspond à l’ou les valeurs de la propriété [Name](name-property-adox.md) d’un objet [Column](column-object-adox.md) ou des objets.</span><span class="sxs-lookup"><span data-stu-id="e0bb9-115">The *Columns* parameter corresponds to the value(s) of the [Name](name-property-adox.md) property of a [Column](column-object-adox.md) object or objects.</span></span>|

## <a name="remarks"></a><span data-ttu-id="e0bb9-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="e0bb9-116">Remarks</span></span>

<span data-ttu-id="e0bb9-117">Le paramètre *Columns* peut prendre soit le nom d’une colonne ou un tableau de noms de colonne.</span><span class="sxs-lookup"><span data-stu-id="e0bb9-117">The *Columns* parameter can take either the name of a column or an array of column names.</span></span>

<span data-ttu-id="e0bb9-118">Une erreur se produit si le fournisseur ne prend pas en charge la création d'index.</span><span class="sxs-lookup"><span data-stu-id="e0bb9-118">An error will occur if the provider does not support creating indexes.</span></span>

