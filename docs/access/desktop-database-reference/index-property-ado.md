---
title: Index, propriété (ADO)
TOCTitle: Index property (ADO)
ms:assetid: 4cc00521-dcb4-19b2-2174-6e0e9bd42e62
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249241(v=office.15)
ms:contentKeyID: 48544715
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7d436ec9102c4c75688b6c6ac973ca85e8c280d0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291705"
---
# <a name="index-property-ado"></a><span data-ttu-id="f0295-102">Index, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="f0295-102">Index property (ADO)</span></span>


<span data-ttu-id="f0295-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f0295-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f0295-104">Indique le nom de l'index utilisé pour un objet [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f0295-104">Indicates the name of the index currently in effect for a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="f0295-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="f0295-105">Settings and return values</span></span>

<span data-ttu-id="f0295-106">Définit ou renvoie une valeur **String** indiquant le nom de l'index.</span><span class="sxs-lookup"><span data-stu-id="f0295-106">Sets or returns a **String** value, which is the name of the index.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0295-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="f0295-107">Remarks</span></span>

<span data-ttu-id="f0295-p101">L'index nommé par la propriété **Index** doit avoir été préalablement déclaré sur la table de base sous-jacente de l'objet **Recordset**. C'est-à-dire que l'index doit avoir été déclaré par programmation soit sous forme d'objet [Index](index-object-adox.md) ADOX, soit au moment de la création de la table de base.</span><span class="sxs-lookup"><span data-stu-id="f0295-p101">The index named by the **Index** property must have previously been declared on the base table underlying the **Recordset** object. That is, the index must have been declared programmatically either as an ADOX [Index](index-object-adox.md) object, or when the base table was created.</span></span>

<span data-ttu-id="f0295-p102">Une erreur d'exécution est générée si l'index ne peut pas être défini. La propriété **Index** ne peut pas être définie :</span><span class="sxs-lookup"><span data-stu-id="f0295-p102">A run-time error will occur if the index cannot be set. The **Index** property cannot be set:</span></span>

  - <span data-ttu-id="f0295-112">Dans un gestionnaire d'événements [WillChangeRecordset](willchangerecordset-and-recordsetchangecomplete-events-ado.md) ou **RecordsetChangeComplete**.</span><span class="sxs-lookup"><span data-stu-id="f0295-112">Within a [WillChangeRecordset](willchangerecordset-and-recordsetchangecomplete-events-ado.md) or **RecordsetChangeComplete** event handler.</span></span>

  - <span data-ttu-id="f0295-113">Si le **Recordset** exécute encore une opération (ce qui peut être déterminé par la propriété [State](state-property-ado.md)).</span><span class="sxs-lookup"><span data-stu-id="f0295-113">If the **Recordset** is still executing an operation (which can be determined by the [State](state-property-ado.md) property).</span></span>

  - <span data-ttu-id="f0295-114">Si un filtre a été défini sur le **Recordset** par la propriété [Filter](filter-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f0295-114">If a filter has been set on the **Recordset** with the [Filter](filter-property-ado.md) property.</span></span>

<span data-ttu-id="f0295-115">La propriété **Index** peut toujours être définie avec succès si le **Recordset** est fermé, mais le **Recordset** ne s'ouvre pas correctement (ou l'index n'est pas utilisable) si le fournisseur sous-jacent ne prend pas en charge les index.</span><span class="sxs-lookup"><span data-stu-id="f0295-115">The **Index** property can always be set successfully if the **Recordset** is closed, but the **Recordset** will not open successfully, or the index will not be usable, if the underlying provider does not support indexes.</span></span>

<span data-ttu-id="f0295-p103">Si l'index peut être défini, il se peut que la position de la ligne active soit modifiée. Cela provoque la mise à jour de la propriété [AbsolutePosition](absoluteposition-property-ado.md) et la génération des événements **WillChangeRecordset**, **RecordsetChangeComplete**, [WillMove](willmove-and-movecomplete-events-ado.md) et [MoveComplete](willmove-and-movecomplete-events-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f0295-p103">If the index can be set, the current row position may change. This will cause an update to the [AbsolutePosition](absoluteposition-property-ado.md) property, and the generation of **WillChangeRecordset**, **RecordsetChangeComplete**, [WillMove](willmove-and-movecomplete-events-ado.md), and [MoveComplete](willmove-and-movecomplete-events-ado.md) events.</span></span>

<span data-ttu-id="f0295-p104">Si l'index peut être défini et que la valeur de la propriété [LockType](locktype-property-ado.md) est **adLockPessimistic** ou **adLockOptimistic**, une opération [UpdateBatch](updatebatch-method-ado.md) implicite est réalisée. Cela libère le groupe actuel et le groupe attribué. S'il existe un filtre, il est libéré, et la ligne active devient la première ligne du **Recordset** réorganisé.</span><span class="sxs-lookup"><span data-stu-id="f0295-p104">If the index can be set and the [LockType](locktype-property-ado.md) property is **adLockPessimistic** or **adLockOptimistic**, then an implicit [UpdateBatch](updatebatch-method-ado.md) operation is performed. This releases the current and affected groups. Any existing filter is released, and the current row position is changed to the first row of the reordered **Recordset**.</span></span>

<span data-ttu-id="f0295-121">La propriété **Index** est utilisée en association avec la méthode [Seek](seek-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f0295-121">The **Index** property is used in conjunction with the [Seek](seek-method-ado.md) method.</span></span> <span data-ttu-id="f0295-122">Si le fournisseur sous-jacent ne prend pas en charge la propriété **Index** (et donc la méthode **Seek** ), pensez à utiliser plutôt la méthode [Find](find-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f0295-122">If the underlying provider does not support the **Index** property, and thus the **Seek** method, consider using the [Find](find-method-ado.md) method instead.</span></span> <span data-ttu-id="f0295-123">Déterminez si **l’objet Recordset** prend en charge les index avec la [méthode Supports](supports-method-ado.md)**(adIndex).**</span><span class="sxs-lookup"><span data-stu-id="f0295-123">Determine whether the **Recordset** object supports indexes with the [Supports](supports-method-ado.md)**(adIndex)** method.</span></span>

<span data-ttu-id="f0295-124">La propriété **Index** intégrée n'a aucun rapport avec la propriété [Optimize](optimize-property-dynamic-ado.md) dynamique, même si toutes deux portent sur les index.</span><span class="sxs-lookup"><span data-stu-id="f0295-124">The built-in **Index** property is not related to the dynamic [Optimize](optimize-property-dynamic-ado.md) property, although they both deal with indexes.</span></span>

