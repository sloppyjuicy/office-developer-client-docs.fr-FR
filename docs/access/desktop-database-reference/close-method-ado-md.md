---
title: Close, méthode (ADO MD)
TOCTitle: Close method (ADO MD)
ms:assetid: 683788b0-0a96-a165-6b49-8d7036850756
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249406(v=office.15)
ms:contentKeyID: 48545382
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 609069d04124146f311166e3ae56d8d6a793675b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709830"
---
# <a name="close-method-ado-md"></a><span data-ttu-id="ba572-102">Close, méthode (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="ba572-102">Close method (ADO MD)</span></span>


<span data-ttu-id="ba572-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ba572-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ba572-104">Ferme un ensemble de cellules ouvert.</span><span class="sxs-lookup"><span data-stu-id="ba572-104">Closes an open cellset.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba572-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ba572-105">Syntax</span></span>

<span data-ttu-id="ba572-106">*Ensemble de cellules*. Fermer</span><span class="sxs-lookup"><span data-stu-id="ba572-106">*Cellset*.Close</span></span>

## <a name="remarks"></a><span data-ttu-id="ba572-107">Notes</span><span class="sxs-lookup"><span data-stu-id="ba572-107">Remarks</span></span>

<span data-ttu-id="ba572-p101">Lorsque vous fermez un objet **Cellset** à l'aide de la méthode [Close](cellset-object-ado-md.md), vous libérez les données associées, ainsi que celles de tous les objets [Cell](cell-object-ado-md.md), [Axis](axis-object-ado-md.md), [Position](position-object-ado-md.md) ou [Member](member-object-ado-md.md) liés. La fermeture d'un objet **Cellset** n'engendre pas sa suppression de la mémoire. Vous pourrez modifier les paramètres de ses propriétés et le rouvrir ultérieurement. Pour supprimer définitivement un objet de la mémoire, affectez à la variable objet la valeur **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="ba572-p101">Using the **Close** method to close a [Cellset](cellset-object-ado-md.md) object will release the associated data, including data in any related [Cell](cell-object-ado-md.md), [Axis](axis-object-ado-md.md), [Position](position-object-ado-md.md), or [Member](member-object-ado-md.md) objects. Closing a **Cellset** does not remove it from memory; you can change its property settings and open it again later. To completely eliminate an object from memory, set the object variable to **Nothing**.</span></span>

<span data-ttu-id="ba572-p102">Par la suite, vous pourrez appeler la méthode [Open](open-method-ado-md.md) pour rouvrir l'objet **Cellset** à l'aide de la même chaîne source ou d'une autre. Lorsque l'objet **Cellset** est fermé, une erreur se produit si vous tentez d'extraire une propriété ou d'appeler une méthode qui fait référence aux données ou métadonnées sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="ba572-p102">You can later call the [Open](open-method-ado-md.md) method to reopen the **Cellset** using the same or another source string. While the **Cellset** object is closed, retrieving any properties or calling any methods that reference the underlying data or metadata generates an error.</span></span>

