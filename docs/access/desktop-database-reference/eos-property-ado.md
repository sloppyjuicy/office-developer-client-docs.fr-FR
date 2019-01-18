---
title: EOS, propriété (ADO - référence du bureau de la base de données Access))
TOCTitle: EOS property (ADO)
ms:assetid: 97cd23ef-cca8-4dcc-2641-082a0e1b853c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249676(v=office.15)
ms:contentKeyID: 48546474
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a35503fb0ad320e82ed385c7014b2a18de586064
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716599"
---
# <a name="eos-property-ado"></a><span data-ttu-id="3b86c-102">EOS, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="3b86c-102">EOS property (ADO)</span></span>


<span data-ttu-id="3b86c-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3b86c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3b86c-104">Indique si la position actuelle est à la fin du flux.</span><span class="sxs-lookup"><span data-stu-id="3b86c-104">Indicates whether the current position is at the end of the stream.</span></span>

## <a name="return-values"></a><span data-ttu-id="3b86c-105">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="3b86c-105">Return values</span></span>

<span data-ttu-id="3b86c-p101">Renvoie une valeur **booléenne** qui indique si la position actuelle est à la fin du flux. **EOS** renvoie **True** s'il ne reste plus d'octets dans le flux ; il renvoie **False** s'il reste des octets après la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="3b86c-p101">Returns a **Boolean** value that indicates whether the current position is at the end of the stream. **EOS** returns **True** if there are no more bytes in the stream; it returns **False** if there are more bytes following the current position.</span></span>

<span data-ttu-id="3b86c-p102">Pour définir la position de fin de flux, utilisez la méthode [SetEOS](seteos-method-ado.md). Pour déterminer la position actuelle, utilisez la propriété [Position](position-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="3b86c-p102">To set the end of stream position, use the [SetEOS](seteos-method-ado.md) method. To determine the current position, use the [Position](position-property-ado.md) property.</span></span>

