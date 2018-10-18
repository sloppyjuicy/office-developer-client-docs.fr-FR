---
title: GetChildren, méthode (ADO)
TOCTitle: GetChildren Method (ADO)
ms:assetid: 998cf640-ffc7-51e1-4d1e-4797f7cdea4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249687(v=office.15)
ms:contentKeyID: 48546515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 06474b6c4ecb29388367f8ceac7c7676002e1384
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602657"
---
# <a name="getchildren-method-ado"></a><span data-ttu-id="24b00-102">GetChildren, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="24b00-102">GetChildren Method (ADO)</span></span>


<span data-ttu-id="24b00-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="24b00-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="24b00-104">Retourne un objet [Recordset](recordset-object-ado.md) dont les lignes représentent les enfants d'un objet [Record](record-object-ado.md) d'une collection.</span><span class="sxs-lookup"><span data-stu-id="24b00-104">Returns a [Recordset](recordset-object-ado.md) whose rows represent the children of a collection [Record](record-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="24b00-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="24b00-105">Syntax</span></span>

<span data-ttu-id="24b00-106">**La valeur** *jeu d’enregistrements*  =  *enregistrement*. GetChildren</span><span class="sxs-lookup"><span data-stu-id="24b00-106">**Set** *recordset* = *record*.GetChildren</span></span>

<span data-ttu-id="24b00-107"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="24b00-107"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="24b00-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="24b00-108">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="24b00-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="24b00-109">Return value</span></span>
>>>>>>> <span data-ttu-id="24b00-110">master</span><span class="sxs-lookup"><span data-stu-id="24b00-110">master</span></span>

<span data-ttu-id="24b00-p101">Objet **Recordset** dont chaque ligne représente un enfant de l'objet **Record** actif. Par exemple, les enfants d'un objet **Record** qui représente un répertoire, sont les fichiers et sous-répertoires contenus dans le répertoire parent.</span><span class="sxs-lookup"><span data-stu-id="24b00-p101">A **Recordset** object for which each row represents a child of the current **Record** object. For example, the children of a **Record** that represents a directory would be the files and subdirectories contained within the parent directory.</span></span>

## <a name="remarks"></a><span data-ttu-id="24b00-113">Notes</span><span class="sxs-lookup"><span data-stu-id="24b00-113">Remarks</span></span>

<span data-ttu-id="24b00-p102">Le fournisseur détermine les colonnes qui figureront dans l'objet **Recordset** retourné. Par exemple, un fournisseur de source de documents retourne toujours un objet **Recordset** de ressource.</span><span class="sxs-lookup"><span data-stu-id="24b00-p102">The provider determines what columns exist in the returned **Recordset**. For example, a document source provider always returns a resource **Recordset**.</span></span>

