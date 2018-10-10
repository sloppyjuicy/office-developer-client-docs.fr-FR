---
title: Append, méthode (Index ADOX)
TOCTitle: Append Method (ADOX Indexes)
ms:assetid: 015ebab4-5e9d-8777-ac82-4d20e957c274
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248784(v=office.15)
ms:contentKeyID: 48542933
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5f91535075c2782861dc409a6c527f159cd5458a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469898"
---
# <a name="append-method-adox-indexes"></a><span data-ttu-id="e378f-102">Append, méthode (Index ADOX)</span><span class="sxs-lookup"><span data-stu-id="e378f-102">Append Method (ADOX Indexes)</span></span>


<span data-ttu-id="e378f-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e378f-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="e378f-104">Ajoute un nouvel objet [Index](index-object-adox.md) à la collection [Indexes](indexes-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="e378f-104">Adds a new [Index](index-object-adox.md) object to the [Indexes](indexes-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="e378f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e378f-105">Syntax</span></span>

<span data-ttu-id="e378f-106">*Index*. Ajouter des*Index* \[,*colonnes*\]</span><span class="sxs-lookup"><span data-stu-id="e378f-106">*Indexes*.Append*Index* \[,*Columns*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="e378f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e378f-107">Parameters</span></span>

  - <span data-ttu-id="e378f-108">*Index*</span><span class="sxs-lookup"><span data-stu-id="e378f-108">*Index*</span></span>

  - <span data-ttu-id="e378f-109">Objet **Index** à ajouter ou nom de l'index à créer et à ajouter.</span><span class="sxs-lookup"><span data-stu-id="e378f-109">The **Index** object to append or the name of the index to create and append.</span></span>

  - <span data-ttu-id="e378f-110">*Columns*</span><span class="sxs-lookup"><span data-stu-id="e378f-110">*Columns*</span></span>

  - <span data-ttu-id="e378f-111">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="e378f-111">Optional.</span></span> <span data-ttu-id="e378f-112">Valeur de type **Variant** qui spécifie le ou les noms des colonne à indexer.</span><span class="sxs-lookup"><span data-stu-id="e378f-112">A **Variant** value that specifies the name(s) of the column(s) to be indexed.</span></span> <span data-ttu-id="e378f-113">Le paramètre *Columns* correspond à l’ou les valeurs de la propriété [Name](name-property-adox.md) d’un objet [Column](column-object-adox.md) ou des objets.</span><span class="sxs-lookup"><span data-stu-id="e378f-113">The *Columns* parameter corresponds to the value(s) of the [Name](name-property-adox.md) property of a [Column](column-object-adox.md) object or objects.</span></span>

## <a name="remarks"></a><span data-ttu-id="e378f-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="e378f-114">Remarks</span></span>

<span data-ttu-id="e378f-115">Le paramètre *Columns* peut prendre soit le nom d’une colonne ou un tableau de noms de colonne.</span><span class="sxs-lookup"><span data-stu-id="e378f-115">The *Columns* parameter can take either the name of a column or an array of column names.</span></span>

<span data-ttu-id="e378f-116">Une erreur se produit si le fournisseur ne prend pas en charge la création d'index.</span><span class="sxs-lookup"><span data-stu-id="e378f-116">An error will occur if the provider does not support creating indexes.</span></span>

