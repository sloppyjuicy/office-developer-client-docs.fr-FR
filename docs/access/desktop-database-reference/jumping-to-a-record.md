---
title: Accès à un enregistrement
TOCTitle: Jumping to a record
ms:assetid: 27177bbe-066c-aeb0-6dfd-45d8c2a87487
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249033(v=office.15)
ms:contentKeyID: 48543829
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9ce27722600ae8a634092612ddf11694faa4ecef
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944472"
---
# <a name="jumping-to-a-record"></a><span data-ttu-id="b6d47-102">Accès à un enregistrement</span><span class="sxs-lookup"><span data-stu-id="b6d47-102">Jumping to a record</span></span>


<span data-ttu-id="b6d47-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b6d47-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b6d47-104">La méthode [Move](move-method-ado.md) vous permet d'avancer ou de reculer d'un nombre spécifié d'enregistrements dans l'objet **Recordset**, en utilisant la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="b6d47-104">The [Move](move-method-ado.md) method allows you to move forward or backward in the **Recordset** a specified number of records by using the following syntax:</span></span>

```vb 
 
oRs.Move NumRecords, Start
```

<span data-ttu-id="b6d47-105">La méthode **Move** est prise en charge sur tous les objets **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="b6d47-105">The **Move** method is supported on all **Recordset** objects.</span></span>

<span data-ttu-id="b6d47-p101">Si l'argument *NumRecords* est supérieur à zéro, la position de l'enregistrement actif est avancée (vers la fin du **jeu d'enregistrements**). Si l'argument *NumRecords* est inférieur à zéro, la position de l'enregistrement actif est déplacée vers l'arrière (vers le début du **jeu d'enregistrements**).</span><span class="sxs-lookup"><span data-stu-id="b6d47-p101">If the *NumRecords* argument is greater than zero, the current record position moves forward (toward the end of the **Recordset**). If *NumRecords* is less than zero, the current record position moves backward (toward the beginning of the **Recordset**).</span></span>

<span data-ttu-id="b6d47-p102">Si l'appel de la méthode **Move** déplace la position de l'enregistrement actif vers un point situé avant le premier enregistrement, ADO place automatiquement l'enregistrement actif à la position précédant le premier enregistrement dans l'objet **Recordset** (la propriété **BOF** a la valeur \*\*True \*\*). Si vous tentez un déplacement vers l'arrière lorsque la propriété **BOF** a déjà la valeur **True**, une erreur est générée.</span><span class="sxs-lookup"><span data-stu-id="b6d47-p102">If the **Move** call would move the current record position to a point before the first record, ADO sets the current record to the position before the first record in the **Recordset** (**BOF** is **True**). An attempt to move backward when the **BOF** property is already **True** generates an error.</span></span>

<span data-ttu-id="b6d47-p103">Si l’appel de la méthode **Move** déplace la position de l’enregistrement actif vers un point situé après le dernier enregistrement, ADO place automatiquement l’enregistrement actif à la position suivant le dernier enregistrement dans l’objet **Recordset** (la propriété **EOF** a la valeur **True**). Si vous tentez un déplacement vers l’avant lorsque la propriété **EOF** a déjà la valeur **True**, une erreur est générée.</span><span class="sxs-lookup"><span data-stu-id="b6d47-p103">If the **Move** call would move the current record position to a point after the last record, ADO sets the current record to the position after the last record in the **Recordset** (**EOF** is **True**). An attempt to move forward when the **EOF** property is already **True** generates an error.</span></span>

<span data-ttu-id="b6d47-112">L'appel de la méthode **Move** à partir d'un objet **Recordset** vide génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="b6d47-112">Calling the **Move** method from an empty **Recordset** object generates an error.</span></span>

<span data-ttu-id="b6d47-113">Si vous passez un signet dans l’argument *Start* , le déplacement est par rapport à l’objet record à ce signet, en supposant que l’objet **Recordset** prend en charge les signets.</span><span class="sxs-lookup"><span data-stu-id="b6d47-113">If you pass a bookmark in the *Start* argument, the move is relative to the record with this bookmark, assuming the **Recordset** object supports bookmarks.</span></span> <span data-ttu-id="b6d47-114">Les signets sont définis par l'intermédiaire de la propriété [Bookmark](bookmark-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="b6d47-114">A bookmark is obtained by using the [Bookmark](bookmark-property-ado.md) property.</span></span> <span data-ttu-id="b6d47-115">Si aucun signet n'est spécifié, le déplacement s'applique à l'enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="b6d47-115">If not specified, the move is relative to the current record.</span></span>

<span data-ttu-id="b6d47-116">Si vous utilisez la propriété **CacheSize** pour cache localement des enregistrements à partir du fournisseur, en passant un argument *NbEnregistrements* qui déplace la position d’enregistrement actif en dehors du groupe actuel d’enregistrements mis en cache force ADO à récupérer un nouveau groupe d’enregistrements, à partir de l’enregistrement de destination.</span><span class="sxs-lookup"><span data-stu-id="b6d47-116">If you are using the **CacheSize** property to locally cache records from the provider, passing a *NumRecords* argument that moves the current record position outside the current group of cached records forces ADO to retrieve a new group of records, starting from the destination record.</span></span> <span data-ttu-id="b6d47-117">La propriété **CacheSize** détermine la taille du nouveau groupe extrait et l’enregistrement de destination est le premier enregistrement récupéré.</span><span class="sxs-lookup"><span data-stu-id="b6d47-117">The **CacheSize** property determines the size of the newly retrieved group, and the destination record is the first record retrieved.</span></span>

