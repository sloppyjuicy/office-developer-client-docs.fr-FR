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
ms.openlocfilehash: b7c1ce8d0338a2bda63a276628bdd6e8be3b8eb1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408277"
---
# <a name="attdate-attributes"></a><span data-ttu-id="2a308-103">Attributs attDate</span><span class="sxs-lookup"><span data-stu-id="2a308-103">attDate Attributes</span></span>

  
  
<span data-ttu-id="2a308-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a308-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a308-105">Toutes les propriétés MAPI relatives aux dates et heures sont mappées aux attributs TNEF qui ont le **préfixe attDate.**</span><span class="sxs-lookup"><span data-stu-id="2a308-105">All MAPI properties relating to dates and times are mapped to TNEF attributes that have the **attDate** prefix.</span></span> <span data-ttu-id="2a308-106">Toutes ces structures sont codées en tant que structures **DTR.**</span><span class="sxs-lookup"><span data-stu-id="2a308-106">These are all encoded as **DTR** structures.</span></span> <span data-ttu-id="2a308-107">Les dates et heures des attributs de pièce jointe sont également codées en tant que structures **DTR.**</span><span class="sxs-lookup"><span data-stu-id="2a308-107">The dates and times for attachment attributes are encoded as **DTR** structures as well.</span></span> 
  
<span data-ttu-id="2a308-108">Toutes les propriétés MAPI relatives aux dates et heures sont mappées aux attributs TNEF qui ont le **préfixe attDate.**</span><span class="sxs-lookup"><span data-stu-id="2a308-108">All MAPI properties relating to dates and times are mapped to TNEF attributes that have the **attDate** prefix.</span></span> <span data-ttu-id="2a308-109">Toutes ces structures sont codées en tant que structures **DTR.**</span><span class="sxs-lookup"><span data-stu-id="2a308-109">These are all encoded as **DTR** structures.</span></span> <span data-ttu-id="2a308-110">Les dates et heures des attributs de pièce jointe sont également codées en tant que structures **DTR.**</span><span class="sxs-lookup"><span data-stu-id="2a308-110">The dates and times for attachment attributes are encoded as **DTR** structures as well.</span></span> 
  
<span data-ttu-id="2a308-111">Une structure **DTR** est très similaire à la structure **SYSTEMTIME** définie dans les fichiers d’en-tête Win32.</span><span class="sxs-lookup"><span data-stu-id="2a308-111">A **DTR** structure is very similar to the **SYSTEMTIME** structure defined in the Win32 header files.</span></span> <span data-ttu-id="2a308-112">La structure **DTR** est codée dans le flux TNEF en tant qu’octets **sizeof(DTR)** en commençant par le premier membre de la structure.</span><span class="sxs-lookup"><span data-stu-id="2a308-112">The **DTR** structure is encoded in the TNEF stream as **sizeof(DTR)** bytes starting with the first member of the structure.</span></span> <span data-ttu-id="2a308-113">La structure **DTR** est définie dans le TNEF. Fichier d’en-tête H.</span><span class="sxs-lookup"><span data-stu-id="2a308-113">The **DTR** structure is defined in the TNEF.H header file.</span></span> 
  

