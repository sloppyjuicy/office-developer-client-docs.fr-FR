---
title: Objet Error - ActiveX Data Objects (ADO)
TOCTitle: Error object (ADO)
ms:assetid: 97e478bf-8b25-03a8-9358-abba5069cba3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249678(v=office.15)
ms:contentKeyID: 48546477
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a7c77a59368851f43b5e7bf2275f9f282546fb4b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699225"
---
# <a name="error-object-ado"></a><span data-ttu-id="b0ed8-102">Error, objet (ADO)</span><span class="sxs-lookup"><span data-stu-id="b0ed8-102">Error object (ADO)</span></span>


<span data-ttu-id="b0ed8-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b0ed8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b0ed8-104">Contient des détails sur les erreurs d'accès aux données relatives à une seule opération impliquant le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-104">Contains details about data access errors that pertain to a single operation involving the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0ed8-105">Notes</span><span class="sxs-lookup"><span data-stu-id="b0ed8-105">Remarks</span></span>

<span data-ttu-id="b0ed8-p101">Toute opération impliquant des objets ADO peut générer une ou plusieurs erreurs liées au fournisseur. Lorsqu'une erreur se produit, un ou plusieurs objets **Error** sont placés dans la collection [Errors](errors-collection-ado.md) de l'objet [Connection](connection-object-ado.md). Lorsqu'une autre opération ADO génère une erreur, la collection **Errors** est vidée de son contenu ; le nouveau jeu d'objets **Error** est placé dans la collection **Errors**.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-p101">Any operation involving ADO objects can generate one or more provider errors. As each error occurs, one or more **Error** objects are placed in the [Errors](errors-collection-ado.md) collection of the [Connection](connection-object-ado.md) object. When another ADO operation generates an error, the **Errors** collection is cleared, and the new set of **Error** objects is placed in the **Errors** collection.</span></span>

> [!NOTE]
> <span data-ttu-id="b0ed8-p102">[!REMARQUE] Chaque objet **Error** représente une erreur de fournisseur spécifique, et pas une erreur ADO. Les erreurs ADO sont exposées au mécanisme de gestion des exceptions d'exécution. Par exemple, dans Microsoft Visual Basic, l'occurrence d'une erreur ADO spécifique déclenchera un événement **On Error** et apparaîtra dans l'objet **Error**. Pour obtenir la liste complète des erreurs ADO, voir la rubrique [ErrorValueEnum](errorvalueenum.md).</span><span class="sxs-lookup"><span data-stu-id="b0ed8-p102">Each **Error** object represents a specific provider error, not an ADO error. ADO errors are exposed to the run-time exception-handling mechanism. For example, in Microsoft Visual Basic, the occurrence of an ADO-specific error will trigger an **On Error** event and appear in the **Error** object. For a complete list of ADO errors, see the [ErrorValueEnum](errorvalueenum.md) topic.</span></span>

<span data-ttu-id="b0ed8-113">Vous pouvez lire les propriétés d'un objet **Error** pour obtenir des détails spécifiques sur chaque erreur, notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="b0ed8-113">You can read an **Error** object's properties to obtain specific details about each error, including the following:</span></span>

- <span data-ttu-id="b0ed8-p103">la propriété [Description](description-property-ado.md), qui contient le texte de l'erreur (propriété par défaut) ;</span><span class="sxs-lookup"><span data-stu-id="b0ed8-p103">The [Description](description-property-ado.md) property, which contains the text of the error. This is the default property.</span></span>

- <span data-ttu-id="b0ed8-116">la propriété [Number](number-property-ado.md), qui contient l'entier **Long** de la constante de l'erreur ;</span><span class="sxs-lookup"><span data-stu-id="b0ed8-116">The [Number](number-property-ado.md) property, which contains the **Long** integer value of the error constant.</span></span>

- <span data-ttu-id="b0ed8-p104">la propriété [Source](source-property-ado-error.md), qui identifie l'objet ayant entraîné l'erreur et est particulièrement utile lorsque vous avez plusieurs objets **Error** dans la collection **Errors** à la suite d'une demande exécutée sur une source de données ;</span><span class="sxs-lookup"><span data-stu-id="b0ed8-p104">The [Source](source-property-ado-error.md) property, which identifies the object that raised the error. This is particularly useful when you have several **Error** objects in the **Errors** collection following a request to a data source.</span></span>

- <span data-ttu-id="b0ed8-119">les propriétés [SQLState](sqlstate-property-ado.md) et [NativeError](nativeerror-property-ado.md), qui fournissent des informations depuis des sources de données SQL.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-119">The [SQLState](sqlstate-property-ado.md) and [NativeError](nativeerror-property-ado.md) properties, which provide information from SQL data sources.</span></span>

<span data-ttu-id="b0ed8-p105">Lorsqu'une erreur liée au fournisseur se produit, elle est placée dans la collection **Errors** de l'objet **Connection**. ADO prend en charge le renvoi de plusieurs erreurs par une seule opération ADO pour la prise en charge des informations d'erreur spécifiques au fournisseur. Pour obtenir ce niveau élevé de détail dans un gestionnaire d'erreurs, utilisez les fonctions d'interception appropriées de la langue ou de l'environnement dans lesquels vous travaillez, puis utilisez des boucles imbriquées pour énumérer les propriétés de chaque objet **Error** dans la collection **Errors**.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-p105">When a provider error occurs, it is placed in the **Errors** collection of the **Connection** object. ADO supports the return of multiple errors by a single ADO operation to allow for error information specific to the provider. To obtain this rich error information in an error handler, use the appropriate error-trapping features of the language or environment you are working with, then use nested loops to enumerate the properties of each **Error** object in the **Errors** collection.</span></span>

<span data-ttu-id="b0ed8-123">**Microsoft Visual Basic et les utilisateurs de VBScript** S’il n’existe aucun objet de **connexion** valide, vous devez récupérer les informations d’erreur à partir de l’objet **Error** .</span><span class="sxs-lookup"><span data-stu-id="b0ed8-123">**Microsoft Visual Basic and VBScript Users**If there is no valid **Connection** object, you will need to retrieve error information from the **Error** object.</span></span>

<span data-ttu-id="b0ed8-p106">Tout comme le font les fournisseurs, ADO efface l'objet **OLE Error Info** avant de lancer un appel susceptible de générer une nouvelle erreur spécifique du fournisseur. Toutefois, les objets présents dans la collection **Errors** sur l'objet **Connection** sont effacés et de nouveaux objets ne lui sont ajoutés que si le fournisseur génère une nouvelle erreur ou si la méthode [Clear](clear-method-ado.md) est appelée.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-p106">Just as providers do, ADO clears the **OLE Error Info** object before making a call that could potentially generate a new provider error. However, the **Errors** collection on the **Connection** object is cleared and populated only when the provider generates a new error, or when the [Clear](clear-method-ado.md) method is called.</span></span>

<span data-ttu-id="b0ed8-p107">Certaines propriétés et méthodes renvoient des avertissements qui s'affichent sous la forme d'objets **Error** dans la collection **Errors**, mais qui n'empêchent pas l'exécution d'un programme. Avant d'appeler les méthodes [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) ou [CancelBatch](cancelbatch-method-ado.md) sur un objet [Recordset](recordset-object-ado.md), la méthode [Open](open-method-ado-connection.md) sur un objet **Connection** ou avant de définir la propriété [Filter](filter-property-ado.md) sur un objet **Recordset**, appelez la méthode **Clear** sur la collection **Errors**. Ceci vous permet de lire la propriété [Count](count-property-ado.md) de la collection **Errors** pour tester les avertissements renvoyés.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-p107">Some properties and methods return warnings that appear as **Error** objects in the **Errors** collection but do not halt a program's execution. Before you call the [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), or [CancelBatch](cancelbatch-method-ado.md) methods on a [Recordset](recordset-object-ado.md) object; the [Open](open-method-ado-connection.md) method on a **Connection** object; or set the [Filter](filter-property-ado.md) property on a **Recordset** object, call the **Clear** method on the **Errors** collection. That way, you can read the [Count](count-property-ado.md) property of the **Errors** collection to test for returned warnings.</span></span>

