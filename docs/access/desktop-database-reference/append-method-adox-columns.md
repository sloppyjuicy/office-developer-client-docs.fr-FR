---
title: Append, méthode (Colonnes ADOX)
TOCTitle: Append Method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ec64241bf63719fe4f5c547d60a93f7804f181ca
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877659"
---
# <a name="append-method-adox-columns"></a><span data-ttu-id="89b0d-102">Append, méthode (Colonnes ADOX)</span><span class="sxs-lookup"><span data-stu-id="89b0d-102">Append Method (ADOX Columns)</span></span>


<span data-ttu-id="89b0d-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="89b0d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="89b0d-104">Ajoute un nouvel objet [Column](column-object-adox.md) à la collection [Columns](columns-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="89b0d-104">Adds a new [Column](column-object-adox.md) object to the [Columns](columns-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="89b0d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="89b0d-105">Syntax</span></span>

<span data-ttu-id="89b0d-106">*Colonnes*.</span><span class="sxs-lookup"><span data-stu-id="89b0d-106">*Columns*.</span></span> <span data-ttu-id="89b0d-107">Ajouter la*colonne* \[,*Type* \] \[,*DefinedSize*\]</span><span class="sxs-lookup"><span data-stu-id="89b0d-107">Append*Column* \[,*Type*\] \[,*DefinedSize*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="89b0d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="89b0d-108">Parameters</span></span>

  - <span data-ttu-id="89b0d-109">*Column*</span><span class="sxs-lookup"><span data-stu-id="89b0d-109">*Column*</span></span>

  - <span data-ttu-id="89b0d-110">Objet **Column** à ajouter ou nom de la colonne à créer et à ajouter.</span><span class="sxs-lookup"><span data-stu-id="89b0d-110">The **Column** object to append or the name of the column to create and append.</span></span>

  - <span data-ttu-id="89b0d-111">*Type*</span><span class="sxs-lookup"><span data-stu-id="89b0d-111">*Type*</span></span>

  - <span data-ttu-id="89b0d-112">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="89b0d-112">Optional.</span></span> <span data-ttu-id="89b0d-113">Valeur de type **long** qui spécifie le type de données de la colonne.</span><span class="sxs-lookup"><span data-stu-id="89b0d-113">A **Long** value that specifies the data type of the column.</span></span> <span data-ttu-id="89b0d-114">Le paramètre *Type* correspond à la propriété [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) d’un objet **Column** .</span><span class="sxs-lookup"><span data-stu-id="89b0d-114">The *Type* parameter corresponds to the [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) property of a **Column** object.</span></span>

  - <span data-ttu-id="89b0d-115">*DefinedSize*</span><span class="sxs-lookup"><span data-stu-id="89b0d-115">*DefinedSize*</span></span>

  - <span data-ttu-id="89b0d-116">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="89b0d-116">Optional.</span></span> <span data-ttu-id="89b0d-117">Valeur de type **long** qui spécifie la taille de la colonne.</span><span class="sxs-lookup"><span data-stu-id="89b0d-117">A **Long** value that specifies the size of the column.</span></span> <span data-ttu-id="89b0d-118">Le paramètre *DefinedSize* correspond à la propriété [DefinedSize](definedsize-property-adox.md) d’un objet **Column** .</span><span class="sxs-lookup"><span data-stu-id="89b0d-118">The *DefinedSize* parameter corresponds to the [DefinedSize](definedsize-property-adox.md) property of a **Column** object.</span></span>


> [!NOTE]
> <span data-ttu-id="89b0d-119">[!REMARQUE] Une erreur survient lors de l'ajout d'une **colonne** à la collection **Columns** d'un [index](index-object-adox.md) si la **colonne** n'existe pas dans une [table](table-object-adox.md) déjà ajoutée à la collection [Tables](tables-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="89b0d-119">An error will occur when appending a **Column** to the **Columns** collection of an [Index](index-object-adox.md) if the **Column** does not exist in a [Table](table-object-adox.md) that is already appended to the [Tables](tables-collection-adox.md) collection.</span></span>


