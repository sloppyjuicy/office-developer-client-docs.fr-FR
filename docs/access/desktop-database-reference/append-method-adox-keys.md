---
title: Append, méthode (Clés ADOX)
TOCTitle: Append method (ADOX Keys)
ms:assetid: 14d6e8d7-5c9e-a422-47d6-ebfd9dd7a120
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248913(v=office.15)
ms:contentKeyID: 48543396
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cc1d03fe68093959406a444419128b161f3b5be4
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921473"
---
# <a name="append-method-adox-keys"></a><span data-ttu-id="88685-102">Append, méthode (Clés ADOX)</span><span class="sxs-lookup"><span data-stu-id="88685-102">Append method (ADOX Keys)</span></span>


<span data-ttu-id="88685-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="88685-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="88685-104">Ajoute un nouvel objet [Key](key-object-adox.md) à la collection [Keys](keys-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="88685-104">Adds a new [Key](key-object-adox.md) object to the [Keys](keys-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="88685-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="88685-105">Syntax</span></span>

<span data-ttu-id="88685-106">*Clés*. Ajoutez la*clé* \[,*type de clé* \] \[,*colonne* \] \[,*RelatedTable* \] \[,*RelatedColumn*\]</span><span class="sxs-lookup"><span data-stu-id="88685-106">*Keys*.Append*Key* \[,*KeyType*\] \[,*Column*\] \[,*RelatedTable*\] \[,*RelatedColumn*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="88685-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="88685-107">Parameters</span></span>

  - <span data-ttu-id="88685-108">*Key*</span><span class="sxs-lookup"><span data-stu-id="88685-108">*Key*</span></span>

  - <span data-ttu-id="88685-109">Objet **Key** à ajouter ou nom de la clé à créer et à ajouter.</span><span class="sxs-lookup"><span data-stu-id="88685-109">The **Key** object to append or the name of the key to create and append.</span></span>

  - <span data-ttu-id="88685-110">*Type de clé*</span><span class="sxs-lookup"><span data-stu-id="88685-110">*KeyType*</span></span>

  - <span data-ttu-id="88685-111">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="88685-111">Optional.</span></span> <span data-ttu-id="88685-112">Valeur de type **Long** qui spécifie le type de clé.</span><span class="sxs-lookup"><span data-stu-id="88685-112">A **Long** value that specifies the type of key.</span></span> <span data-ttu-id="88685-113">Le paramètre de *clé* correspond à la propriété [Type](https://msdn.microsoft.com/library/jj248879\(v=office.15\)) d’un objet **Key** .</span><span class="sxs-lookup"><span data-stu-id="88685-113">The *Key* parameter corresponds to the [Type](https://msdn.microsoft.com/library/jj248879\(v=office.15\)) property of a **Key** object.</span></span>

  - <span data-ttu-id="88685-114">*Column*</span><span class="sxs-lookup"><span data-stu-id="88685-114">*Column*</span></span>

  - <span data-ttu-id="88685-115">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="88685-115">Optional.</span></span> <span data-ttu-id="88685-116">Valeur de type **String** qui spécifie le nom de la colonne à indexer.</span><span class="sxs-lookup"><span data-stu-id="88685-116">A **String** value that specifies the name of the column to be indexed.</span></span> <span data-ttu-id="88685-117">Le paramètre *Columns* correspond à la valeur de la propriété [Name](name-property-adox.md) d’un objet [Column](column-object-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="88685-117">The *Columns* parameter corresponds to the value of the [Name](name-property-adox.md) property of a [Column](column-object-adox.md) object.</span></span>

  - <span data-ttu-id="88685-118">*RelatedTable*</span><span class="sxs-lookup"><span data-stu-id="88685-118">*RelatedTable*</span></span>

  - <span data-ttu-id="88685-119">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="88685-119">Optional.</span></span> <span data-ttu-id="88685-120">Valeur de type **String** qui spécifie le nom de la table liée.</span><span class="sxs-lookup"><span data-stu-id="88685-120">A **String** value that specifies the name of the related table.</span></span> <span data-ttu-id="88685-121">Le paramètre *RelatedTable* correspond à la valeur de la propriété **Name** d’un objet [Table](table-object-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="88685-121">The *RelatedTable* parameter corresponds to the value of the **Name** property of a [Table](table-object-adox.md) object.</span></span>

  - <span data-ttu-id="88685-122">*RelatedColumn*</span><span class="sxs-lookup"><span data-stu-id="88685-122">*RelatedColumn*</span></span>

  - <span data-ttu-id="88685-p104">Facultatif. Valeur de type **String** qui spécifie le nom de la colonne liée pour une clé étrangère. Le paramètre RelatedColumn correspond à la valeur de la propriété **Name** d'un objet **Column**.</span><span class="sxs-lookup"><span data-stu-id="88685-p104">Optional. A **String** value that specifies the name of the related column for a foreign key. The RelatedColumn parameter corresponds to the value of the **Name** property of a **Column** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="88685-126">Notes</span><span class="sxs-lookup"><span data-stu-id="88685-126">Remarks</span></span>

<span data-ttu-id="88685-127">Le paramètre *Columns* peut prendre soit le nom d’une colonne ou un tableau de noms de colonne.</span><span class="sxs-lookup"><span data-stu-id="88685-127">The *Columns* parameter can take either the name of a column or an array of column names.</span></span>

