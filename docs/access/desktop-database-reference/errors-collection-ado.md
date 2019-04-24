---
title: Errors, collection (ADO)
TOCTitle: Errors collection (ADO)
ms:assetid: 76c234b8-7fec-11c5-275e-864d5d880ee7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249486(v=office.15)
ms:contentKeyID: 48545706
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: db9fa4fccc4f3d13849f34c157f2ea07cc3f171d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293426"
---
# <a name="errors-collection-ado"></a><span data-ttu-id="ebe16-102">Errors, collection (ADO)</span><span class="sxs-lookup"><span data-stu-id="ebe16-102">Errors collection (ADO)</span></span>


<span data-ttu-id="ebe16-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ebe16-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ebe16-104">Contient tous les objets [Error](error-object-ado.md) créés en réponse à une erreur liée au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ebe16-104">Contains all the [Error](error-object-ado.md) objects created in response to a single provider-related failure provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebe16-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="ebe16-105">Remarks</span></span>

<span data-ttu-id="ebe16-p101">Toute opération impliquant des objets ADO peut générer une ou plusieurs erreurs d'un fournisseur. Lorsqu'une erreur se produit, un ou plusieurs objets **Error** peuvent être placés dans la collection **Errors** de l'objet [Connection](connection-object-ado.md). Lorsqu'une autre opération ADO génère une erreur, la collection **Errors** est vidée de son contenu, et le nouveau jeu d'objets **Error** peut être placé dans la collection **Errors**.</span><span class="sxs-lookup"><span data-stu-id="ebe16-p101">Any operation involving ADO objects can generate one or more provider errors. As each error occurs, one or more **Error** objects can be placed in the **Errors** collection of the [Connection](connection-object-ado.md) object. When another ADO operation generates an error, the **Errors** collection is cleared, and the new set of **Error** objects can be placed in the **Errors** collection.</span></span>

<span data-ttu-id="ebe16-p102">Chaque objet **Error** représente une erreur de fournisseur spécifique, et pas une erreur ADO. Les erreurs ADO sont exposées au mécanisme de gestion des exceptions d'exécution. Par exemple, dans Microsoft Visual Basic, l'occurrence d'une erreur ADO spécifique déclenchera un événement [onError](onerror-event-rds.md) et apparaîtra dans l'objet **Err**.</span><span class="sxs-lookup"><span data-stu-id="ebe16-p102">Each **Error** object represents a specific provider error, not an ADO error. ADO errors are exposed to the run-time exception-handling mechanism. For example, in Microsoft Visual Basic, the occurrence of an ADO-specific error will trigger an [onError](onerror-event-rds.md) event and appear in the **Err** object.</span></span>

<span data-ttu-id="ebe16-p103">Les opérations ADO qui ne génèrent pas d'erreur sont sans effet sur la collection **Errors**. Utilisez la méthode [Clear](clear-method-ado.md) pour effacer manuellement le contenu de la collection **Errors**.</span><span class="sxs-lookup"><span data-stu-id="ebe16-p103">ADO operations that don't generate an error have no effect on the **Errors** collection. Use the [Clear](clear-method-ado.md) method to manually clear the **Errors** collection.</span></span>

<span data-ttu-id="ebe16-p104">Le jeu d'objets **Error** de la collection **Errors** décrit toutes les erreurs qui ont eu lieu en réponse à une seule instruction. Le fait d'énumérer les erreurs spécifiques dans la collection **Errors** permet à vos routines de gestion des erreurs de déterminer avec plus de précision la cause et l'origine d'une erreur et d'exécuter les actions appropriées pour la corriger.</span><span class="sxs-lookup"><span data-stu-id="ebe16-p104">The set of **Error** objects in the **Errors** collection describes all errors that occurred in response to a single statement. Enumerating the specific errors in the **Errors** collection enables your error-handling routines to more precisely determine the cause and origin of an error, and take appropriate steps to recover.</span></span>

<span data-ttu-id="ebe16-p105">Certaines propriétés et méthodes renvoient des avertissements qui s'affichent sous la forme d'objets **Error** dans la collection **Errors**, mais qui n'empêchent pas l'exécution d'un programme. Avant d'appeler les méthodes [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) ou [CancelBatch](cancelbatch-method-ado.md) sur un objet [Recordset](recordset-object-ado.md), la méthode [Open](open-method-ado-connection.md) sur un objet **Connection** ou avant de définir la propriété [Filter](filter-property-ado.md) sur un objet **Recordset**, appelez la méthode **Clear** sur la collection **Errors**. Ceci vous permet de lire la propriété [Count](count-property-ado.md) de la collection **Errors** pour tester les avertissements renvoyés.</span><span class="sxs-lookup"><span data-stu-id="ebe16-p105">Some properties and methods return warnings that appear as **Error** objects in the **Errors** collection but do not halt a program's execution. Before you call the [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), or [CancelBatch](cancelbatch-method-ado.md) methods on a [Recordset](recordset-object-ado.md) object, the [Open](open-method-ado-connection.md) method on a **Connection** object, or set the [Filter](filter-property-ado.md) property on a **Recordset** object, call the **Clear** method on the **Errors** collection. That way you can read the [Count](count-property-ado.md) property of the **Errors** collection to test for returned warnings.</span></span>


> [!NOTE]
> <span data-ttu-id="ebe16-119">[!REMARQUE] Pour plus d'informations sur la manière dont une seule opération ADO peut générer plusieurs erreurs, voir la rubrique consacrée à l'objet **Error**.</span><span class="sxs-lookup"><span data-stu-id="ebe16-119">See the **Error** object topic for a more detailed explanation of the way a single ADO operation can generate multiple errors.</span></span>


