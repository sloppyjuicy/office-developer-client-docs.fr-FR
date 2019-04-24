---
title: attAttachRenddata
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c510b7a5-0f55-46af-bddb-40a8195a84d4
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: d58fc0eae5401773d28f5bbe510913ff381ade8d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331912"
---
# <a name="attattachrenddata"></a><span data-ttu-id="aab2d-103">attAttachRenddata</span><span class="sxs-lookup"><span data-stu-id="aab2d-103">attAttachRenddata</span></span>

  
  
<span data-ttu-id="aab2d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aab2d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aab2d-105">L'attribut **attAttachRenddata** est encodé sous la forme d'une structure **RENDDATA** qui décrit comment et où la pièce jointe est affichée dans le texte du message.</span><span class="sxs-lookup"><span data-stu-id="aab2d-105">The **attAttachRenddata** attribute is encoded as a **RENDDATA** structure that describes how and where the attachment is rendered in the message text.</span></span> <span data-ttu-id="aab2d-106">La structure **RENDDATA** est simplement codée dans le flux TNEF en tant qu'octets **sizeof (RENDDATA)** en commençant par le premier membre de la structure **RENDDATA** .</span><span class="sxs-lookup"><span data-stu-id="aab2d-106">The **RENDDATA** structure is simply encoded in the TNEF stream as **sizeof(RENDDATA)** bytes beginning with the first member of the **RENDDATA** structure.</span></span> <span data-ttu-id="aab2d-107">Si la valeur du membre **dwFlags** de la structure **RENDDATA** est définie sur **MAC_BINARY**, les données de la pièce jointe suivante sont stockées dans le format MacBinary; dans le cas contraire, les données de la pièce jointe sont codées comme d'habitude.</span><span class="sxs-lookup"><span data-stu-id="aab2d-107">If the value of the **RENDDATA** structure's **dwFlags** member is set to **MAC_BINARY**, then the data for the following attachment is stored in MacBinary format; otherwise, the attachment data is encoded as usual.</span></span>
  

