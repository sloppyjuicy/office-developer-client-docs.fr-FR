---
title: attOwner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3c6a4050-fd97-42ce-abb1-118254b367bd
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 0cb40c3c644618bdf65a2c90a91580a5be8fc88c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782965"
---
# <a name="attowner"></a><span data-ttu-id="54a3e-103">attOwner</span><span class="sxs-lookup"><span data-stu-id="54a3e-103">attOwner</span></span>

  
  
<span data-ttu-id="54a3e-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="54a3e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="54a3e-105">L’attribut **attOwner** est codée selon les chaînes comptées bout en bout.</span><span class="sxs-lookup"><span data-stu-id="54a3e-105">The **attOwner** attribute is encoded as counted strings laid end-to-end.</span></span> <span data-ttu-id="54a3e-106">Le format de **attOwner** est la suivante :</span><span class="sxs-lookup"><span data-stu-id="54a3e-106">The format for **attOwner** is as follows:</span></span> 
  
 <span data-ttu-id="54a3e-107">**attOwner**:</span><span class="sxs-lookup"><span data-stu-id="54a3e-107">**attOwner**:</span></span> 
  
> <span data-ttu-id="54a3e-108">longueur du nom d’affichage du nom d’affichage longueur adresse _adresse de messagerie_</span><span class="sxs-lookup"><span data-stu-id="54a3e-108">display-name-length display-name address-length  _email-address_</span></span>
    
 <span data-ttu-id="54a3e-109">_adresse de messagerie_</span><span class="sxs-lookup"><span data-stu-id="54a3e-109">_email-address_</span></span>
  
> <span data-ttu-id="54a3e-110">adresse de type **:**</span><span class="sxs-lookup"><span data-stu-id="54a3e-110">type **:** address</span></span> 
    
<span data-ttu-id="54a3e-111">Contrairement à d’autres longueur valeurs, la longueur du nom d’affichage et adresse longueur sont des valeurs de 16 bits non signées au lieu d’entiers longs non signés.</span><span class="sxs-lookup"><span data-stu-id="54a3e-111">Unlike other length values, the display-name-length and address-length are unsigned 16-bit values instead of unsigned long integers.</span></span> <span data-ttu-id="54a3e-112">Elles incluent toujours abandon de caractères null, toutefois.</span><span class="sxs-lookup"><span data-stu-id="54a3e-112">They still include terminating null characters, however.</span></span> <span data-ttu-id="54a3e-113">Les chaînes de type et l’adresse dans l’entrée _d’adresse de messagerie_ sont séparés par un caractère littéral (deux-points), tel que « smtp:joe@nowhere.com ».</span><span class="sxs-lookup"><span data-stu-id="54a3e-113">The type and address strings in the  _email-address_ entry are separated by a literal colon (:) character, such as "smtp:joe@nowhere.com".</span></span> <span data-ttu-id="54a3e-114">Uniquement la chaîne d’adresse type combinée **:** est terminée.</span><span class="sxs-lookup"><span data-stu-id="54a3e-114">Only the combined type **:** address string is null-terminated.</span></span>
  
<span data-ttu-id="54a3e-115">Le mappage des propriétés MAPI à l’attribut **attOwner** dépend de la classe de message du message encodé.</span><span class="sxs-lookup"><span data-stu-id="54a3e-115">The mapping of MAPI properties to the **attOwner** attribute is dependent on the message class of the message being encoded.</span></span> 
  

