---
title: Codes d’erreur ADO
TOCTitle: ADO error codes
ms:assetid: d7cad7f6-9b95-a521-9947-32658f503e3b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250086(v=office.15)
ms:contentKeyID: 48548016
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2d3d51fa745f17fb07f6a46064ba8ffc626cbb3e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283386"
---
# <a name="ado-error-codes"></a><span data-ttu-id="68f53-102">Codes d’erreur ADO</span><span class="sxs-lookup"><span data-stu-id="68f53-102">ADO error codes</span></span>

<span data-ttu-id="68f53-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="68f53-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="68f53-p101">ADO peut renvoyer des erreurs au mécanisme de gestion des exceptions de votre environnement d'exécution en plus des erreurs de fournisseur renvoyées dans les objets [Error](error-object-ado.md) de la collection [Errors](errors-collection-ado.md). Pour capturer les erreurs ADO, utilisez le mécanisme de recouvrement des erreurs de votre langage de programmation, c'est-à-dire l'instruction **OnError** dans Microsoft Visual Basic ou le bloc **try-catch** dans Microsoft Visual C++ et Microsoft Visual J++.</span><span class="sxs-lookup"><span data-stu-id="68f53-p101">In addition to the provider errors returned in the [Error](error-object-ado.md) objects of the [Errors](errors-collection-ado.md) collection, ADO itself can return errors to the exception-handling mechanism of your run-time environment. Use the error trapping mechanism your programming language, such as the **On Error** statement in Microsoft Visual Basic or the **try-catch** block in Microsoft Visual C++ or Microsoft Visual J++ to capture ADO errors.</span></span>

<span data-ttu-id="68f53-106">Pour obtenir la liste des codes d'erreur ADO, consultez[ErrorValueEnum](errorvalueenum.md).</span><span class="sxs-lookup"><span data-stu-id="68f53-106">For the list of ADO error codes, see [ErrorValueEnum](errorvalueenum.md).</span></span>

