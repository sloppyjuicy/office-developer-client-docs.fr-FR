---
title: Name, propriété (ADO)
TOCTitle: Name property (ADO)
ms:assetid: 4b19bd08-ac3c-86f0-471d-06a37a0d4f89
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249234(v=office.15)
ms:contentKeyID: 48544683
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f6fbfbd7008919cc4d784a4d0468d8471d102708
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721546"
---
# <a name="name-property-ado"></a><span data-ttu-id="803d7-102">Name, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="803d7-102">Name property (ADO)</span></span>


<span data-ttu-id="803d7-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="803d7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="803d7-104">Indique le nom d'un objet.</span><span class="sxs-lookup"><span data-stu-id="803d7-104">Indicates the name of an object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="803d7-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="803d7-105">Settings and return values</span></span>

<span data-ttu-id="803d7-106">Définit ou renvoie une valeur **String** indiquant le nom d'un objet.</span><span class="sxs-lookup"><span data-stu-id="803d7-106">Sets or returns a **String** value that indicates the name of an object.</span></span>

## <a name="remarks"></a><span data-ttu-id="803d7-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="803d7-107">Remarks</span></span>

<span data-ttu-id="803d7-108">Utilisez la propriété **Name** pour attribuer un nom ou pour récupérer au nom d'un objet **Command**, **Property**, **Field** ou **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="803d7-108">Use the **Name** property to assign a name to or retrieve the name of a **Command**, **Property**, **Field**, or **Parameter** object.</span></span>

<span data-ttu-id="803d7-109">La valeur est accessible en lecture/écriture sur un objet **Command** et lecture seule sur un objet **Property**.</span><span class="sxs-lookup"><span data-stu-id="803d7-109">The value is read/write on a **Command** object and read-only on a **Property** object.</span></span>

<span data-ttu-id="803d7-p101">Pour un objet **Field**, **Name** est généralement en lecture seule. Toutefois, pour les objets **Field** récemment ajoutés à la collection [Fields](fields-collection-ado.md) d'un objet [Record](record-object-ado.md), **Name** est exceptionnellement accessible en lecture et en écriture après la définition de la propriété [Value](value-property-ado.md) de l'objet **Field** et une fois que le fournisseur de données a ajouté le nouvel objet **Field** en appelant la méthode [Update](update-method-ado.md) de la collection **Fields**.</span><span class="sxs-lookup"><span data-stu-id="803d7-p101">For a **Field** object, **Name** is normally read-only. However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Name** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

<span data-ttu-id="803d7-p102">Pour les objets **Parameter** qui n'ont pas encore été ajoutés à la collection [Parameters](parameters-collection-ado.md), la propriété **Name** est accessible en lecture/écriture. Pour les objets **Parameter** ajoutés et tous les autres objets, la propriété **Name** est en lecture seule. Les noms peuvent exister en double au sein de la même collection.</span><span class="sxs-lookup"><span data-stu-id="803d7-p102">For **Parameter** objects not yet appended to the [Parameters](parameters-collection-ado.md) collection, the **Name** property is read/write. For appended **Parameter** objects and all other objects, the **Name** property is read-only. Names do not have to be unique within a collection.</span></span>

<span data-ttu-id="803d7-115">Vous pouvez récupérer la propriété **Name** d'un objet par référence ordinale, après quoi vous pouvez directement faire référence à l'objet par son nom.</span><span class="sxs-lookup"><span data-stu-id="803d7-115">You can retrieve the **Name** property of an object by an ordinal reference, after which you can refer to the object directly by name.</span></span> <span data-ttu-id="803d7-116">Par exemple, si rstMain.Properties (20). Nom de produit de mise à jour, vous pouvez ensuite référencer cette propriété comme mise à jour de produit, vous pouvez ensuite référencer cette propriété en tant que rstMain.Properties("Updatability").</span><span class="sxs-lookup"><span data-stu-id="803d7-116">For example, if rstMain.Properties(20).Name yields Updatability , you can subsequently refer to this property as yields Updatability , you can subsequently refer to this property as rstMain.Properties("Updatability") .</span></span>

