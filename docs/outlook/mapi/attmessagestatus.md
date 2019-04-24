---
title: attMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8f55470a-65b3-4210-a7d2-9031cb17ca80
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d4dc72309ff090317b2353cab0b4fc2c5be41181
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318213"
---
# <a name="attmessagestatus"></a><span data-ttu-id="cfc33-103">attMessageStatus</span><span class="sxs-lookup"><span data-stu-id="cfc33-103">attMessageStatus</span></span>

  
  
<span data-ttu-id="cfc33-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cfc33-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cfc33-105">Les indicateurs de message MAPI sont mappés aux indicateurs TNEF pour conserver la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="cfc33-105">MAPI message flags are mapped to TNEF flags to preserve backward compatibility.</span></span> <span data-ttu-id="cfc33-106">Tous les indicateurs sont regroupés et codés en un seul octet.</span><span class="sxs-lookup"><span data-stu-id="cfc33-106">All the flags are grouped together and encoded in a single byte.</span></span> <span data-ttu-id="cfc33-107">Les mappages sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="cfc33-107">The mappings are as follows:</span></span>
  
|<span data-ttu-id="cfc33-108">**Indicateurs de message MAPI**</span><span class="sxs-lookup"><span data-stu-id="cfc33-108">**MAPI message flags**</span></span>|<span data-ttu-id="cfc33-109">**Indicateurs TNEF**</span><span class="sxs-lookup"><span data-stu-id="cfc33-109">**TNEF flags**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cfc33-110">MSGFLAG_READ</span><span class="sxs-lookup"><span data-stu-id="cfc33-110">MSGFLAG_READ</span></span>  <br/> |<span data-ttu-id="cfc33-111">fmsRead</span><span class="sxs-lookup"><span data-stu-id="cfc33-111">fmsRead</span></span>  <br/> |
|<span data-ttu-id="cfc33-112">MSGFLAG_UNMODIFED</span><span class="sxs-lookup"><span data-stu-id="cfc33-112">MSGFLAG_UNMODIFED</span></span>  <br/> |<span data-ttu-id="cfc33-113">~ fmsModified</span><span class="sxs-lookup"><span data-stu-id="cfc33-113">~fmsModified</span></span>  <br/> |
|<span data-ttu-id="cfc33-114">MSGFLAG_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="cfc33-114">MSGFLAG_SUBMIT</span></span>  <br/> |<span data-ttu-id="cfc33-115">fmsSubmitted</span><span class="sxs-lookup"><span data-stu-id="cfc33-115">fmsSubmitted</span></span>  <br/> |
|<span data-ttu-id="cfc33-116">MSGFLAG_HASATTACH</span><span class="sxs-lookup"><span data-stu-id="cfc33-116">MSGFLAG_HASATTACH</span></span>  <br/> |<span data-ttu-id="cfc33-117">fmsHasAttach</span><span class="sxs-lookup"><span data-stu-id="cfc33-117">fmsHasAttach</span></span>  <br/> |
|<span data-ttu-id="cfc33-118">MSGFLAG_UNSENT</span><span class="sxs-lookup"><span data-stu-id="cfc33-118">MSGFLAG_UNSENT</span></span>  <br/> |<span data-ttu-id="cfc33-119">fmsLocal</span><span class="sxs-lookup"><span data-stu-id="cfc33-119">fmsLocal</span></span>  <br/> |
   
<span data-ttu-id="cfc33-120">Ces indicateurs sont définis dans le format TNEF. Fichier d'en-tête H.</span><span class="sxs-lookup"><span data-stu-id="cfc33-120">These flags are defined in the TNEF.H header file.</span></span>
  

