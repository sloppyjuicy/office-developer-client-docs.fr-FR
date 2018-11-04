---
title: Append, méthode (Colonnes ADOX)
TOCTitle: Append method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7a6f7ac26c3089a973a68e07acbe0f6f3e4029df
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949438"
---
# <a name="append-method-adox-columns"></a><span data-ttu-id="70377-102">Append, méthode (Colonnes ADOX)</span><span class="sxs-lookup"><span data-stu-id="70377-102">Append method (ADOX Columns)</span></span>

<span data-ttu-id="70377-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="70377-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="70377-104">Ajoute un nouvel objet [Column](column-object-adox.md) à la collection [Columns](columns-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="70377-104">Adds a new [Column](column-object-adox.md) object to the [Columns](columns-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="70377-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="70377-105">Syntax</span></span>

<span data-ttu-id="70377-106">*Colonnes*.</span><span class="sxs-lookup"><span data-stu-id="70377-106">*Columns*.</span></span> <span data-ttu-id="70377-107">Ajouter la*colonne* \[,*Type* \] \[,*DefinedSize*\]</span><span class="sxs-lookup"><span data-stu-id="70377-107">Append*Column* \[,*Type*\] \[,*DefinedSize*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="70377-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="70377-108">Parameters</span></span>

|<span data-ttu-id="70377-109">Paramètre</span><span class="sxs-lookup"><span data-stu-id="70377-109">Parameter</span></span>|<span data-ttu-id="70377-110">Description</span><span class="sxs-lookup"><span data-stu-id="70377-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="70377-111">*Column*</span><span class="sxs-lookup"><span data-stu-id="70377-111">*Column*</span></span> |<span data-ttu-id="70377-112">Objet **Column** à ajouter ou nom de la colonne à créer et à ajouter.</span><span class="sxs-lookup"><span data-stu-id="70377-112">The **Column** object to append or the name of the column to create and append.</span></span>|
|<span data-ttu-id="70377-113">*Type*</span><span class="sxs-lookup"><span data-stu-id="70377-113">*Type*</span></span> |<span data-ttu-id="70377-114">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="70377-114">Optional.</span></span> <span data-ttu-id="70377-115">Valeur de type **long** qui spécifie le type de données de la colonne.</span><span class="sxs-lookup"><span data-stu-id="70377-115">A **Long** value that specifies the data type of the column.</span></span> <span data-ttu-id="70377-116">Le paramètre *Type* correspond à la propriété [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) d’un objet **Column** .</span><span class="sxs-lookup"><span data-stu-id="70377-116">The *Type* parameter corresponds to the [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) property of a **Column** object.</span></span>|
|<span data-ttu-id="70377-117">*DefinedSize*</span><span class="sxs-lookup"><span data-stu-id="70377-117">*DefinedSize*</span></span> |<span data-ttu-id="70377-118">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="70377-118">Optional.</span></span> <span data-ttu-id="70377-119">Valeur de type **long** qui spécifie la taille de la colonne.</span><span class="sxs-lookup"><span data-stu-id="70377-119">A **Long** value that specifies the size of the column.</span></span> <span data-ttu-id="70377-120">Le paramètre *DefinedSize* correspond à la propriété [DefinedSize](definedsize-property-adox.md) d’un objet **Column** .</span><span class="sxs-lookup"><span data-stu-id="70377-120">The *DefinedSize* parameter corresponds to the [DefinedSize](definedsize-property-adox.md) property of a **Column** object.</span></span>|


> [!NOTE]
> <span data-ttu-id="70377-121">[!REMARQUE] Une erreur survient lors de l'ajout d'une **colonne** à la collection **Columns** d'un [index](index-object-adox.md) si la **colonne** n'existe pas dans une [table](table-object-adox.md) déjà ajoutée à la collection [Tables](tables-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="70377-121">An error will occur when appending a **Column** to the **Columns** collection of an [Index](index-object-adox.md) if the **Column** does not exist in a [Table](table-object-adox.md) that is already appended to the [Tables](tables-collection-adox.md) collection.</span></span>


