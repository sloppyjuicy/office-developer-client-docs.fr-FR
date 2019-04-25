---
title: Recordset.MoveNext, méthode (DAO)
TOCTitle: MoveNext Method
ms:assetid: 0a1315cf-92f8-b8ef-1542-081e8c2d5be0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845090(v=office.15)
ms:contentKeyID: 48543142
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 1b0ebe0edcfcbfac5942fc83a3ff1f99eddfea7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300342"
---
# <a name="recordsetmovenext-method-dao"></a><span data-ttu-id="524e8-102">Recordset.MoveNext, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="524e8-102">Recordset.MoveNext Method (DAO)</span></span>


<span data-ttu-id="524e8-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="524e8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="524e8-104">Passe à l’enregistrement suivant dans un objet **Recordset** spécifié et en fait l’enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="524e8-104">Moves to the next record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="524e8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="524e8-105">Syntax</span></span>

<span data-ttu-id="524e8-106">*expression* .MoveNext</span><span class="sxs-lookup"><span data-stu-id="524e8-106">expression  . MoveNext</span></span>

<span data-ttu-id="524e8-107">*expression* Variable représentant un objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="524e8-107">*expression*  A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="524e8-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="524e8-108">Remarks</span></span>

<span data-ttu-id="524e8-109">La méthode **Move** permet de passer d’un enregistrement à un autre sans appliquer de condition.</span><span class="sxs-lookup"><span data-stu-id="524e8-109">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="524e8-p101">Si vous modifiez l’enregistrement actif, utilisez la méthode **Update** pour enregistrer les modifications avant de passer à un autre enregistrement. Si vous passez à un autre enregistrement sans procéder à la mise à jour, vos modifications seront perdues sans avertissement.</span><span class="sxs-lookup"><span data-stu-id="524e8-p101">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record. If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="524e8-p102">Lorsque vous ouvrez un objet **Recordset**, le premier enregistrement est actif et la propriété **BOF** a la valeur **False**. Si l’objet **Recordset** ne contient pas d’enregistrements, la propriété **BOF** a la valeur **True** et aucun enregistrement n’est actif.</span><span class="sxs-lookup"><span data-stu-id="524e8-p102">When you open a **Recordset**, the first record is current and the **BOF** property is **False**. If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="524e8-p103">Si vous utilisez **MoveNext** lorsque le dernier enregistrement est à jour, la **EOF** propriété est **vrai**, et aucun enregistrement actif. Si vous utilisez **MoveNext** là encore, une erreur se produit, et **EOF** reste **vrai**.</span><span class="sxs-lookup"><span data-stu-id="524e8-p103">If you use **MoveNext** when the last record is current, the **EOF** property is **True**, and there is no current record. If you use **MoveNext** again, an error occurs, and **EOF** remains **True**.</span></span>

<span data-ttu-id="524e8-116">Si recordset fait référence à un objet **Recordset** de type table (espaces de travail Microsoft Access uniquement), le déplacement suit l’index actuel.</span><span class="sxs-lookup"><span data-stu-id="524e8-116">If  recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="524e8-117">Vous pouvez définir l’index en cours à l’aide de la **Index** propriété.</span><span class="sxs-lookup"><span data-stu-id="524e8-117">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="524e8-118">Si vous ne définissez l’index en cours, l’ordre des enregistrements renvoyés n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="524e8-118">If you don't set the current index, the order of returned records is undefined.</span></span>

<span data-ttu-id="524e8-119">Vous ne pouvez pas appliquer les méthodes **MoveFirst**, **MoveLast** et **MovePrevious** à un objet **Recordset** de type avant uniquement.</span><span class="sxs-lookup"><span data-stu-id="524e8-119">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="524e8-120">Pour faire avancer ou reculer l’enregistrement actif d’un certain nombre d’enregistrements dans un objet **Recordset**, utilisez la méthode **Move**.</span><span class="sxs-lookup"><span data-stu-id="524e8-120">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

