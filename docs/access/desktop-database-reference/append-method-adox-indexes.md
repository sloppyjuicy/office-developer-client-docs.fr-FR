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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297094"
---
# <a name="append-method-adox-indexes"></a><span data-ttu-id="0d670-102">Append, méthode (Index ADOX)</span><span class="sxs-lookup"><span data-stu-id="0d670-102">Append method (ADOX Indexes)</span></span>


<span data-ttu-id="0d670-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0d670-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="0d670-104">Ajoute un nouvel objet [Index](index-object-adox.md) à la collection [Indexes](indexes-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="0d670-104">Adds a new [Index](index-object-adox.md) object to the [Indexes](indexes-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d670-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d670-105">Syntax</span></span>

<span data-ttu-id="0d670-106">*Index*. Ajouter un*index* \[,*colonnes*\]</span><span class="sxs-lookup"><span data-stu-id="0d670-106">*Indexes*.Append*Index* \[,*Columns*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="0d670-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d670-107">Parameters</span></span>

|<span data-ttu-id="0d670-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d670-108">Parameter</span></span>|<span data-ttu-id="0d670-109">Description</span><span class="sxs-lookup"><span data-stu-id="0d670-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="0d670-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="0d670-110">*Index*</span></span> |<span data-ttu-id="0d670-111">Objet **Index** à ajouter ou nom de l'index à créer et à ajouter.</span><span class="sxs-lookup"><span data-stu-id="0d670-111">The **Index** object to append or the name of the index to create and append.</span></span>|
|<span data-ttu-id="0d670-112">*Columns*</span><span class="sxs-lookup"><span data-stu-id="0d670-112">*Columns*</span></span> |<span data-ttu-id="0d670-p101">Facultatif. Valeur de type **Variant** qui spécifie le ou les noms des colonne à indexer. Le paramètre *Column* correspond à la ou aux valeurs de la propriété [Name](name-property-adox.md) d’un ou plusieurs objets [Column](column-object-adox.md).</span><span class="sxs-lookup"><span data-stu-id="0d670-p101">Optional. A **Variant** value that specifies the name(s) of the column(s) to be indexed. The *Columns* parameter corresponds to the value(s) of the [Name](name-property-adox.md) property of a [Column](column-object-adox.md) object or objects.</span></span>|

## <a name="remarks"></a><span data-ttu-id="0d670-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="0d670-116">Remarks</span></span>

<span data-ttu-id="0d670-117">Le paramètre *Columns* peut prendre soit le nom d'une colonne, soit une matrice de noms de colonne.</span><span class="sxs-lookup"><span data-stu-id="0d670-117">The *Columns* parameter can take either the name of a column or an array of column names.</span></span>

<span data-ttu-id="0d670-118">Une erreur se produit si le fournisseur ne prend pas en charge la création d'index.</span><span class="sxs-lookup"><span data-stu-id="0d670-118">An error will occur if the provider does not support creating indexes.</span></span>

