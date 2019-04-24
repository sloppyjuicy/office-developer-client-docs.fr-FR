---
title: Attributs attDate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22801641-752c-4c81-be90-02039eaa4277
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: b7c1ce8d0338a2bda63a276628bdd6e8be3b8eb1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318066"
---
# <a name="attdate-attributes"></a><span data-ttu-id="cc6c3-103">Attributs attDate</span><span class="sxs-lookup"><span data-stu-id="cc6c3-103">attDate Attributes</span></span>

  
  
<span data-ttu-id="cc6c3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cc6c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cc6c3-105">Toutes les propriétés MAPI liées aux dates et heures sont mappées aux attributs TNEF qui ont le préfixe **attDate** .</span><span class="sxs-lookup"><span data-stu-id="cc6c3-105">All MAPI properties relating to dates and times are mapped to TNEF attributes that have the **attDate** prefix.</span></span> <span data-ttu-id="cc6c3-106">Ces éléments sont tous codés sous forme de structures **DTR** .</span><span class="sxs-lookup"><span data-stu-id="cc6c3-106">These are all encoded as **DTR** structures.</span></span> <span data-ttu-id="cc6c3-107">Les dates et les heures des attributs de pièce jointe sont également codées en tant que structures **DTR** .</span><span class="sxs-lookup"><span data-stu-id="cc6c3-107">The dates and times for attachment attributes are encoded as **DTR** structures as well.</span></span> 
  
<span data-ttu-id="cc6c3-108">Toutes les propriétés MAPI liées aux dates et heures sont mappées aux attributs TNEF qui ont le préfixe **attDate** .</span><span class="sxs-lookup"><span data-stu-id="cc6c3-108">All MAPI properties relating to dates and times are mapped to TNEF attributes that have the **attDate** prefix.</span></span> <span data-ttu-id="cc6c3-109">Ces éléments sont tous codés sous forme de structures **DTR** .</span><span class="sxs-lookup"><span data-stu-id="cc6c3-109">These are all encoded as **DTR** structures.</span></span> <span data-ttu-id="cc6c3-110">Les dates et les heures des attributs de pièce jointe sont également codées en tant que structures **DTR** .</span><span class="sxs-lookup"><span data-stu-id="cc6c3-110">The dates and times for attachment attributes are encoded as **DTR** structures as well.</span></span> 
  
<span data-ttu-id="cc6c3-111">Une structure **DTR** est très semblable à la structure **SystemTime** définie dans les fichiers d'en-tête Win32.</span><span class="sxs-lookup"><span data-stu-id="cc6c3-111">A **DTR** structure is very similar to the **SYSTEMTIME** structure defined in the Win32 header files.</span></span> <span data-ttu-id="cc6c3-112">La structure **DTR** est codée dans le flux TNEF en tant qu'octets **sizeof (DTR)** en commençant par le premier membre de la structure.</span><span class="sxs-lookup"><span data-stu-id="cc6c3-112">The **DTR** structure is encoded in the TNEF stream as **sizeof(DTR)** bytes starting with the first member of the structure.</span></span> <span data-ttu-id="cc6c3-113">La structure **DTR** est définie dans le format TNEF. Fichier d'en-tête H.</span><span class="sxs-lookup"><span data-stu-id="cc6c3-113">The **DTR** structure is defined in the TNEF.H header file.</span></span> 
  

