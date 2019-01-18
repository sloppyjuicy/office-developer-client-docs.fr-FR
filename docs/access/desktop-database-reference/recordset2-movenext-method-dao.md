---
title: Méthode Recordset2.MoveNext (DAO)
TOCTitle: MoveNext Method
ms:assetid: 0eeb917e-f76a-03ec-9e1e-aa8d501db031
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845265(v=office.15)
ms:contentKeyID: 48543254
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6f500578182aac74b608117ee4105a6b657057df
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719910"
---
# <a name="recordset2movenext-method-dao"></a><span data-ttu-id="9f27a-102">Méthode Recordset2.MoveNext (DAO)</span><span class="sxs-lookup"><span data-stu-id="9f27a-102">Recordset2.MoveNext method (DAO)</span></span>


<span data-ttu-id="9f27a-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9f27a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9f27a-104">Se déplace jusqu'à l'enregistrement suivant dans un objet **Recordset** spécifié et définit cet enregistrement comme l'enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="9f27a-104">Moves to the next record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f27a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9f27a-105">Syntax</span></span>

<span data-ttu-id="9f27a-106">*expression* . MoveNext</span><span class="sxs-lookup"><span data-stu-id="9f27a-106">*expression* .MoveNext</span></span>

<span data-ttu-id="9f27a-107">*expression* Variable qui représente un objet **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="9f27a-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f27a-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="9f27a-108">Remarks</span></span>

<span data-ttu-id="9f27a-109">Utilisez les méthodes **Move** pour vous déplacer entre les enregistrements sans appliquer de condition.</span><span class="sxs-lookup"><span data-stu-id="9f27a-109">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="9f27a-p101">Si vous modifiez l'enregistrement actif, veillez à utiliser la méthode **Update** pour enregistrer les modifications avant de passer à un autre enregistrement. Si vous accédez à un autre enregistrement alors que vous effectuez une mise à jour, les modifications seront perdues sans notification.</span><span class="sxs-lookup"><span data-stu-id="9f27a-p101">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record. If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="9f27a-p102">Lorsque vous ouvrez un objet **Recordset**, le premier enregistrement est actif et la propriété **BOF** prend la valeur **False**. Si l'objet **Recordset** ne contient pas d'enregistrement, la propriété **BOF** prend la valeur **True**, et il n'y a pas d'enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="9f27a-p102">When you open a **Recordset**, the first record is current and the **BOF** property is **False**. If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="9f27a-p103">Si vous utilisez **MoveNext** lorsque le dernier enregistrement est l'enregistrement actif, la propriété **EOF** prend la valeur **True**, et il n'y a pas d'enregistrement actif. Si vous utilisez de nouveau **MoveNext**, une erreur se produit et **EOF** conserve la valeur **True**.</span><span class="sxs-lookup"><span data-stu-id="9f27a-p103">If you use **MoveNext** when the last record is current, the **EOF** property is **True**, and there is no current record. If you use **MoveNext** again, an error occurs, and **EOF** remains **True**.</span></span>

<span data-ttu-id="9f27a-116">Si le jeu d’enregistrements fait référence à un **objet Recordset** de type table (espaces de travail Microsoft Access uniquement), le déplacement suit l’index actuel.</span><span class="sxs-lookup"><span data-stu-id="9f27a-116">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="9f27a-117">Vous pouvez définir l'index actif à l'aide de la propriété **Index**.</span><span class="sxs-lookup"><span data-stu-id="9f27a-117">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="9f27a-118">Si vous ne définissez pas l'index actif, l'ordre des enregistrements renvoyés est indéfini.</span><span class="sxs-lookup"><span data-stu-id="9f27a-118">If you don't set the current index, the order of returned records is undefined.</span></span>

<span data-ttu-id="9f27a-119">Vous ne pouvez pas utiliser les méthodes **MoveFirst**, **MoveLast**et **MovePrevious** sur un objet **Recordset** de type avant uniquement.</span><span class="sxs-lookup"><span data-stu-id="9f27a-119">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="9f27a-120">Pour déplacer la position de l'enregistrement actif dans un objet **Recordset** d'un objet d'un nombre d'enregistrements spécifique vers l'avant ou l'arrière, utilisez la méthode **Move**.</span><span class="sxs-lookup"><span data-stu-id="9f27a-120">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

