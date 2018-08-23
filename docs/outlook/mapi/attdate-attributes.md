---
title: Attributs attDate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22801641-752c-4c81-be90-02039eaa4277
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ff0cc6b1c17b2ed83d7b0ec0921904763da8624b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567012"
---
# <a name="attdate-attributes"></a><span data-ttu-id="ef21e-103">Attributs attDate</span><span class="sxs-lookup"><span data-stu-id="ef21e-103">attDate Attributes</span></span>

  
  
<span data-ttu-id="ef21e-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ef21e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ef21e-105">Toutes les propriétés MAPI relatives aux dates et heures sont mappées aux attributs TNEF qui ont le préfixe **attDate** .</span><span class="sxs-lookup"><span data-stu-id="ef21e-105">All MAPI properties relating to dates and times are mapped to TNEF attributes that have the **attDate** prefix.</span></span> <span data-ttu-id="ef21e-106">Tous ces sont codées en tant que structures **DTR** .</span><span class="sxs-lookup"><span data-stu-id="ef21e-106">These are all encoded as **DTR** structures.</span></span> <span data-ttu-id="ef21e-107">Les dates et heures pour les attributs des pièces jointes sont codées en tant que structures **DTR** également.</span><span class="sxs-lookup"><span data-stu-id="ef21e-107">The dates and times for attachment attributes are encoded as **DTR** structures as well.</span></span> 
  
<span data-ttu-id="ef21e-108">Toutes les propriétés MAPI relatives aux dates et heures sont mappées aux attributs TNEF qui ont le préfixe **attDate** .</span><span class="sxs-lookup"><span data-stu-id="ef21e-108">All MAPI properties relating to dates and times are mapped to TNEF attributes that have the **attDate** prefix.</span></span> <span data-ttu-id="ef21e-109">Tous ces sont codées en tant que structures **DTR** .</span><span class="sxs-lookup"><span data-stu-id="ef21e-109">These are all encoded as **DTR** structures.</span></span> <span data-ttu-id="ef21e-110">Les dates et heures pour les attributs des pièces jointes sont codées en tant que structures **DTR** également.</span><span class="sxs-lookup"><span data-stu-id="ef21e-110">The dates and times for attachment attributes are encoded as **DTR** structures as well.</span></span> 
  
<span data-ttu-id="ef21e-111">Une structure **DTR** est très similaire à la structure **SYSTEMTIME** définie dans les fichiers d’en-tête Win32.</span><span class="sxs-lookup"><span data-stu-id="ef21e-111">A **DTR** structure is very similar to the **SYSTEMTIME** structure defined in the Win32 header files.</span></span> <span data-ttu-id="ef21e-112">La structure **DTR** est codée dans le flux TNEF en octets **sizeof(DTR)** commençant par le premier membre de la structure.</span><span class="sxs-lookup"><span data-stu-id="ef21e-112">The **DTR** structure is encoded in the TNEF stream as **sizeof(DTR)** bytes starting with the first member of the structure.</span></span> <span data-ttu-id="ef21e-113">La structure **DTR** est définie dans le format TNEF. Fichier d’en-tête H.</span><span class="sxs-lookup"><span data-stu-id="ef21e-113">The **DTR** structure is defined in the TNEF.H header file.</span></span> 
  

