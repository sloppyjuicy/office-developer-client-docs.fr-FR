---
title: Close, méthode (ADO MD)
TOCTitle: Close Method (ADO MD)
ms:assetid: 683788b0-0a96-a165-6b49-8d7036850756
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249406(v=office.15)
ms:contentKeyID: 48545382
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 28c5ff23470015c9b40c996a1eb5b60f74766da3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888789"
---
# <a name="close-method-ado-md"></a><span data-ttu-id="d158a-102">Close, méthode (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="d158a-102">Close Method (ADO MD)</span></span>


<span data-ttu-id="d158a-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d158a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d158a-104">Ferme un ensemble de cellules ouvert.</span><span class="sxs-lookup"><span data-stu-id="d158a-104">Closes an open cellset.</span></span>

## <a name="syntax"></a><span data-ttu-id="d158a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d158a-105">Syntax</span></span>

<span data-ttu-id="d158a-106">*Ensemble de cellules*. Fermer</span><span class="sxs-lookup"><span data-stu-id="d158a-106">*Cellset*.Close</span></span>

## <a name="remarks"></a><span data-ttu-id="d158a-107">Notes</span><span class="sxs-lookup"><span data-stu-id="d158a-107">Remarks</span></span>

<span data-ttu-id="d158a-p101">Lorsque vous fermez un objet **Cellset** à l'aide de la méthode [Close](cellset-object-ado-md.md), vous libérez les données associées, ainsi que celles de tous les objets [Cell](cell-object-ado-md.md), [Axis](axis-object-ado-md.md), [Position](position-object-ado-md.md) ou [Member](member-object-ado-md.md) liés. La fermeture d'un objet **Cellset** n'engendre pas sa suppression de la mémoire. Vous pourrez modifier les paramètres de ses propriétés et le rouvrir ultérieurement. Pour supprimer définitivement un objet de la mémoire, affectez à la variable objet la valeur **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="d158a-p101">Using the **Close** method to close a [Cellset](cellset-object-ado-md.md) object will release the associated data, including data in any related [Cell](cell-object-ado-md.md), [Axis](axis-object-ado-md.md), [Position](position-object-ado-md.md), or [Member](member-object-ado-md.md) objects. Closing a **Cellset** does not remove it from memory; you can change its property settings and open it again later. To completely eliminate an object from memory, set the object variable to **Nothing**.</span></span>

<span data-ttu-id="d158a-p102">Par la suite, vous pourrez appeler la méthode [Open](open-method-ado-md.md) pour rouvrir l'objet **Cellset** à l'aide de la même chaîne source ou d'une autre. Lorsque l'objet **Cellset** est fermé, une erreur se produit si vous tentez d'extraire une propriété ou d'appeler une méthode qui fait référence aux données ou métadonnées sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="d158a-p102">You can later call the [Open](open-method-ado-md.md) method to reopen the **Cellset** using the same or another source string. While the **Cellset** object is closed, retrieving any properties or calling any methods that reference the underlying data or metadata generates an error.</span></span>

