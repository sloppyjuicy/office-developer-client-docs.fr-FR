---
title: EOS, propriété (ADO - référence du bureau de la base de données Access))
TOCTitle: EOS property (ADO)
ms:assetid: 97cd23ef-cca8-4dcc-2641-082a0e1b853c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249676(v=office.15)
ms:contentKeyID: 48546474
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 32b76259f9be90ebd60cbc8c618a4d2bb80de165
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870120"
---
# <a name="eos-property-ado"></a><span data-ttu-id="d5776-102">EOS, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="d5776-102">EOS property (ADO)</span></span>


<span data-ttu-id="d5776-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d5776-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d5776-104">Indique si la position actuelle est à la fin du flux.</span><span class="sxs-lookup"><span data-stu-id="d5776-104">Indicates whether the current position is at the end of the stream.</span></span>

## <a name="return-values"></a><span data-ttu-id="d5776-105">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="d5776-105">Return values</span></span>

<span data-ttu-id="d5776-p101">Renvoie une valeur **booléenne** qui indique si la position actuelle est à la fin du flux. **EOS** renvoie **True** s'il ne reste plus d'octets dans le flux ; il renvoie **False** s'il reste des octets après la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="d5776-p101">Returns a **Boolean** value that indicates whether the current position is at the end of the stream. **EOS** returns **True** if there are no more bytes in the stream; it returns **False** if there are more bytes following the current position.</span></span>

<span data-ttu-id="d5776-p102">Pour définir la position de fin de flux, utilisez la méthode [SetEOS](seteos-method-ado.md). Pour déterminer la position actuelle, utilisez la propriété [Position](position-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d5776-p102">To set the end of stream position, use the [SetEOS](seteos-method-ado.md) method. To determine the current position, use the [Position](position-property-ado.md) property.</span></span>

