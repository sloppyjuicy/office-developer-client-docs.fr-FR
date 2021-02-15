---
title: Propriété EOS (ADO - Référence de base de données de bureau Access))
TOCTitle: EOS property (ADO)
ms:assetid: 97cd23ef-cca8-4dcc-2641-082a0e1b853c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249676(v=office.15)
ms:contentKeyID: 48546474
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a35503fb0ad320e82ed385c7014b2a18de586064
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293524"
---
# <a name="eos-property-ado"></a><span data-ttu-id="d51cb-102">EOS, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="d51cb-102">EOS property (ADO)</span></span>


<span data-ttu-id="d51cb-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d51cb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d51cb-104">Indique si la position actuelle est à la fin du flux.</span><span class="sxs-lookup"><span data-stu-id="d51cb-104">Indicates whether the current position is at the end of the stream.</span></span>

## <a name="return-values"></a><span data-ttu-id="d51cb-105">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="d51cb-105">Return values</span></span>

<span data-ttu-id="d51cb-p101">Renvoie une valeur **booléenne** qui indique si la position actuelle est à la fin du flux. **EOS** renvoie **True** s'il ne reste plus d'octets dans le flux ; il renvoie **False** s'il reste des octets après la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="d51cb-p101">Returns a **Boolean** value that indicates whether the current position is at the end of the stream. **EOS** returns **True** if there are no more bytes in the stream; it returns **False** if there are more bytes following the current position.</span></span>

<span data-ttu-id="d51cb-p102">Pour définir la position de fin de flux, utilisez la méthode [SetEOS](seteos-method-ado.md). Pour déterminer la position actuelle, utilisez la propriété [Position](position-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d51cb-p102">To set the end of stream position, use the [SetEOS](seteos-method-ado.md) method. To determine the current position, use the [Position](position-property-ado.md) property.</span></span>

