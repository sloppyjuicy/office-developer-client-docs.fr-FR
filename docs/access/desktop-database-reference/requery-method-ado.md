---
title: Requery, méthode (ADO)
TOCTitle: Requery Method (ADO)
ms:assetid: 1062d907-979f-020a-b2ed-94e11c0e7d08
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248871(v=office.15)
ms:contentKeyID: 48543292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3fde13d923a67ca995cdb3e7f59a327e82a9688
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471122"
---
# <a name="requery-method-ado"></a><span data-ttu-id="653e5-102">Requery, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="653e5-102">Requery Method (ADO)</span></span>


<span data-ttu-id="653e5-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="653e5-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="653e5-104">Cette méthode met à jour les données d'un objet [Recordset](recordset-object-ado.md) en réexécutant la requête sur laquelle l'objet est basé.</span><span class="sxs-lookup"><span data-stu-id="653e5-104">Updates the data in a [Recordset](recordset-object-ado.md) object by re-executing the query on which the object is based.</span></span>

## <a name="syntax"></a><span data-ttu-id="653e5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="653e5-105">Syntax</span></span>

<span data-ttu-id="653e5-106">*jeu d’enregistrements*. Actualiser les *Options*</span><span class="sxs-lookup"><span data-stu-id="653e5-106">*recordset*.Requery *Options*</span></span>

## <a name="parameter"></a><span data-ttu-id="653e5-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="653e5-107">Parameter</span></span>

  - <span data-ttu-id="653e5-108">*Options*</span><span class="sxs-lookup"><span data-stu-id="653e5-108">*Options*</span></span>

  - <span data-ttu-id="653e5-p101">Facultatif. Masque de bits contenant des valeurs [ExecuteOptionEnum](executeoptionenum.md) et [CommandTypeEnum](commandtypeenum.md) affectant cette opération.</span><span class="sxs-lookup"><span data-stu-id="653e5-p101">Optional. A bitmask that contains [ExecuteOptionEnum](executeoptionenum.md) and [CommandTypeEnum](commandtypeenum.md) values affecting this operation.</span></span>


> [!NOTE]
> <P><span data-ttu-id="653e5-111">Si <EM>Options</EM> a la valeur <STRONG>adAsyncExecute</STRONG>, cette opération est exécutée de façon asynchrone et un événement <A href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</A> est déclenché lorsqu’elle est terminée.</span><span class="sxs-lookup"><span data-stu-id="653e5-111">If <EM>Options</EM> is set to <STRONG>adAsyncExecute</STRONG>, this operation will execute asynchronously and a <A href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</A> event will be issued when it concludes.</span></span></P>



<span data-ttu-id="653e5-112">Les valeurs **adExecuteNoRecords** ou **adExecuteStream** de l'énumération **ExecuteOpenEnum** ne doivent pas être utilisées avec **Requery**.</span><span class="sxs-lookup"><span data-stu-id="653e5-112">The **ExecuteOpenEnum** values of **adExecuteNoRecords** or **adExecuteStream** should not be used with **Requery**.</span></span>

## <a name="remarks"></a><span data-ttu-id="653e5-113">Notes</span><span class="sxs-lookup"><span data-stu-id="653e5-113">Remarks</span></span>

<span data-ttu-id="653e5-p102">Faites appel à la méthode **Requery** pour actualiser tout le contenu d'un objet **Recordset** à partir de la base de données en réexécutant la commande d'origine et en extrayant les données une seconde fois. L'appel de cette méthode revient à appeler successivement les méthodes [Close](close-method-ado.md) et [Open](open-method-ado-recordset.md). Si vous modifiez l'enregistrement actif ou que vous ajoutez un nouvel enregistrement, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="653e5-p102">Use the **Requery** method to refresh the entire contents of a **Recordset** object from the data source by reissuing the original command and retrieving the data a second time. Calling this method is equivalent to calling the [Close](close-method-ado.md) and [Open](open-method-ado-recordset.md) methods in succession. If you are editing the current record or adding a new record, an error occurs.</span></span>

<span data-ttu-id="653e5-p103">Lorsque l’objet **Recordset** est ouvert, les propriétés qui définissent la nature du curseur ([CursorType](cursortype-property-ado.md), [LockType](locktype-property-ado.md), [MaxRecords](maxrecords-property-ado.md), etc.) sont en lecture seule. Ainsi, la méthode **Requery** ne peut actualiser que le curseur actif. Pour changer des propriétés du curseur et afficher les résultats ainsi obtenus, vous devez faire appel à la méthode [Close](close-method-ado.md) afin que les propriétés soient à nouveau en lecture-écriture. Vous pouvez alors changer les paramètres des propriétés et appeler la méthode [Open](open-method-ado-recordset.md) pour rouvrir le curseur.</span><span class="sxs-lookup"><span data-stu-id="653e5-p103">While the **Recordset** object is open, the properties that define the nature of the cursor ([CursorType](cursortype-property-ado.md), [LockType](locktype-property-ado.md), [MaxRecords](maxrecords-property-ado.md), and so forth) are read-only. Thus, the **Requery** method can only refresh the current cursor. To change any of the cursor properties and view the results, you must use the [Close](close-method-ado.md) method so that the properties become read/write again. You can then change the property settings and call the [Open](open-method-ado-recordset.md) method to reopen the cursor.</span></span>

