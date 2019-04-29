---
title: attMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8f55470a-65b3-4210-a7d2-9031cb17ca80
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d4dc72309ff090317b2353cab0b4fc2c5be41181
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430314"
---
# <a name="attmessagestatus"></a><span data-ttu-id="4d77d-103">attMessageStatus</span><span class="sxs-lookup"><span data-stu-id="4d77d-103">attMessageStatus</span></span>

  
  
<span data-ttu-id="4d77d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d77d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d77d-105">Les indicateurs de message MAPI sont mappés aux indicateurs TNEF pour conserver la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="4d77d-105">MAPI message flags are mapped to TNEF flags to preserve backward compatibility.</span></span> <span data-ttu-id="4d77d-106">Tous les indicateurs sont regroupés et codés en un seul octet.</span><span class="sxs-lookup"><span data-stu-id="4d77d-106">All the flags are grouped together and encoded in a single byte.</span></span> <span data-ttu-id="4d77d-107">Les mappages sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="4d77d-107">The mappings are as follows:</span></span>
  
|<span data-ttu-id="4d77d-108">**Indicateurs de message MAPI**</span><span class="sxs-lookup"><span data-stu-id="4d77d-108">**MAPI message flags**</span></span>|<span data-ttu-id="4d77d-109">**Indicateurs TNEF**</span><span class="sxs-lookup"><span data-stu-id="4d77d-109">**TNEF flags**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4d77d-110">MSGFLAG_READ</span><span class="sxs-lookup"><span data-stu-id="4d77d-110">MSGFLAG_READ</span></span>  <br/> |<span data-ttu-id="4d77d-111">fmsRead</span><span class="sxs-lookup"><span data-stu-id="4d77d-111">fmsRead</span></span>  <br/> |
|<span data-ttu-id="4d77d-112">MSGFLAG_UNMODIFED</span><span class="sxs-lookup"><span data-stu-id="4d77d-112">MSGFLAG_UNMODIFED</span></span>  <br/> |<span data-ttu-id="4d77d-113">~ fmsModified</span><span class="sxs-lookup"><span data-stu-id="4d77d-113">~fmsModified</span></span>  <br/> |
|<span data-ttu-id="4d77d-114">MSGFLAG_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="4d77d-114">MSGFLAG_SUBMIT</span></span>  <br/> |<span data-ttu-id="4d77d-115">fmsSubmitted</span><span class="sxs-lookup"><span data-stu-id="4d77d-115">fmsSubmitted</span></span>  <br/> |
|<span data-ttu-id="4d77d-116">MSGFLAG_HASATTACH</span><span class="sxs-lookup"><span data-stu-id="4d77d-116">MSGFLAG_HASATTACH</span></span>  <br/> |<span data-ttu-id="4d77d-117">fmsHasAttach</span><span class="sxs-lookup"><span data-stu-id="4d77d-117">fmsHasAttach</span></span>  <br/> |
|<span data-ttu-id="4d77d-118">MSGFLAG_UNSENT</span><span class="sxs-lookup"><span data-stu-id="4d77d-118">MSGFLAG_UNSENT</span></span>  <br/> |<span data-ttu-id="4d77d-119">fmsLocal</span><span class="sxs-lookup"><span data-stu-id="4d77d-119">fmsLocal</span></span>  <br/> |
   
<span data-ttu-id="4d77d-120">Ces indicateurs sont définis dans le format TNEF. Fichier d'en-tête H.</span><span class="sxs-lookup"><span data-stu-id="4d77d-120">These flags are defined in the TNEF.H header file.</span></span>
  

