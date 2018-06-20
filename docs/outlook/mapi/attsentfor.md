---
title: attSentFor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aa8c8d64-d2a0-4cdf-a8aa-21c8d0a0a3fc
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: fd7f79ad7a36fd174bf9817ff463b00e6a334104
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782985"
---
# <a name="attsentfor"></a><span data-ttu-id="635f9-103">attSentFor</span><span class="sxs-lookup"><span data-stu-id="635f9-103">attSentFor</span></span>

  
  
<span data-ttu-id="635f9-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="635f9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="635f9-105">L’attribut **attSentFor** est codée selon les chaînes comptées bout en bout.</span><span class="sxs-lookup"><span data-stu-id="635f9-105">The **attSentFor** attribute is encoded as counted strings laid end-to-end.</span></span> <span data-ttu-id="635f9-106">Le format de **attSentFor** est la suivante :</span><span class="sxs-lookup"><span data-stu-id="635f9-106">The format for **attSentFor** is as follows:</span></span> 
  
 <span data-ttu-id="635f9-107">**attSentFor**:</span><span class="sxs-lookup"><span data-stu-id="635f9-107">**attSentFor**:</span></span> 
  
> <span data-ttu-id="635f9-108">longueur du nom d’affichage du nom d’affichage longueur adresse _adresse de messagerie_</span><span class="sxs-lookup"><span data-stu-id="635f9-108">display-name-length display-name address-length  _email-address_</span></span>
    
 <span data-ttu-id="635f9-109">_adresse de messagerie_</span><span class="sxs-lookup"><span data-stu-id="635f9-109">_email-address_</span></span>
  
> <span data-ttu-id="635f9-110">adresse de type **:**</span><span class="sxs-lookup"><span data-stu-id="635f9-110">type **:** address</span></span> 
    
<span data-ttu-id="635f9-111">Contrairement à d’autres longueur valeurs, la longueur du nom d’affichage et adresse longueur sont des valeurs de 16 bits non signées au lieu d’entiers longs non signés.</span><span class="sxs-lookup"><span data-stu-id="635f9-111">Unlike other length values, the display-name-length and address-length are unsigned 16-bit values instead of unsigned long integers.</span></span> <span data-ttu-id="635f9-112">Elles incluent toujours abandon de caractères null, toutefois.</span><span class="sxs-lookup"><span data-stu-id="635f9-112">They still include terminating null characters, however.</span></span> <span data-ttu-id="635f9-113">Les chaînes de type et l’adresse dans l’entrée _d’adresse de messagerie_ sont séparés par un caractère littéral (deux-points), tel que « smtp:joe@nowhere.com ».</span><span class="sxs-lookup"><span data-stu-id="635f9-113">The type and address strings in the  _email-address_ entry are separated by a literal colon (:) character, such as "smtp:joe@nowhere.com".</span></span> <span data-ttu-id="635f9-114">Uniquement la chaîne d’adresse type combinée **:** est terminée.</span><span class="sxs-lookup"><span data-stu-id="635f9-114">Only the combined type **:** address string is null-terminated.</span></span>
  

