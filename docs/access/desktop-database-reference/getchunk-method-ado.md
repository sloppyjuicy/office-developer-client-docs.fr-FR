---
title: GetChunk, méthode (ADO)
TOCTitle: GetChunk Method (ADO)
ms:assetid: 1ef1c37a-8453-8d3b-251a-d16e0d519fd7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248979(v=office.15)
ms:contentKeyID: 48543629
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 77726a20decd8029d4ced8198ac1bb622a1c6b11
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881516"
---
# <a name="getchunk-method-ado"></a><span data-ttu-id="f4f99-102">GetChunk, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="f4f99-102">GetChunk Method (ADO)</span></span>


<span data-ttu-id="f4f99-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f4f99-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="f4f99-104">Retourne l'ensemble ou une partie du contenu d'un objet [Field](field-object-ado.md) volumineux contenant du texte ou des données binaires.</span><span class="sxs-lookup"><span data-stu-id="f4f99-104">Returns all, or a portion, of the contents of a large text or binary data [Field](field-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4f99-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f4f99-105">Syntax</span></span>

<span data-ttu-id="f4f99-106">*variable* = *champ*. GetChunk (*taille* )</span><span class="sxs-lookup"><span data-stu-id="f4f99-106">*variable* = *field*.GetChunk(*Size* )</span></span>

## <a name="return-value"></a><span data-ttu-id="f4f99-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f4f99-107">Return value</span></span>

<span data-ttu-id="f4f99-108">Retourne une valeur de type **Variant**.</span><span class="sxs-lookup"><span data-stu-id="f4f99-108">Returns a **Variant**.</span></span>

## <a name="parameters"></a><span data-ttu-id="f4f99-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f4f99-109">Parameters</span></span>

  - <span data-ttu-id="f4f99-110">*Taille*</span><span class="sxs-lookup"><span data-stu-id="f4f99-110">*Size*</span></span>

  - <span data-ttu-id="f4f99-111">Expression de type **Long** égale au nombre d'octets ou de caractères que vous souhaitez récupérer.</span><span class="sxs-lookup"><span data-stu-id="f4f99-111">A **Long** expression that is equal to the number of bytes or characters that you want to retrieve.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4f99-112">Notes</span><span class="sxs-lookup"><span data-stu-id="f4f99-112">Remarks</span></span>

<span data-ttu-id="f4f99-p101">Utilisez la méthode **GetChunk** sur un objet **Field** pour récupérer une partie ou l'ensemble de ses données binaires ou de caractères de type long. Dans les cas où la mémoire système est limitée, vous pouvez utiliser la méthode **GetChunk** pour manipuler des parties de données de type long par partie au lieu de l'intégralité de ces données.</span><span class="sxs-lookup"><span data-stu-id="f4f99-p101">Use the **GetChunk** method on a **Field** object to retrieve part or all of its long binary or character data. In situations where system memory is limited, you can use the **GetChunk** method to manipulate long values in portions, rather than in their entirety.</span></span>

<span data-ttu-id="f4f99-p102">Les données renvoyées par une invocation **GetChunk** sont affectées à *variable*. Si la *taille* est supérieure aux données restantes, la méthode **GetChunk** renvoie uniquement les données restantes sans compléter les *variables* avec des espaces vides. Si le champ est vide, la méthode **GetChunk** renvoie une valeur nulle.</span><span class="sxs-lookup"><span data-stu-id="f4f99-p102">The data that a **GetChunk** call returns is assigned to *variable*. If *Size* is greater than the remaining data, the **GetChunk** method returns only the remaining data without padding *variable* with empty spaces. If the field is empty, the **GetChunk** method returns a null value.</span></span>

<span data-ttu-id="f4f99-p103">Chaque appel à **GetChunk** ultérieur récupère les données à partir de l'emplacement où l'appel à **GetChunk** précédent s'est arrêté. Toutefois, si vous récupérez des données d'un champ et qu'ensuite vous définissez ou lisez la valeur d'un autre champ dans l'enregistrement actif, ADO suppose que vous avez terminé de récupérer les données du premier champ. Si vous appelez de nouveau la méthode **GetChunk** sur le premier champ, ADO interprète l'appel comme une nouvelle opération **GetChunk** et recommence sa lecture à partir du début des données. L'accès à d'autres champs d'objets [Recordset](recordset-object-ado.md) qui ne sont pas des clones du premier objet **Recordset** ne perturbent pas les opérations **GetChunk**.</span><span class="sxs-lookup"><span data-stu-id="f4f99-p103">Each subsequent **GetChunk** call retrieves data starting from where the previous **GetChunk** call left off. However, if you are retrieving data from one field and then you set or read the value of another field in the current record, ADO assumes you have finished retrieving data from the first field. If you call the **GetChunk** method on the first field again, ADO interprets the call as a new **GetChunk** operation and starts reading from the beginning of the data. Accessing fields in other [Recordset](recordset-object-ado.md) objects that are not clones of the first **Recordset** object will not disrupt **GetChunk** operations.</span></span>

<span data-ttu-id="f4f99-122">Si le bit **adFldLong** de la propriété [Attributes](attributes-property-ado.md) d'un objet **Field** a la valeur **True**, vous pouvez utiliser la méthode **GetChunk** pour ce champ.</span><span class="sxs-lookup"><span data-stu-id="f4f99-122">If the **adFldLong** bit in the [Attributes](attributes-property-ado.md) property of a **Field** object is set to **True**, you can use the **GetChunk** method for that field.</span></span>

<span data-ttu-id="f4f99-123">S'il n'existe aucun enregistrement actif lorsque vous utilisez la méthode **GetChunk** sur un objet **Field**, l'erreur 3021 (aucun enregistrement en cours) se produit.</span><span class="sxs-lookup"><span data-stu-id="f4f99-123">If there is no current record when you use the **GetChunk** method on a **Field** object, error 3021 (no current record) occurs.</span></span>


> [!NOTE]
> <P><span data-ttu-id="f4f99-p104">[!REMARQUE] La méthode <STRONG>GetChunk</STRONG> ne fonctionne pas sur les objets <STRONG>Field</STRONG> d'un objet <A href="record-object-ado.md">Record</A>. Elle n'exécute aucune opération et génère une erreur d'exécution.</span><span class="sxs-lookup"><span data-stu-id="f4f99-p104">The <STRONG>GetChunk</STRONG> method does not operate on <STRONG>Field</STRONG> objects of a <A href="record-object-ado.md">Record</A> object. It does not perform any operation and will produce a run-time error.</span></span></P>


