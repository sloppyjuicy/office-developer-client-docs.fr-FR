---
title: Close, méthode - ActiveX Data Objects (ADO)
TOCTitle: Close method (ADO)
ms:assetid: 26a7cced-ebeb-70be-f5de-96a35711bc37
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249029(v=office.15)
ms:contentKeyID: 48543818
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 269a782e85fab1e5dc47cd32f2e2c11306e11470
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720771"
---
# <a name="close-method-ado"></a><span data-ttu-id="edb51-102">Close, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="edb51-102">Close method (ADO)</span></span>


<span data-ttu-id="edb51-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="edb51-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="edb51-104">Ferme un objet ouvert, ainsi que tous les objets qui en dépendent.</span><span class="sxs-lookup"><span data-stu-id="edb51-104">Closes an open object and any dependent objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="edb51-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="edb51-105">Syntax</span></span>

<span data-ttu-id="edb51-106">*object*.Close</span><span class="sxs-lookup"><span data-stu-id="edb51-106">*object*.Close</span></span>

## <a name="remarks"></a><span data-ttu-id="edb51-107">Notes</span><span class="sxs-lookup"><span data-stu-id="edb51-107">Remarks</span></span>

<span data-ttu-id="edb51-108">Utilisez la méthode **Close** pour fermer un objet [Connection](connection-object-ado.md), [Record](record-object-ado.md), [Recordset](recordset-object-ado.md) ou [Stream](stream-object-ado.md) et libérer ainsi toutes les ressources système associées.</span><span class="sxs-lookup"><span data-stu-id="edb51-108">Use the **Close** method to close a [Connection](connection-object-ado.md), a [Record](record-object-ado.md), a [Recordset](recordset-object-ado.md), or a [Stream](stream-object-ado.md) object to free any associated system resources.</span></span> <span data-ttu-id="edb51-109">La fermeture d'un objet n'entraîne pas sa suppression de la mémoire ; vous pouvez modifier ses paramètres de propriété et le rouvrir ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="edb51-109">Closing an object does not remove it from memory; you can change its property settings and open it again later.</span></span> <span data-ttu-id="edb51-110">Pour supprimer définitivement un objet de la mémoire, définissez la variable d’objet sur *Nothing* (dans Visual Basic) après la fermeture de l’objet.</span><span class="sxs-lookup"><span data-stu-id="edb51-110">To completely eliminate an object from memory, set the object variable to *Nothing* (in Visual Basic) after closing the object.</span></span>

<span data-ttu-id="edb51-111">**Objet Connection**</span><span class="sxs-lookup"><span data-stu-id="edb51-111">**Connection**</span></span>

<span data-ttu-id="edb51-p102">Lorsque vous utilisez la méthode **Close** pour fermer un objet **Connection**, tous les objets **Recordset** actifs associés à cette connexion sont également fermés. Si un objet [Command](command-object-ado.md) est associé à l'objet **Connection** que vous fermez, il est conservé, mais il ne sera plus associé à l'objet **Connection**. En d'autres termes, sa propriété [ActiveConnection](activeconnection-property-ado.md) prendra la valeur **Nothing**. Par ailleurs, les paramètres définis par le fournisseur seront supprimés de la collection **Parameters** de l'objet [Command](parameters-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="edb51-p102">Using the **Close** method to close a **Connection** object also closes any active **Recordset** objects associated with the connection. A [Command](command-object-ado.md) object associated with the **Connection** object you are closing will persist, but it will no longer be associated with a **Connection** object; that is, its [ActiveConnection](activeconnection-property-ado.md) property will be set to **Nothing**. Also, the **Command** object's [Parameters](parameters-collection-ado.md) collection will be cleared of any provider-defined parameters.</span></span>

<span data-ttu-id="edb51-p103">Vous pouvez ensuite appeler la méthode [Open](open-method-ado-connection.md) pour rétablir la connexion à la même source de données ou à une source de données différente. Lorsque l'objet **Connection** est fermé, l'appel d'une méthode nécessitant une connexion ouverte à la source de données génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="edb51-p103">You can later call the [Open](open-method-ado-connection.md) method to re-establish the connection to the same, or another, data source. While the **Connection** object is closed, calling any methods that require an open connection to the data source generates an error.</span></span>

<span data-ttu-id="edb51-p104">Lorsque vous fermez un objet **Connection** alors que des objets **Recordset** sont ouverts sur la connexion, les modifications en attente dans tous les objets **Recordset** sont annulées. La fermeture explicite d'un objet **Connection** (par un appel de la méthode **Close** ) alors qu'une transaction est en cours génère une erreur. Si un objet **Connection** devient hors de portée lorsqu'une transaction est en cours, ADO restaure automatiquement la transaction.</span><span class="sxs-lookup"><span data-stu-id="edb51-p104">Closing a **Connection** object while there are open **Recordset** objects on the connection rolls back any pending changes in all of the **Recordset** objects. Explicitly closing a **Connection** object (calling the **Close** method) while a transaction is in progress generates an error. If a **Connection** object falls out of scope while a transaction is in progress, ADO automatically rolls back the transaction.</span></span>

<span data-ttu-id="edb51-120">Objets **Recordset, Record et Stream**</span><span class="sxs-lookup"><span data-stu-id="edb51-120">**Recordset, Record, Stream**</span></span>

<span data-ttu-id="edb51-p105">L'utilisation de la méthode **Close** pour fermer un objet **Recordset**, **Record** ou **Stream** libère les données associées, ainsi que tout accès exclusif aux données dont vous disposiez via cet objet spécifique. Vous pouvez appeler ultérieurement la méthode [Open](open-method-ado-recordset.md) pour rouvrir l'objet avec les mêmes attributs ou avec des attributs modifiés.</span><span class="sxs-lookup"><span data-stu-id="edb51-p105">Using the **Close** method to close a **Recordset**, **Record**, or **Stream** object releases the associated data and any exclusive access you may have had to the data through this particular object. You can later call the [Open](open-method-ado-recordset.md) method to reopen the object with the same, or modified, attributes.</span></span>

<span data-ttu-id="edb51-123">Lorsqu'un objet **Recordset** est fermé, l'appel d'une méthode nécessitant un curseur actif génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="edb51-123">While a **Recordset** object is closed, calling any methods that require a live cursor generates an error.</span></span>

<span data-ttu-id="edb51-p106">Lorsqu'une modification est en cours en mode de mise à jour immédiate, l'appel de la méthode **Close** génère une erreur ; vous devez appeler, au préalable, la méthode [Update](update-method-ado.md) ou [CancelUpdate](cancelupdate-method-ado.md). Si vous fermez l'objet **Recordset** en mode de mise à jour par lot, toutes les modifications apportées depuis le dernier appel de la méthode [UpdateBatch](updatebatch-method-ado.md) sont perdues.</span><span class="sxs-lookup"><span data-stu-id="edb51-p106">If an edit is in progress while in immediate update mode, calling the **Close** method generates an error; instead, call the [Update](update-method-ado.md) or [CancelUpdate](cancelupdate-method-ado.md) method first. If you close the **Recordset** object while in batch update mode, all changes since the last [UpdateBatch](updatebatch-method-ado.md) call are lost.</span></span>

<span data-ttu-id="edb51-126">Si vous utilisez la méthode [Clone](clone-method-ado.md) pour créer des copies d'un objet **Recordset** ouvert, la fermeture de l'objet d'origine ou d'un clone n'affecte pas les autres copies.</span><span class="sxs-lookup"><span data-stu-id="edb51-126">If you use the [Clone](clone-method-ado.md) method to create copies of an open **Recordset** object, closing the original or a clone does not affect any of the other copies.</span></span>

