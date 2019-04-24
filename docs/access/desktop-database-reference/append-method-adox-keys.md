---
title: Append, méthode (Clés ADOX)
TOCTitle: Append method (ADOX Keys)
ms:assetid: 14d6e8d7-5c9e-a422-47d6-ebfd9dd7a120
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248913(v=office.15)
ms:contentKeyID: 48543396
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c301f6809ab7f785497637b12e0b5d7a0bb7772d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297087"
---
# <a name="append-method-adox-keys"></a><span data-ttu-id="09846-102">Append, méthode (Clés ADOX)</span><span class="sxs-lookup"><span data-stu-id="09846-102">Append method (ADOX Keys)</span></span>

<span data-ttu-id="09846-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="09846-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="09846-104">Ajoute un nouvel objet [Key](key-object-adox.md) à la collection [Keys](keys-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="09846-104">Adds a new [Key](key-object-adox.md) object to the [Keys](keys-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="09846-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09846-105">Syntax</span></span>

<span data-ttu-id="09846-106">*Clés*. *Touche* \[Append,*KeyType* \] \[,*Column* \] \[,\*\* \] RelatedTable \[,*RelatedColumn*\]</span><span class="sxs-lookup"><span data-stu-id="09846-106">*Keys*.Append*Key* \[,*KeyType*\] \[,*Column*\] \[,*RelatedTable*\] \[,*RelatedColumn*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="09846-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="09846-107">Parameters</span></span>

|<span data-ttu-id="09846-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="09846-108">Parameter</span></span>|<span data-ttu-id="09846-109">Description</span><span class="sxs-lookup"><span data-stu-id="09846-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="09846-110">*Key*</span><span class="sxs-lookup"><span data-stu-id="09846-110">*Key*</span></span> |<span data-ttu-id="09846-111">Objet **Key** à ajouter ou nom de la clé à créer et à ajouter.</span><span class="sxs-lookup"><span data-stu-id="09846-111">The **Key** object to append or the name of the key to create and append.</span></span>|
|<span data-ttu-id="09846-112">*KeyType*</span><span class="sxs-lookup"><span data-stu-id="09846-112">*KeyType*</span></span> |<span data-ttu-id="09846-113">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="09846-113">Optional.</span></span> <span data-ttu-id="09846-114">Valeur de type **Long** qui spécifie le type de clé.</span><span class="sxs-lookup"><span data-stu-id="09846-114">A **Long** value that specifies the type of key.</span></span> <span data-ttu-id="09846-115">Le paramètre *Key* correspond à la propriété [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox) d’un objet **Key**.</span><span class="sxs-lookup"><span data-stu-id="09846-115">The *Key* parameter corresponds to the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox) property of a **Key** object.</span></span>|
|<span data-ttu-id="09846-116">*Colonne*</span><span class="sxs-lookup"><span data-stu-id="09846-116">*Column*</span></span> |<span data-ttu-id="09846-p102">Facultatif. Valeur de type **String** qui spécifie le nom de la colonne à indexer. Le paramètre *Columns* correspond à la valeur de la propriété [Name](name-property-adox.md) d’un objet [Column](column-object-adox.md).</span><span class="sxs-lookup"><span data-stu-id="09846-p102">Optional. A **String** value that specifies the name of the column to be indexed. The *Columns* parameter corresponds to the value of the [Name](name-property-adox.md) property of a [Column](column-object-adox.md) object.</span></span>|
|<span data-ttu-id="09846-120">*RelatedTable*</span><span class="sxs-lookup"><span data-stu-id="09846-120">*RelatedTable*</span></span> |<span data-ttu-id="09846-p103">Facultatif. Valeur de type **String** qui spécifie le nom de la table liée. Le paramètre *RelatedTable* correspond à la valeur de la propriété **Name** d’un objet [Table](table-object-adox.md).</span><span class="sxs-lookup"><span data-stu-id="09846-p103">Optional. A **String** value that specifies the name of the related table. The *RelatedTable* parameter corresponds to the value of the **Name** property of a [Table](table-object-adox.md) object.</span></span>|
|<span data-ttu-id="09846-124">*RelatedColumn*</span><span class="sxs-lookup"><span data-stu-id="09846-124">*RelatedColumn*</span></span> |<span data-ttu-id="09846-p104">Facultatif. Valeur de type **String** qui spécifie le nom de la colonne liée pour une clé étrangère. Le paramètre RelatedColumn correspond à la valeur de la propriété **Name** d'un objet **Column**.</span><span class="sxs-lookup"><span data-stu-id="09846-p104">Optional. A **String** value that specifies the name of the related column for a foreign key. The RelatedColumn parameter corresponds to the value of the **Name** property of a **Column** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="09846-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="09846-128">Remarks</span></span>

<span data-ttu-id="09846-129">Le paramètre *Columns* peut prendre soit le nom d'une colonne, soit une matrice de noms de colonne.</span><span class="sxs-lookup"><span data-stu-id="09846-129">The *Columns* parameter can take either the name of a column or an array of column names.</span></span>

