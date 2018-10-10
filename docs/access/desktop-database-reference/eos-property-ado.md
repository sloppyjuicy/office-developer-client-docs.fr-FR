---
title: EOS, propriété (ADO - référence du bureau de la base de données Access))
TOCTitle: EOS Property (ADO)
ms:assetid: 97cd23ef-cca8-4dcc-2641-082a0e1b853c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249676(v=office.15)
ms:contentKeyID: 48546474
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d4c6d96e2c143cb0548a2de987f11ea708d1669a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470699"
---
# <a name="eos-property-ado"></a><span data-ttu-id="c5e80-102">EOS, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="c5e80-102">EOS Property (ADO)</span></span>


<span data-ttu-id="c5e80-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c5e80-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c5e80-104">Indique si la position actuelle est à la fin du flux.</span><span class="sxs-lookup"><span data-stu-id="c5e80-104">Indicates whether the current position is at the end of the stream.</span></span>

## <a name="return-values"></a><span data-ttu-id="c5e80-105">Valeurs renvoyées</span><span class="sxs-lookup"><span data-stu-id="c5e80-105">Return Values</span></span>

<span data-ttu-id="c5e80-p101">Renvoie une valeur **booléenne** qui indique si la position actuelle est à la fin du flux. **EOS** renvoie **True** s'il ne reste plus d'octets dans le flux ; il renvoie **False** s'il reste des octets après la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="c5e80-p101">Returns a **Boolean** value that indicates whether the current position is at the end of the stream. **EOS** returns **True** if there are no more bytes in the stream; it returns **False** if there are more bytes following the current position.</span></span>

<span data-ttu-id="c5e80-p102">Pour définir la position de fin de flux, utilisez la méthode [SetEOS](seteos-method-ado.md). Pour déterminer la position actuelle, utilisez la propriété [Position](position-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c5e80-p102">To set the end of stream position, use the [SetEOS](seteos-method-ado.md) method. To determine the current position, use the [Position](position-property-ado.md) property.</span></span>

