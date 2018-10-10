---
title: Append, méthode (Colonnes ADOX)
TOCTitle: Append Method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1f64f3b04df989348173ad2fc975dcefbd1114b2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469553"
---
# <a name="append-method-adox-columns"></a><span data-ttu-id="c08e8-102">Append, méthode (Colonnes ADOX)</span><span class="sxs-lookup"><span data-stu-id="c08e8-102">Append Method (ADOX Columns)</span></span>


<span data-ttu-id="c08e8-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c08e8-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c08e8-104">Ajoute un nouvel objet [Column](column-object-adox.md) à la collection [Columns](columns-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="c08e8-104">Adds a new [Column](column-object-adox.md) object to the [Columns](columns-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c08e8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c08e8-105">Syntax</span></span>

<span data-ttu-id="c08e8-106">*Colonnes*.</span><span class="sxs-lookup"><span data-stu-id="c08e8-106">*Columns*.</span></span> <span data-ttu-id="c08e8-107">Ajouter la*colonne* \[,*Type* \] \[,*DefinedSize*\]</span><span class="sxs-lookup"><span data-stu-id="c08e8-107">Append*Column* \[,*Type*\] \[,*DefinedSize*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="c08e8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c08e8-108">Parameters</span></span>

  - <span data-ttu-id="c08e8-109">*Column*</span><span class="sxs-lookup"><span data-stu-id="c08e8-109">*Column*</span></span>

  - <span data-ttu-id="c08e8-110">Objet **Column** à ajouter ou nom de la colonne à créer et à ajouter.</span><span class="sxs-lookup"><span data-stu-id="c08e8-110">The **Column** object to append or the name of the column to create and append.</span></span>

  - <span data-ttu-id="c08e8-111">*Type*</span><span class="sxs-lookup"><span data-stu-id="c08e8-111">*Type*</span></span>

  - <span data-ttu-id="c08e8-112">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="c08e8-112">Optional.</span></span> <span data-ttu-id="c08e8-113">Valeur de type **long** qui spécifie le type de données de la colonne.</span><span class="sxs-lookup"><span data-stu-id="c08e8-113">A **Long** value that specifies the data type of the column.</span></span> <span data-ttu-id="c08e8-114">Le paramètre *Type* correspond à la propriété [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) d’un objet **Column** .</span><span class="sxs-lookup"><span data-stu-id="c08e8-114">The *Type* parameter corresponds to the [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) property of a **Column** object.</span></span>

  - <span data-ttu-id="c08e8-115">*DefinedSize*</span><span class="sxs-lookup"><span data-stu-id="c08e8-115">*DefinedSize*</span></span>

  - <span data-ttu-id="c08e8-116">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="c08e8-116">Optional.</span></span> <span data-ttu-id="c08e8-117">Valeur de type **long** qui spécifie la taille de la colonne.</span><span class="sxs-lookup"><span data-stu-id="c08e8-117">A **Long** value that specifies the size of the column.</span></span> <span data-ttu-id="c08e8-118">Le paramètre *DefinedSize* correspond à la propriété [DefinedSize](definedsize-property-adox.md) d’un objet **Column** .</span><span class="sxs-lookup"><span data-stu-id="c08e8-118">The *DefinedSize* parameter corresponds to the [DefinedSize](definedsize-property-adox.md) property of a **Column** object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="c08e8-119">[!REMARQUE] Une erreur survient lors de l'ajout d'une <STRONG>colonne</STRONG> à la collection <STRONG>Columns</STRONG> d'un <A href="index-object-adox.md">index</A> si la <STRONG>colonne</STRONG> n'existe pas dans une <A href="table-object-adox.md">table</A> déjà ajoutée à la collection <A href="tables-collection-adox.md">Tables</A>.</span><span class="sxs-lookup"><span data-stu-id="c08e8-119">An error will occur when appending a <STRONG>Column</STRONG> to the <STRONG>Columns</STRONG> collection of an <A href="index-object-adox.md">Index</A> if the <STRONG>Column</STRONG> does not exist in a <A href="table-object-adox.md">Table</A> that is already appended to the <A href="tables-collection-adox.md">Tables</A> collection.</span></span></P>


