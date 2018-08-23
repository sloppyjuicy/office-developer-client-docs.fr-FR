---
title: attMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8f55470a-65b3-4210-a7d2-9031cb17ca80
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 704707b34fb4532f0e60636df31edbae1a939f35
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565745"
---
# <a name="attmessagestatus"></a><span data-ttu-id="d473b-103">attMessageStatus</span><span class="sxs-lookup"><span data-stu-id="d473b-103">attMessageStatus</span></span>

  
  
<span data-ttu-id="d473b-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d473b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d473b-105">Indicateurs de message MAPI sont mappés aux indicateurs TNEF pour conserver la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="d473b-105">MAPI message flags are mapped to TNEF flags to preserve backward compatibility.</span></span> <span data-ttu-id="d473b-106">Tous les indicateurs sont groupées et codés à un octet.</span><span class="sxs-lookup"><span data-stu-id="d473b-106">All the flags are grouped together and encoded in a single byte.</span></span> <span data-ttu-id="d473b-107">Les mappages sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="d473b-107">The mappings are as follows:</span></span>
  
|<span data-ttu-id="d473b-108">**Indicateurs de message MAPI**</span><span class="sxs-lookup"><span data-stu-id="d473b-108">**MAPI message flags**</span></span>|<span data-ttu-id="d473b-109">**Indicateurs TNEF**</span><span class="sxs-lookup"><span data-stu-id="d473b-109">**TNEF flags**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d473b-110">MSGFLAG_READ</span><span class="sxs-lookup"><span data-stu-id="d473b-110">MSGFLAG_READ</span></span>  <br/> |<span data-ttu-id="d473b-111">fmsRead</span><span class="sxs-lookup"><span data-stu-id="d473b-111">fmsRead</span></span>  <br/> |
|<span data-ttu-id="d473b-112">MSGFLAG_UNMODIFED</span><span class="sxs-lookup"><span data-stu-id="d473b-112">MSGFLAG_UNMODIFED</span></span>  <br/> |<span data-ttu-id="d473b-113">~ fmsModified</span><span class="sxs-lookup"><span data-stu-id="d473b-113">~fmsModified</span></span>  <br/> |
|<span data-ttu-id="d473b-114">MSGFLAG_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="d473b-114">MSGFLAG_SUBMIT</span></span>  <br/> |<span data-ttu-id="d473b-115">fmsSubmitted</span><span class="sxs-lookup"><span data-stu-id="d473b-115">fmsSubmitted</span></span>  <br/> |
|<span data-ttu-id="d473b-116">MSGFLAG_HASATTACH</span><span class="sxs-lookup"><span data-stu-id="d473b-116">MSGFLAG_HASATTACH</span></span>  <br/> |<span data-ttu-id="d473b-117">fmsHasAttach</span><span class="sxs-lookup"><span data-stu-id="d473b-117">fmsHasAttach</span></span>  <br/> |
|<span data-ttu-id="d473b-118">MSGFLAG_UNSENT</span><span class="sxs-lookup"><span data-stu-id="d473b-118">MSGFLAG_UNSENT</span></span>  <br/> |<span data-ttu-id="d473b-119">fmsLocal</span><span class="sxs-lookup"><span data-stu-id="d473b-119">fmsLocal</span></span>  <br/> |
   
<span data-ttu-id="d473b-120">Ces indicateurs sont définis dans le format TNEF. Fichier d’en-tête H.</span><span class="sxs-lookup"><span data-stu-id="d473b-120">These flags are defined in the TNEF.H header file.</span></span>
  

