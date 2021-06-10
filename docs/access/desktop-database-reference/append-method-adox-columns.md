---
title: Append, méthode (Colonnes ADOX)
TOCTitle: Append method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 48bc100b7b56265a570ce963b80f569f1d827150
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297122"
---
# <a name="append-method-adox-columns"></a><span data-ttu-id="6b741-102">Append, méthode (Colonnes ADOX)</span><span class="sxs-lookup"><span data-stu-id="6b741-102">Append method (ADOX Columns)</span></span>

<span data-ttu-id="6b741-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6b741-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6b741-104">Ajoute un nouvel objet [Column](column-object-adox.md) à la collection [Columns](columns-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="6b741-104">Adds a new [Column](column-object-adox.md) object to the [Columns](columns-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b741-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6b741-105">Syntax</span></span>

<span data-ttu-id="6b741-106">*Colonnes*.</span><span class="sxs-lookup"><span data-stu-id="6b741-106">*Columns*.</span></span> <span data-ttu-id="6b741-107">Append *Column* \[ ,*Type* \] \[ ,*DefinedSize*\]</span><span class="sxs-lookup"><span data-stu-id="6b741-107">Append *Column* \[,*Type*\] \[,*DefinedSize*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="6b741-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6b741-108">Parameters</span></span>

|<span data-ttu-id="6b741-109">Paramètre</span><span class="sxs-lookup"><span data-stu-id="6b741-109">Parameter</span></span>|<span data-ttu-id="6b741-110">Description</span><span class="sxs-lookup"><span data-stu-id="6b741-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="6b741-111">*Column*</span><span class="sxs-lookup"><span data-stu-id="6b741-111">*Column*</span></span> |<span data-ttu-id="6b741-112">Objet **Column** à ajouter ou nom de la colonne à créer et à ajouter.</span><span class="sxs-lookup"><span data-stu-id="6b741-112">The **Column** object to append or the name of the column to create and append.</span></span>|
|<span data-ttu-id="6b741-113">*Type*</span><span class="sxs-lookup"><span data-stu-id="6b741-113">*Type*</span></span> |<span data-ttu-id="6b741-p102">Facultatif. Valeur de type **long** qui spécifie le type de données de la colonne. Le paramètre *Type* correspond à la propriété [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) d’un objet **Column**.</span><span class="sxs-lookup"><span data-stu-id="6b741-p102">Optional. A **Long** value that specifies the data type of the column. The *Type* parameter corresponds to the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) property of a **Column** object.</span></span>|
|<span data-ttu-id="6b741-117">*DefinedSize*</span><span class="sxs-lookup"><span data-stu-id="6b741-117">*DefinedSize*</span></span> |<span data-ttu-id="6b741-p103">Facultatif. Valeur de type **long** qui spécifie la taille de la colonne. Le paramètre *DefinedSize* correspond à la propriété [DefinedSize](definedsize-property-adox.md) d’
un objet **Column**.</span><span class="sxs-lookup"><span data-stu-id="6b741-p103">Optional. A **Long** value that specifies the size of the column. The *DefinedSize* parameter corresponds to the [DefinedSize](definedsize-property-adox.md) property of a **Column** object.</span></span>|


> [!NOTE]
> <span data-ttu-id="6b741-121">Une erreur se produit en cas d’ajout d’un objet **Column** à la collection **Columns** d’un objet [Index](index-object-adox.md) si l’objet **Column** n’existe pas dans un objet [Table](table-object-adox.md) déjà ajouté à la collection [Tables](tables-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="6b741-121">An error will occur when appending a **Column** to the **Columns** collection of an [Index](index-object-adox.md) if the **Column** does not exist in a [Table](table-object-adox.md) that is already appended to the [Tables](tables-collection-adox.md) collection.</span></span>


