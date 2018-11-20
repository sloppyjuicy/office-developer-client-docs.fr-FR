---
title: Append, méthode (Colonnes ADOX)
TOCTitle: Append method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 12e79802587874aacb5b47a56387e331b8148069
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026371"
---
# <a name="append-method-adox-columns"></a><span data-ttu-id="0f4d8-102">Append, méthode (Colonnes ADOX)</span><span class="sxs-lookup"><span data-stu-id="0f4d8-102">Append method (ADOX Columns)</span></span>

<span data-ttu-id="0f4d8-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0f4d8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0f4d8-104">Ajoute un nouvel objet [Column](column-object-adox.md) à la collection [Columns](columns-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="0f4d8-104">Adds a new [Column](column-object-adox.md) object to the [Columns](columns-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f4d8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0f4d8-105">Syntax</span></span>

<span data-ttu-id="0f4d8-106">*Colonnes*.</span><span class="sxs-lookup"><span data-stu-id="0f4d8-106">*Columns*.</span></span> <span data-ttu-id="0f4d8-107">Ajouter la*colonne* \[,*Type* \] \[,*DefinedSize*\]</span><span class="sxs-lookup"><span data-stu-id="0f4d8-107">Append*Column* \[,*Type*\] \[,*DefinedSize*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="0f4d8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f4d8-108">Parameters</span></span>

|<span data-ttu-id="0f4d8-109">Paramètre</span><span class="sxs-lookup"><span data-stu-id="0f4d8-109">Parameter</span></span>|<span data-ttu-id="0f4d8-110">Description</span><span class="sxs-lookup"><span data-stu-id="0f4d8-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="0f4d8-111">*Column*</span><span class="sxs-lookup"><span data-stu-id="0f4d8-111">*Column*</span></span> |<span data-ttu-id="0f4d8-112">Objet **Column** à ajouter ou nom de la colonne à créer et à ajouter.</span><span class="sxs-lookup"><span data-stu-id="0f4d8-112">The **Column** object to append or the name of the column to create and append.</span></span>|
|<span data-ttu-id="0f4d8-113">*Type*</span><span class="sxs-lookup"><span data-stu-id="0f4d8-113">*Type*</span></span> |<span data-ttu-id="0f4d8-114">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="0f4d8-114">Optional.</span></span> <span data-ttu-id="0f4d8-115">Valeur de type **long** qui spécifie le type de données de la colonne.</span><span class="sxs-lookup"><span data-stu-id="0f4d8-115">A **Long** value that specifies the data type of the column.</span></span> <span data-ttu-id="0f4d8-116">Le paramètre *Type* correspond à la propriété [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) d’un objet **Column** .</span><span class="sxs-lookup"><span data-stu-id="0f4d8-116">The *Type* parameter corresponds to the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) property of a **Column** object.</span></span>|
|<span data-ttu-id="0f4d8-117">*DefinedSize*</span><span class="sxs-lookup"><span data-stu-id="0f4d8-117">*DefinedSize*</span></span> |<span data-ttu-id="0f4d8-118">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="0f4d8-118">Optional.</span></span> <span data-ttu-id="0f4d8-119">Valeur de type **long** qui spécifie la taille de la colonne.</span><span class="sxs-lookup"><span data-stu-id="0f4d8-119">A **Long** value that specifies the size of the column.</span></span> <span data-ttu-id="0f4d8-120">Le paramètre *DefinedSize* correspond à la propriété [DefinedSize](definedsize-property-adox.md) d’un objet **Column** .</span><span class="sxs-lookup"><span data-stu-id="0f4d8-120">The *DefinedSize* parameter corresponds to the [DefinedSize](definedsize-property-adox.md) property of a **Column** object.</span></span>|


> [!NOTE]
> <span data-ttu-id="0f4d8-121">[!REMARQUE] Une erreur survient lors de l'ajout d'une **colonne** à la collection **Columns** d'un [index](index-object-adox.md) si la **colonne** n'existe pas dans une [table](table-object-adox.md) déjà ajoutée à la collection [Tables](tables-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="0f4d8-121">An error will occur when appending a **Column** to the **Columns** collection of an [Index](index-object-adox.md) if the **Column** does not exist in a [Table](table-object-adox.md) that is already appended to the [Tables](tables-collection-adox.md) collection.</span></span>


