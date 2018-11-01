---
title: AppendChunk, méthode (ADO)
TOCTitle: AppendChunk Method (ADO)
ms:assetid: 3fa931a3-2cd7-a3b0-a750-40e18bc9937e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249179(v=office.15)
ms:contentKeyID: 48544405
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3e13ebd5d222bc765fe2e38198588274508baa4a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881936"
---
# <a name="appendchunk-method-ado"></a><span data-ttu-id="aa941-102">AppendChunk, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="aa941-102">AppendChunk Method (ADO)</span></span>


<span data-ttu-id="aa941-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="aa941-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="aa941-104">Cette méthode ajoute des données à un objet [Field](field-object-ado.md) de données binaires ou de texte volumineux ou à un objet [Parameter](parameter-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="aa941-104">Appends data to a large text or binary data [Field](field-object-ado.md), or to a [Parameter](parameter-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa941-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aa941-105">Syntax</span></span>

<span data-ttu-id="aa941-106">*objet.* AppendChunk *données*</span><span class="sxs-lookup"><span data-stu-id="aa941-106">*object.* AppendChunk *Data*</span></span>

## <a name="parameters"></a><span data-ttu-id="aa941-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aa941-107">Parameters</span></span>

  - <span data-ttu-id="aa941-108">*object*</span><span class="sxs-lookup"><span data-stu-id="aa941-108">*object*</span></span>

  - <span data-ttu-id="aa941-109">Objet **Field** ou **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="aa941-109">A **Field** or **Parameter** object.</span></span>

  - <span data-ttu-id="aa941-110">*Data*</span><span class="sxs-lookup"><span data-stu-id="aa941-110">*Data*</span></span>

  - <span data-ttu-id="aa941-111">**Variant** contenant les données à ajouter à l'objet.</span><span class="sxs-lookup"><span data-stu-id="aa941-111">A **Variant** that contains the data to append to the object.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa941-112">Notes</span><span class="sxs-lookup"><span data-stu-id="aa941-112">Remarks</span></span>

<span data-ttu-id="aa941-113">Utilisez la méthode **AppendChunk** sur un objet **Field** ou **Parameter** à remplir avec des données binaires longues ou caractères.</span><span class="sxs-lookup"><span data-stu-id="aa941-113">Use the **AppendChunk** method on a **Field** or **Parameter** object to fill it with long binary or character data.</span></span> <span data-ttu-id="aa941-114">Si vous manquez de mémoire système, vous pouvez utiliser la méthode **AppendChunk** pour manipuler une partie des valeurs longues plutôt que leur totalité.</span><span class="sxs-lookup"><span data-stu-id="aa941-114">In situations where system memory is limited, you can use the **AppendChunk** method to manipulate long values in portions rather than in their entirety.</span></span>

<span data-ttu-id="aa941-115">**Champ**</span><span class="sxs-lookup"><span data-stu-id="aa941-115">**Field**</span></span>

<span data-ttu-id="aa941-116">Si le bit **adFldLong** de la propriété [Attributes](attributes-property-ado.md) d'un objet **Field** a la valeur true, vous pouvez appliquer la méthode **AppendChunk** à ce champ.</span><span class="sxs-lookup"><span data-stu-id="aa941-116">If the **adFldLong** bit in the [Attributes](attributes-property-ado.md) property of a **Field** object is set to true, you can use the **AppendChunk** method for that field.</span></span>

<span data-ttu-id="aa941-p102">La première invocation de la méthode **AppendChunk** sur un objet **Field** écrit les données dans le champ en écrasant toute donnée existante. Les invocations suivantes de **AppendChunk** s'ajoutent aux données existantes. Si vous ajoutez des données à un champ, puis définissez ou lisez la valeur d'un autre champ de l'enregistrement actif, ADO suppose que vous avez terminé l'ajout de données dans le premier champ. Si vous invoquez à nouveau la méthode **AppendChunk** sur le premier champ, ADO interprète l'invocation comme une nouvelle opération **AppendChunk** et écrase les données existantes. L'accès à des champs d'autres objets [Recordset](recordset-object-ado.md) non identiques au premier objet **Recordset** n'interrompt pas les opérations **AppendChunk**.</span><span class="sxs-lookup"><span data-stu-id="aa941-p102">The first **AppendChunk** call on a **Field** object writes data to the field, overwriting any existing data. Subsequent **AppendChunk** calls add to existing data. If you are appending data to one field and then you set or read the value of another field in the current record, ADO assumes that you are finished appending data to the first field. If you call the **AppendChunk** method on the first field again, ADO interprets the call as a new **AppendChunk** operation and overwrites the existing data. Accessing fields in other [Recordset](recordset-object-ado.md) objects that are not clones of the first **Recordset** object will not disrupt **AppendChunk** operations.</span></span>

<span data-ttu-id="aa941-122">S'il n'existe pas d'enregistrement actif lorsque vous appelez la méthode **AppendChunk** sur un objet **Field**, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="aa941-122">If there is no current record when you call **AppendChunk** on a **Field** object, an error occurs.</span></span>


> [!NOTE]
> <span data-ttu-id="aa941-p103">[!REMARQUE] La méthode **AppendChunk** ne fonctionne pas sur les objets **Field** d'un objet [Record](record-object-ado.md) ; elle n'exécute aucune opération et génère une erreur d'exécution.</span><span class="sxs-lookup"><span data-stu-id="aa941-p103">The **AppendChunk** method does not operate on **Field** objects of a [Record](record-object-ado.md) object. It does not perform any operation and will produce a run-time error.</span></span>



<span data-ttu-id="aa941-125">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="aa941-125">**Parameter**</span></span>

<span data-ttu-id="aa941-126">Si le bit **adParamLong** de la propriété **Attributes** d'un objet **Parameter** a la valeur true, vous pouvez utiliser la méthode **AppendChunk** pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="aa941-126">If the **adParamLong** bit in the **Attributes** property of a **Parameter** object is set to true, you can use the **AppendChunk** method for that parameter.</span></span>

<span data-ttu-id="aa941-127">Le premier appel **AppendChunk** sur un objet **Parameter** écrit des données dans ce paramètre en remplaçant les données existantes.</span><span class="sxs-lookup"><span data-stu-id="aa941-127">The first **AppendChunk** call on a **Parameter** object writes data to the parameter, overwriting any existing data.</span></span> <span data-ttu-id="aa941-128">Les appels suivants **AppendChunk** sur un objet **Parameter** ajoutent paramètre aux données existantes.</span><span class="sxs-lookup"><span data-stu-id="aa941-128">Subsequent **AppendChunk** calls on a **Parameter** object add to existing parameter data.</span></span> <span data-ttu-id="aa941-129">Un appel à **AppendChunk** qui passe une valeur null annule toutes les données de paramètre.</span><span class="sxs-lookup"><span data-stu-id="aa941-129">An **AppendChunk** call that passes a null value discards all of the parameter data.</span></span>

